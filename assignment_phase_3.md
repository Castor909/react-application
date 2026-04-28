# React application: Phase 3 (forms, mutations and dockerization)

Complete your React application by implementing the write operations (create, update, delete) required by your user stories. Build controlled forms, manage form state with `useState`, provide clear UI feedback for user actions, and optionally containerize your frontend.

## 1. Planning and design setup

Follow these steps before you start coding:

- Review and update your user stories and mock-ups.
- Update the component hierarchy to include new form components, UI feedback elements, and where mutation functions are passed as props.

### User stories and mock-ups

Your application must represent the UI for exactly six user stories.

- First, complete your 4 previous user stories by adding the necessary "write" operations (for example, if you had a read-only list, add the ability to create, edit, or delete items). Update mock-ups and workflows to reflect these additions.
- Second, create 2 new user stories that focus on data mutation so the total is six.
- Ensure your mock-ups explicitly show UI feedback (success messages, error toasts, validation warnings) for all write operations.
- Format: deliver one image (raster or vector) per user story.

### Updated component hierarchy map

Update your component diagram to include the new form components, UI feedback elements (toasts, modals, inline messages), and where mutation functions (POST, PUT/PATCH, DELETE) are passed down as props.

## 2. Technical requirements

### Forms and State management

Build HTML forms in React to capture user input using controlled components — bind input fields to `useState` and manage the form state before sending it to the API.

### All HTTP verbs

Across your 6 user stories, you must use every standard HTTP verb at least once:

- `GET` (read)
- `POST` (create)
- `PUT` or `PATCH` (update)
- `DELETE` (delete)

### UI feedback and error handling

Submitting data to a server takes time and can fail. Implement visual feedback for all write operations:

- Disable submit buttons while a request is processing (loading state).
- Show a clear success message or gracefully redirect the user on successful `POST`, `PUT`/`PATCH`, or `DELETE`.
- Show a friendly, well-designed error message if the API rejects the submission.

Tips:

- Use optimistic or pessimistic UI updates consistently and document your choice in the README.
- Validate inputs on the client and show inline validation warnings prior to submission.

### Component expansion

Ensure your application has a minimum of 6 functional components in total, separating lists, detail views, and forms into reusable child components.

### Component quality and clean code

Follow industry best practices for readability and separation of concerns:

- No spaghetti code: don't put all logic, styling, and UI into a single massive component. Break complex UIs into smaller, reusable child components.
- Keep JSX clean: the `return (...)` of your component should primarily contain UI. Complex JavaScript logic, data filtering, and event handlers should be defined above the return statement.
- Styling practices: avoid heavy use of inline styles (for example, `style={{ color: 'red' }}`); prefer external CSS files, CSS modules, or a consistent styling framework.
- Semantic HTML: use semantic tags such as `<header>`, `<main>`, `<section>`, `<nav>`, and `<button>` inside your JSX (avoid unnecessary `<div>` soup).

## 3. Extra credit: Dockerization

Optional: containerize your React frontend using a multi-stage Docker build.

Guidelines:

- Use a Node.js image to copy your source code, run `npm install`, and run `npm run build` to generate the production static files in `dist/` or `build/`.
- Use a lightweight NGINX image (for example, `nginx:alpine`) to serve the contents of that `dist/` (or `build/`) folder.
- You do not need to modify any backend `docker-compose.yml` or the backend NGINX config — provide a working `Dockerfile` and a simple `docker-compose.yml` inside a `docker/` subdirectory for this frontend-only packaging.

Example multi-stage Dockerfile outline (document in README):

1. Build stage: use `node:18-alpine` (or similar) to install dependencies and run the build.
2. Serve stage: use `nginx:alpine` to copy build output into the NGINX `html` folder and serve it.

## 4. Deliverables

You must submit the following:

- The user stories: one image or vector file per story (6 files total) containing the updated workflows and mock-ups. Name each file `user-story-<name-or-description>.<ext>`.
- The updated component hierarchy map: your updated diagram or structured list. Name the file `chm.<ext>`.
- `README.md`: update your project README with exact steps to install dependencies and run the frontend. If you attempted Docker extra credit, include the exact Docker commands to build and run your frontend container.
- The source code: a ZIP archive containing your Vite project files. Do not include `node_modules/` or the `dist/` (or `build/`) folder in the archive.
- Link to repo (optional): a public GitHub repository link hosting your code.

## Notes and grading hints

- Demonstrate the full CRUD workflow across your six stories and show each HTTP verb at least once.
- Make sure UI feedback is visible in mock-ups and implemented in the app (loading states, success messages, and error handling).
- Keep components small and focused; show separation between presentation and logic where sensible.

## Grading rubric

The project will be evaluated across the following categories (points shown per category):

- **User stories and mock-ups:** 15 — completeness and clarity of the six user stories and their mock-ups.
- **Updated component map:** 10 — clear component hierarchy showing forms, feedback elements, and props flow.
- **Forms and state management:** 20 — use of controlled components, `useState` management, and validation.
- **API mutations (HTTP verbs):** 20 — correct use of `POST`, `PUT`/`PATCH`, and `DELETE` across stories (plus `GET`).
- **UI feedback and error handling:** 20 — loading states, success messages, and friendly error handling for write operations.
- **Execution and architecture:** 15 — build/run instructions, structure, and correct use of tools (e.g., build output).
- **Code quality and best practices:** 10 — readable, modular components, semantic HTML, and styling conventions.
- **Extra credit: Dockerization:** 10 — working multi-stage `Dockerfile` and optional `docker-compose.yml` to serve the built frontend.

---

If you want, I can also:

- produce the component hierarchy diagram in text or simple ASCII/tree form,
- create a starter `Dockerfile` and `docker-compose.yml` in a `docker/` folder, or
- convert this file into a shorter checklist tailored to your repo structure.

Please tell me which of the optional extras you'd like me to do next.
