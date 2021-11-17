# What is Svelte? [![Cybernetically enhanced web apps: Svelte](https://avatars.githubusercontent.com/u/23617963?s=40)](https://github.com/josh-hernd/svelte-dockerized)
Svelte is a new way to build web applications. It's a compiler that takes your declarative components and converts them into efficient JavaScript that surgically updates the DOM.

Learn more at the [Svelte website](https://svelte.dev), or stop by the [Discord chatroom](https://svelte.dev/chat).

# Before we begin
SvelteKit is in early development, and there are a lot of bugs. That being said everything on this build is working correctly with the exception of routing. For an unknown reason when a new path is created while docker container is running, it does not render the newly created page. Dirty work around is simply restarting the container.


# Development

```
    git clone https://github.com/josh-hernd/svelte-dockerized
    npm install
```

Run a local dev test

```
    npm run dev -- --host --open
```
[localhost:3000](http://localhost:3000/) will open on browser

# Dockerizing Svelte

For faster builds

```
    COMPOSE_DOCKER_CLI_BUILD=1 DOCKER_BUILDKIT=1 docker-compose build
    
    # or simply

    docker-compose up -d
```
For detatched build use **-d** flag
```
    docker-compose up -d 
```
Removing build. **--volumes** flag will remove all Containers/App

```
    docker-compose down --volumes
```
For clearing build cache 

```
    docker builder prune --all
```