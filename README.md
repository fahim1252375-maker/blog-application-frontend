# BlogSpace — Frontend

BlogSpace is a browser-based blogging interface I built to practise multi-page frontend development. It has a public reading experience as well as screens for signing in and managing posts.

**Live demo:** https://bejewelled-haupia-dd6200.netlify.app  
**Source:** https://github.com/fahim1252375-maker/blog-application-frontend

## What you can try

- Browse article cards on the homepage
- Search articles and filter them by category
- Open an article in the reader modal
- Explore the login and registration screens
- Open the author dashboard
- Create, edit, publish, and delete demo posts
- Resize the page to see the responsive layouts

The dashboard and post actions are part of the frontend demonstration. They are not connected to the separate BlogSpace backend in this repository.

## Built with

- HTML5 and CSS3
- Vanilla JavaScript using ES modules
- Vite
- LocalStorage for demo data

## Run it locally

You will need Node.js and npm.

~~~bash
git clone https://github.com/fahim1252375-maker/blog-application-frontend.git
cd blog-application-frontend
npm install
npm run dev
~~~

Vite prints the local address in the terminal.

## Project checks

The repository includes these scripts:

~~~bash
npm run lint
npm test
npm run build
~~~

Run them on your current checkout before treating the result as a verified build.

## A note about the demo

This version stores its sample posts and interface state in the browser with LocalStorage. It does not provide real account authentication, shared user data, or server-side persistence. Please do not use real passwords or private information in the demo.

For the API-backed version, see [BlogSpace Full-Stack](https://github.com/fahim1252375-maker/blogspace-fullstack).

---

A frontend project by MD. Minhazur Rahman Fahim.
