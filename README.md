HR Workflow Designer (React + React Flow)

This project is a compact HR Workflow Builder that lets HR teams visually design and test processes like onboarding, approvals, and automated actions.
I built it as part of a 4–6 hour assignment, so the focus was on clean architecture, solid functionality, and future scalability—not on perfect UI polish.

🌟 What the App Can Do
🎨 Visual Workflow Canvas

Drag-and-drop nodes from the sidebar

Connect and arrange them to build end-to-end workflows

Supports five node types:

Start

Task

Approval

Automated Step

End

📝 Configurable Node Editor

Selecting any node opens a form where you can configure that step.
Each type exposes the fields that actually matter:

Start Node: title, metadata

Task Node: title, description, assignee, due date

Approval Node: approver role, auto-approve threshold

Automated Node: action picker + dynamic input fields

End Node: summary toggle, final message

⚙️ Workflow Simulation

You can test your workflow flow by:

Running validations

Serializing the entire graph to JSON

Sending it to a mock /simulate endpoint

Viewing a simple step-by-step execution log

This helps visualize how a workflow would behave in a real HR system.

🧩 Architecture at a Glance

The project is split into clean, modular sections:

src/
  api/              # Mock API for automations + simulation
  components/
    canvas/         # React Flow canvas + node components
    forms/          # Node configuration forms
    layout/         # Main layout + sidebar
    panels/         # Node config + simulation panels
  hooks/            # Zustand workflow store
  types/            # Node types + workflow interfaces
  utils/            # Validation + serialization helpers
  App.tsx
  main.tsx


React Flow handles graph rendering and interactions

Zustand keeps workflow state centralized and predictable

Node logic stays separate from UI for long-term maintainability

🔌 Mock API Layer
GET /automations

Returns available automated actions (like "Send Email" or "Generate Document") along with their parameters.

POST /simulate

Takes the serialized workflow and returns a mock execution trace.

This keeps the project lightweight while still showing realistic data flow.

🚀 Running the Project

Install dependencies:

npm install


Start the dev server:

npm run dev


Open the app:

http://localhost:5173


You'll see the canvas, sidebar, configuration panel, and simulation panel ready to use.

✔ What’s Done (Within the Time Limit)

Drag-and-drop workflow builder

Custom React Flow nodes

Full configuration forms

Dynamic automated-step parameters

Zustand-based global state

Workflow validation + simulation

Clean serialization to JSON

Cycle detection, orphan detection, start/end validation

Modular and extendable project structure

Everything required for the assignment is implemented.

➕ What I’d Add With More Time

Undo/Redo

Workflow import/export (JSON)

Auto-layout for cleaner graphs

Error indicators directly on nodes

A small library of templates

Persistence + versioning on a backend

More polished UI/UX and interactions

💡 Final Thoughts

This project was intentionally built to show strong fundamentals:

Comfort with React Flow

Clean state and component architecture

Practical understanding of workflow design

Ability to ship a meaningful feature set under tight time constraints

If you're reviewing this project, thanks for taking a look!
