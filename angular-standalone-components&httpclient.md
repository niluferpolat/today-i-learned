## HttpClient

Angular provider http client module that simplifies making HTTP requests and handling responses in the application. 

I set up HTTPClient as shown below:

<img width="643" height="413" alt="image" src="https://github.com/user-attachments/assets/066bc2a9-081b-499b-bf08-363dc0ba0fa7" />

Then i write service like that: 

```bash
import { HttpClient } from '@angular/common/http';
import { inject, Injectable } from '@angular/core';
import { Observable } from 'rxjs';
import {TaskEntity} from '@task-manager-workspace/models'
import { environment } from '../../environments/environment';

@Injectable({
  providedIn: 'root'
})
export class TaskService {
  private http = inject(HttpClient);
  private baseUrl = environment.apiBaseUrl;

  getTasks():Observable<TaskEntity[]> {
    return this.http.get<TaskEntity[]>(`${this.baseUrl}/tasks`);
  }
}

```

<img width="533" height="419" alt="image" src="https://github.com/user-attachments/assets/a0982136-de70-4515-86cf-ac7d5a856353" />
I used the service that i write is like that. 

