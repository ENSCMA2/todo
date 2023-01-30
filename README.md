# Svelte To-Do App: Notes For CS178 Assignment
This repo contains a Svelte to-do app, with comments for examples of software concepts discussed in Lecture 2 of CS178, spring 2023. Citations:  
- I ripped the entirety of of this app from [Mozilla's MDN Web Docs tutorial](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_deployment_next). I only changed some button colors and font styles.  
- I used [this W3Schools page](https://www.w3schools.com/cssref/index.php) to learn about and implement some CSS style properties.  
- I used [this Svelte tutorial section](https://svelte.dev/tutorial/await-blocks) to learn about and help myself find examples of asynchronous programming.  
- After realizing that there were no `await` blocks in this code, I discovered that there was still asynchronous programming because of the direct use of JavaScript `Promises`, and that was with the help of the explanations on [this page](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) and [this page](https://www.w3schools.com/tags/att_script_defer.asp). This code uses `defer`, which is a form of asynchronous programming.  
- I used [this explanation](https://svelte.dev/tutorial/writable-stores) to learn about and find examples of the reactive programming concept through writable stores.
- Many thanks to Ziwei Gu for his responses on EdStem that helped clarify the assignment, which led me to initially (though unsuccessfully) try [this tutorial](https://fireship.io/lessons/svelte-v3-overview-firebase/), and thanks to the anonymous students who posted questions that prompted these helpful responses.  
---Below is the documentation from [Mozilla's MDN Web Docs tutorial](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_deployment_next) that I used to make this app (or rather, I ripped the whole app directly from the tutorial and changed a few colors and borders).---
# Source code for Svelte Tutorials at MDN Web docs

Source code of the To-Do list app for the Svelte tutorials at [Understanding client-side JavaScript frameworks](Understanding client-side JavaScript frameworks) series at MDN Web docs.

## 08. Deployment and next Steps

In this article we will learn about a couple of zero-fuss options to deploy our app in production and see how to setup a basic pipeline to deploy our app to GitLab on every commit. We will also provide a list of Svelte resources to go further with your Svelte learning.

You can see the complete content of this article [here](../08-next-steps/Svelte_next_steps.md) or at [MDN web docs](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Svelte_deployment_next).

The source code to follow this article is in the `08-next-steps` folder, you can download it with the `npx degit opensas/mdn-svelte-tutorial/08-next-steps svelte-todo` command. 
---

*Looking for a shareable component template? Go here --> [sveltejs/component-template](https://github.com/sveltejs/component-template)*

---

# svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## Get started

Install the dependencies...

```bash
cd svelte-app
npm install
```

...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.


## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```


## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within your project folder:

```bash
cd public
now deploy --name my-project
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
# todo
