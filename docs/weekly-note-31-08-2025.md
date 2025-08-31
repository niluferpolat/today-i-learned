# Week 1 – Progress Log

---

### Day 1 (25.08.2025)
- Installed **NX CLI** and created a new monorepo (`task-manager-workspace`).
- Added Angular frontend (`task-manager-fe`) and NestJS backend (`task-manager-be`).
- Created shared **Task model** in `/libs/models`.

<img width="281" height="141" alt="Task Model" src="https://github.com/user-attachments/assets/e3fe343a-e73e-4cb4-a8e3-2183a8bff3ed" />


---

### Day 2 (26.08.2025)
- Removed default app files to clean up the structure.
- Implemented **TaskController** and **TaskService**.
- Exposed basic endpoints: `GET /tasks`, `DELETE /tasks/:id`.

```ts
@Get()
findAll() {
  return this.taskService.findAll(2);
}

@Delete("delete/:id")
deleteTask(@Param('id') id:string) {
  return this.taskService.delete(Number(id));
}
```
<img width="1534" height="870" alt="Controller Example" src="https://github.com/user-attachments/assets/6b06e11e-83da-4dd8-b436-76674e7a902d" />
This was my first backend CRUD implementation with NestJS.

-----
### Day 4 (28.08.2025)
- Edited the code to make it clean and added Angular TaskService to consume backend API.
- Build a mock UI component to render tasks.
---
### Day 6 (30.08.2025) 
- Added redis and kafka for possible future use.
- Added ``` POST /create ``` endpoint in the backend.
- Added Dockerfiles to run the both of projects simultaneously.
---
### Day 7 (31.08.2025)
- Wrote a weekly recap
- Started exploring Spring Cloud concepts and documented.
  
  

  
  
