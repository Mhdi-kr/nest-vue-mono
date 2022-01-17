# Fullstack Application boilerplate

## Getting started

install pnpm package manager globally

```Bash
npm i -g pnpm
```

install project dependecies

```Bash
pnpm install --recursive
```

run the project for development, the following command will concurrently run client and server packages on different ports.

```Bash
pnpm run dev
```

you can run pacakges in isolation like

```Bash
# pnpm run PACKAGE_NAME:SCRIPT_KEY

pnpm run client:build
pnpm run server:dev
```

## Tech Stack

### Frontend

The application uses:

-   vue 3 as the frontend framwork
-   vite build system
-   tailwind css as the css library
-   vue router
-   vite PWA module

### Backend

The application uses:

-   Nestjs backend framwork

### Deployment

The project uses `docker-compose.yml` to scaffold project. Each and every can have its own `dockerfile` so it can be run in isolation.
