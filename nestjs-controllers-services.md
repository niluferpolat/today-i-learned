## NESTJS
<img width="319" height="225" alt="image" src="https://github.com/user-attachments/assets/260bdbde-10be-4f2d-8266-24f41191d4bc" />

  NestJS is a framework for building efficient,scalable serverside Nodejs applications. 

### Installation
In the documentation we can install and create a new project as shown in the below:

```bash
 npm i -g @nestjs/cli
 nest new project-name
```
But since I am using an Nx monorepo workspace, I added NestJS with this command:

```
npm i -D @nx/nest@latest
npm install -D @nx/nest@latest --legacy-peer-deps
```

<img width="424" height="251" alt="image" src="https://github.com/user-attachments/assets/1412f0f5-00d8-4354-a417-47f14948a20b" />

This is how app.module.ts seems like. The controllers,providers and imports are automatically added when we created the project at first time.

I added **task.controller** in my project with this command:

```
 nx g @nx/nest:controller apps/task-manager-be/src/app/task.controller.ts
```
But for a standalone nestjs project you can generate controller with 
```
nest g controller controllerName
```


```
import { Controller, Delete, Get, Param } from '@nestjs/common';
import { TaskService } from './task.service';

@Controller('task')
export class TaskController {
    constructor(private readonly taskService: TaskService) {}
    @Get()
    findAll(){
        return this.taskService.findAll(2);
    }

    @Delete("delete/:id")
    deleteTask(@Param('id') id:string){
        return this.taskService.delete(Number(id))
    }
}
```
This is my example controller. 

Then i added service.

```
 nx g @nx/nest:service apps/task-manager-be/src/app/task
```

This is my example service.

```
@Injectable()
export class TaskService {
    private tasks = [
        {
            id: 1,
            status:"DONE",
            userId:2,
            taskText: "Buy some suppliers"
        },
         {
            id: 2,
            status:"UNDONE",
            userId:2,
            taskText: "Wash the dishes"
        }
    ]

    findAll(userId: number){
        return this.tasks.filter(task=> task.userId === userId);
    }
    findOne(id: number){
        return this.tasks.filter(task=>task.id === id);
    }
    delete(id: number){
        return this.tasks.filter(task=>task.id !== id);
    }

}
```


