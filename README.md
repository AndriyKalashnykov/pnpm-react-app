# Create a front-end app with React with PNPM


## Requirements

* [nvm](https://github.com/nvm-sh/nvm#install--update-script)
  ```bash
  nvm install v17.4.0
  nvm use v17.4.0
  ```
* [pnpm](https://pnpm.io/installation)


## Create react app
```bash
pnpm create react-app pnpm-cra --template typescript
```

## Install modules

```
pnpm install
```

## Upgrade modules
```
pnpm update upgrade
```

## Build production

```
pnpm build
```

## Run

```
pnpm run
```

## Build Docker image

```bash
docker build -t pnpm-react-app .
```

## References

* [Set up a modern web app by running one command](https://github.com/facebook/create-react-app)
* [Setup a Monorepo with PNPM workspaces and speed it up with Nx!](https://blog.nrwl.io/setup-a-monorepo-with-pnpm-workspaces-and-speed-it-up-with-nx-bc5d97258a7e)
* [How To Set Up a React Project with Create React App](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-react-project-with-create-react-app)
* [Ant design](https://ant.design/docs/react/use-in-typescript)
* [Best practices for using PNPM with docker monorepo](https://github.com/pnpm/pnpm/issues/3114)
