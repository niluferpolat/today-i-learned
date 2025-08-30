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

#### The problems i faced with
````
 it will be ignored, please remove it to avoid potential confusion"
unable to get image 'node:20-alpine': request returned 500 Internal Server Error for API route and version
````
When i open docker desktop i saw this problem:
<img width="821" height="449" alt="image" src="https://github.com/user-attachments/assets/e4bab71b-a83e-4c71-9694-84bcd8dc9b65" />

I downloaded wsl msi. You can find the details from this link [WSL](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiI86XllrOPAxXzcfEDHa6NFa0QFnoECAwQAQ&url=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Fwindows%2Fwsl%2Finstall&usg=AOvVaw3NDNYJVUKnKqnP9DjgAR3M&opi=89978449)

<img width="650" height="214" alt="image" src="https://github.com/user-attachments/assets/acc24e7a-90ec-4215-9e15-6652e853f542" />

Now it works!



