# Custom react scripts with integrated relay support
Latest version of original react-scripts: **0.8.4**

### ⚠️ Disclaimer:
> This is **not** a fork of ```create-react-app```. It's just a fork of ```react-scripts``` with simple babel/webpack modifications that can toggle extra features.

The reason for this fork's existence is explained better in [this Medium article](https://medium.com/@kitze/configure-create-react-app-without-ejecting-d8450e96196a).

### Instalation
```
npm i -D @valentin-seehausen/react-scripts
```
Afterwards check your `package.json` for ```"react-script": "~> 0.8.4",``` and delete the whole line.

### 💡Features:
Relay

### ❔How to use it
1. Add a `.env` file to your root directory (next to your `package.json`file) and write `REACT_APP_GRAPHQL_URL=http://localhost:4000/graphql` with a link to your graphql server.
2. Add a line to your `package.json`: ```"proxy": "http://localhost:4000",``` (without */graphql*) that links to your graphql server.

Ready to go. When you start and build your application, the plugin will automatically fetch your schema and save it into your repository.

### Original Code comes from

This is a fork of [svrcekmichal/create-react-app](https://github.com/svrcekmichal/create-react-app).
All the work is taken from this [PR](https://github.com/facebookincubator/create-react-app/pull/662) which was not published, because
Relay is out of scope of most CRA packages. This work would be not possible without [@saintsjd](https://github.com/saintsjd) and [@maxwell-oroark](https://github.com/maxwell-oroark) work and many contributors.
Thanks to [@kitze](https://github.com/kitze) for structure of this readme

### Future plans

I will put all of my efforts into supporting this fork to be always on par with features with the newest ```create-react-app``` and ```react-scripts``` versions.
