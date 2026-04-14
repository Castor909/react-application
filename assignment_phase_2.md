# React application: Phase 2 (dynamic data and API integration)

## Objective

Upgrade your static prototype into a dynamic, multi-page React application. You will connect your UI to the local Athletics Sports Club REST API, handle asynchronous data fetching, manage loading and error states, and implement routing.

## 1. Planning and design setup

Go through the following steps before you start coding.

### User stories and mock-ups

Your application must now represent the UI for exactly **four** user stories. Reuse your stories from phase 1 and create the necessary new ones to reach four. For the new stories, deliver the same visual assets as before:

- Set the title using the format: _"As a [persona], I want [goal] so that [benefit]."_
- Define a workflow that solves it. Include forks, arrows, error messages, cancellations, and alternative endings.
- Create the mock-up representing the steps the user follows to achieve it, and use arrows to define the flow. Use labels to highlight relevant details.
- **Format:** Delivered as a single file (image or vector) per story.

### Updated component hierarchy map

Update your previous diagram to include the new components and the new routes/pages. Identify where the new fetch requests will happen and how the data will be passed down as props.

## 2. Technical requirements

Your work must meet the following technical requirements:

### API Integration (GET requests only)

You must run the provided Athletics Sports Club API locally using Docker Compose. Replace your previous static JSON imports with the fetch() API to retrieve real data from the backend. Focus strictly on *implementing the read-only parts* of your user stories. Keep in mind that, in phase 3, you will complete these stories by adding the write operations (create, update, delete). For now, focus on presenting the data.

### Endpoints

You must use **all the necessary GET endpoints** required to completely fulfill the read operations for your 4 user stories. Available endpoint bases include /athletes, /coaches, /venues, /competitions, /trainings, /seasons, and /addresses. You should utilise both list endpoints (e.g., /api/v1/athletes) and detail endpoints (e.g., /api/v1/athletes/{public_id}) as dictated by your designs.

### Component expansion

Add at least **3 new functional components** to your project to accommodate the new user stories and data presentation.

### State and asynchrony

Use useEffect and useState, add loading and error states:

- Use useEffect to trigger your fetch calls when the relevant components mount.
- Use useState to store the incoming JSON data.
- You must implement a **loading state** (e.g., showing a spinner, skeleton loader, or "Loading..." text while waiting for the API response) and an **error state** (e.g., a gracefully designed error message if the fetch fails or the Docker container is not running).

### Mandatory routing

Implement react-router-dom to create actual navigation. Your app must have at least two distinct views (e.g., a global navigation bar that switches between /athletes and /competitions, or clicking on a list item to navigate to a detail page).

### Component quality and clean code

React code must follow industry best practices for readability and separation of concerns.

- **No spaghetti code.** Do not put all your logic, styling, and UI into a single massive component. Break complex UIs into smaller, reusable child components.
- **Keep JSX clean.** The return (...) block of your component should primarily contain UI. Complex JavaScript logic, data filtering, and event handler functions should be defined above the return statement.
- **Styling practices.** Avoid heavy use of inline styles, e.g., style={{ color: 'red', margin: '10px' }}. Use standard external CSS files, CSS modules, or a consistent styling framework to keep your component files clean.
- **Semantic HTML.** Avoid a div soup. Use semantic HTML tags (<header>, <main>, <section>, <nav>, <button>) inside your JSX.

## 3. Deliverables

You must submit the following:

- **The user stories.** A single image or vector file per story (including your previous ones), containing the workflow and mock-ups. Name the files user-story-<name-or-description>.<extension>.
- **The updated component hierarchy map.** A single image, exported from your diagram. Name the file chm.extension.
- **README.md.** Update your Markdown file as necessary. You do not need to include the `docker compose up -d` command used to launch the backend (REST API). Include any extra context for grading.
- **The source code.** A ZIP archive containing your Vite project files. Do not include the node_modules folder in your archive. Use ZIP format.
- **Link to repo.** Optionally, a link to the public GitHub repository hosting your code.

## Grading rubric (visible categories)

- User stories and mock-ups — /15
- Updated component map — /10
- Component expansion — /15
- API integration (fetch) — /25
- Asynchronous UI states — /15
- Routing (react-router-dom) — /10
- Execution and deliverables — /10
- Code quality and best practices — /10

**Total:** /110
