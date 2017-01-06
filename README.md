> Latest version of original react-scripts: **0.8.4**
### ⚠️ Disclaimer:
> This is **not** a fork of ```create-react-app```. It's just a fork of ```react-scripts``` with simple babel/webpack modifications that can toggle extra features.

# Relay for create-react-app
It is quite difficult to get relay up and running with create-react-app. Here is a react-script, that you can use to get relay support with your create-react-app app. You can also fork this repo and add other features, this is only meant to provide relay support.

The reason for this fork's existence is explained better in [this Medium article](https://medium.com/@kitze/configure-create-react-app-without-ejecting-d8450e96196a).

### Installation
1. ```npm i -D @valentin-seehausen/react-scripts```
2. Check your `package.json` for ```"react-script": "~> 0.8.4",``` and delete the whole line.
3. Add a `.env` file to your root directory (next to your `package.json`file) and write `REACT_APP_GRAPHQL_URL=http://localhost:4000/graphql` with a link to your graphql server.
4. Add a line to your `package.json`: ```"proxy": "http://localhost:4000",``` (without */graphql*) that links to your graphql server.

Ready to go. When you start and build your application, the plugin will automatically fetch your schema and save it into your repository.

### Original Code comes from

This is a fork of [svrcekmichal/create-react-app](https://github.com/svrcekmichal/create-react-app).
All the work is taken from this [PR](https://github.com/facebookincubator/create-react-app/pull/662) which was not published, because
Relay is out of scope of most CRA packages. This work would be not possible without [@saintsjd](https://github.com/saintsjd) and [@maxwell-oroark](https://github.com/maxwell-oroark) work and many contributors.
Thanks to [@kitze](https://github.com/kitze) for structure of this readme
