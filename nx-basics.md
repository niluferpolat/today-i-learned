# What is Monorepo?
A Monorepo (monolithic repository) is a version control strategy where multiple projects and components are stored in a single repository.

# What is Nx?
Nx is an open-source build platform designed to manage codebases of any scale. It helps when codebases or teams grow. Nx is designed to reduce build times and split code into smaller parts, making projects more manageable.

To install the Nx CLI you can use this command:


```
npm add --global nx
```

To start a new project you can use this command.

```
npx create-nx-workspace@latest
```

### What is the difference between applications and libraries?
- **Applications** are executable programs that you can serve and deploy. They are meant to be standalone.  
- **Libraries** are collections of reusable code that can be shared across multiple applications. They contain components, services, and functions. They are imported into other applications.  

In an Nx workspace, applications are located in the **apps/** folder and libraries are located in the **libs/** folder.

To generate a nx dependency graph use this command:
```
nx dep-graph
```
It is used to visualize your workspace.

To check whether any change affect a project or not,use this command:

```
nx graph --affected
```

