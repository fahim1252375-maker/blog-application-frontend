# BlogSpace — Frontend

A responsive, browser-based blogging interface built to practise multi-page frontend development. It includes a public reading experience as well as screens for signing in and managing posts.

**Live demo:** https://bejewelled-haupia-dd6200.netlify.app  
**Source:** https://github.com/fahim1252375-maker/blog-application-frontend

## Features

- Browse article cards on the homepage
- Search articles and filter them by category
- Open an article in the reader modal
- Explore login and registration screens
- Open the author dashboard
- Create, edit, publish, and delete demonstration posts
- Responsive layouts for different screen sizes

The dashboard and post actions are part of the frontend demonstration. They are not connected to the separate BlogSpace backend in this repository.

## Built With

- HTML5 and CSS3
- Vanilla JavaScript using ES modules
- Vite
- LocalStorage for demonstration data

## Run Locally

You will need Node.js and npm.

~~~bash
git clone https://github.com/fahim1252375-maker/blog-application-frontend.git
cd blog-application-frontend
npm install
npm run dev
~~~

Vite prints the local address in the terminal.

## Project Checks

The repository includes these scripts:

~~~bash
npm run lint
npm test
npm run build
~~~

Run them on your current checkout before treating the result as a verified build.

## Demo Scope and Data Handling

This version stores sample posts and interface state in the browser with LocalStorage. It does not provide real account authentication, shared user data, or server-side persistence. Do not use real passwords or private information in the demo.

For the API-backed version, see [BlogSpace Full-Stack](https://github.com/fahim1252375-maker/blogspace-fullstack).

## AI Use Disclosure

AI tools may be used as supporting aids for brainstorming, explaining concepts, debugging, and drafting documentation. The project author is responsible for reviewing, adapting, understanding, and testing published work. AI suggestions are not treated as verified results unless checked against the actual implementation.

---

A frontend learning and portfolio project by MD. Minhazur Rahman Fahim.
