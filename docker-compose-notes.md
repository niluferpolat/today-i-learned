## What is Docker? 
<img width="725" height="630" alt="image" src="https://github.com/user-attachments/assets/a934b01d-548b-4339-8105-fe4e2d41d607" />

Docker is an open-source platform for packaging, distributing, and running applications.

Its working principle is based on **containers.**

<ul>
  <li>
    Containers allow us to separate applications and their components, making Docker fast, consistent, and portable.
  </li>
  <li>
    With Docker, applications can be delivered quickly and run reliably across different environments.
  </li>
</ul>

In short, Docker makes it easier to build, ship, and run applications anywhere.

## What is Docker Compose?

Docker compose a toll that allows us to define and manage multiple Docker containers simultaneously. 
For example you can create individual containers for each part of your application: one for web server,one for DB,another one for caching service.
Then you define a **docker-compose.yml** file where you specify how these containers should work together. This file includes the details such as images to use,network settings etc.
Finally, you can run with a single command: 
```
docker-compose up
```
Docker compose starts and manages all the defined containers.

