# React Static Application Assignment (Vite)

## Objective

Transform your wireframes into a functional, **static** React application using Vite.  
You will implement your design guidelines (style book), establish a clear component hierarchy, and manage local state by importing mock data from JSON files.

---

## 1. Planning and Design Setup

Go through the following steps before you start coding.

### User stories and mock-ups

Your prototype must represent the UI for **two user stories** related to the Athletics Sports Club domain.

- If you already delivered two user stories in previous assignments, you may reuse them.
- If not, create what is missing.
- The delivery for these user stories must follow the same specific guidelines as before:

1. Set the title of the user story using this format:  
	`As a [persona], I want [goal] so that [benefit].`
2. Define a workflow that solves it. Include forks, arrows, labels, error messages, cancellations, and alternative endings.
3. Create the mock-up that represents the steps the user follows to achieve it, and use arrows to define the flow.
4. Use labels to highlight relevant details.
5. Ideally, use the same image for the workflow and the mock-up (separate images are also acceptable).
6. **Format:** deliver as a single file (image or vector).

### Component hierarchy map

Map out your React components based on your wireframes. Identify:

- Parent components
- Child components
- Where data needs to be passed as `props`

### Styling

Apply the color palette and typography from your style book.  
Using a CSS framework (for example, Bootstrap or Tailwind) is optional.

---

## 2. Technical Requirements

Your work must meet the following technical requirements:

### Use Vite

Scaffold the project using Vite (`npm create vite@latest`).  
Do **not** use backend frameworks (for example, Node.js).

### Component structure

Create a well-structured application with at least **3 to 5 functional components**.

Examples:

- `Header`
- `Footer`
- `MainLayout`
- Domain-specific components such as `AthleteCard`, `CoachList`, etc.

Textual example:

```text
App (holds global routing)
  Header (static UI)
  MainLayout (wraps the main content)
	 AthleteDashboard (loads athletes data into useState)
		AthleteList (receives athlete array as props)
		  AthleteCard (receives a single athlete object as props and shows Edit/Delete buttons)
		AthleteForm (receives onAddAthlete / onUpdateAthlete functions as props)
  Footer (static UI)
```

### Mock data via JSON

Create a `data` folder inside `src/`.  
Create `.json` files containing mock arrays of objects that mimic the Athletics Sports Club domain (for example, `athletes.json`, `coaches.json`).

### Data integration

Import your JSON files directly into your components (for example, `import athletesData from './data/athletes.json'`).  
Do **not** use `fetch` in this assignment.

Use `useState` to store imported data so it is ready to be manipulated or rendered in your UI.

### React Router (optional, extra credit)

You may deliver this assignment as an SPA (Single Page Application).  
For extra points, use `react-router-dom` to create navigation between different views/pages (for example, switching from a Home dashboard to an Athletes list) instead of rendering everything on one screen.

---

## 3. Deliverables

You must submit the following:

1. **User stories**  
	One image/vector file per story, containing workflow + mock-up/wireframe details.  
	File naming pattern: `user-story-<name-or-description>.<extension>`

2. **Component hierarchy map**  
	One exported diagram image.  
	File naming pattern: `chm.<extension>`

3. **README.md**  
	A Markdown file with exact steps to:
	- Set up the project from scratch
	- Install dependencies
	- Run the app locally

	Include any additional context you want the teacher to consider while grading.

4. **Source code (ZIP)**  
	A ZIP archive containing your Vite project files.  
	Do **not** include the `node_modules` folder.

5. **Repository link (optional)**  
	A link to a public GitHub repository hosting your code.

---

## 4. Evaluation Criteria (100 points)

Your work will be graded using the following rubric:

| Criterion | Points |
|---|---:|
| User stories and mock-ups | 20 |
| Component Hierarchy Map | 10 |
| React setup and structure | 25 |
| Styling and UI fidelity | 15 |
| Mock data and state management | 10 |
| Execution and documentation | 10 |
| Navigation / Routing | 10 |
| **Total** | **100** |

