---
id: how to make this site
title: How to make this site
author: Auryn Macmillan
tags: [docusaurus]
---

Install git
Install npm
Install yarn

## Create empty GitHub repo
If you want to serve it from `[github user/org name].github.io` then you need to name the repo `[github user/org name].github.io`.
If you're ok with it serving from a subfolder, `[github user/org name].github.io/[repo name]`, then call the repo whatever you want the subfolder to be called.
You can also serve from a custom domain, you can name the repo whatever you like.

## Initialize docusaurus
`npx @docusaurus/init@next init [github repo name] classic`

## Initialize git repo and push it to your empty GitHub repo
`cd [github repo name]`
`git init`
`git add .`
`git commit -m "docusaurus init"`
`git remote add origin git@github.com:[github user or org name]/[github repo name].git`
`git push -u origin master`

## Build and serve the build from GitHub pages
Modify your `docusaurus.config.js` file as follows.

```js
url: '[github user/org name].github.io', // or your custom domain
baseUrl: '/', // or "/projectName/" if your hosting from a subfolder
organizationName: '[GitHub user/org name]', // Usually your GitHub org/user name.
projectName: '[GitHub repo name]', // Usually your repo name.
```

If you're using a custom domain for GitHub Pages, create a `CNAME` file in the static directory.
