# Build and deploy a blog using Docusaurus 2

## Prerequisites

- node version 16.14 or higher
- pnpm || yarn || npm

## Create the project structure

```bash
pnpx create-docusaurus@latest build-and-deploy-a-blog-using-docusaurus2 classic
```

## Using commands in the project directory

```bash
cd build-and-deploy-a-blog-using-docusaurus2
## Start the local development server.
pnpm start
## Build the static website ready to be deployed.
pnpm build
## Launch a local web server to test the static website.
pnpm serve
## Deploy the static website to GitHub Pages.
pnpm deploy
```

## Configuration of the Docusaurus Blog function

To configure the Docusaurus Blog function, you need to modify the `docusaurus.config.js` file by adding the following configuration:

```js
module.exports = {
  themeConfig: {
    // ...
    navbar: {
      items: [
        // ...
        { to: "blog", label: "Blog", position: "left" }, // ou position: 'right'
      ],
    },
  },
};
```

## Deploy the static website to GitHub Pages

To deploy the static website to GitHub Pages, you need to modify the `docusaurus.config.js` file by adding the following configuration:

```js
module.exports = {
  // ...
  url: "https://<your-github-username>.github.io",
  baseUrl: "/<your-repo-name>/",
  onBrokenLinks: "throw",
  onBrokenMarkdownLinks: "warn",
  favicon: "img/favicon.ico",
  organizationName: "<your-github-username>", // Usually your GitHub org/user name.
  projectName: "<your-repo-name>", // Usually your repo name.
  trailingSlash: false,
  //...
};
```
