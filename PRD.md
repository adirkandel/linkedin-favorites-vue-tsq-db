PRD: LinkedIn Favorites Manager (v1.1)

## 1. Overview

Users need a simple, private way to curate a list of interesting LinkedIn profiles. Instead of relying on browser bookmarks, which are static and unorganized, this application will provide a dedicated space to save, view, and manage these profiles with rich data and flexible display options.

## 2. Target Audience

This tool is for any individual who uses LinkedIn for networking, recruiting, research, or personal reference and wants a more structured way to manage profiles of interest.

## 3. User Stories

- As a user, I want to add a new profile to my list by simply pasting its LinkedIn URL.
- As a user, I want the application to pre-fill basic information from the profile so I don't have to type it all manually.
- As a user, I want to see all my saved profiles in a visually appealing "Card View," showing the person's photo, name, and title.
- As a user, I want to switch to a compact "Table View" to see more profiles at once and compare them easily.
- As a user, I want to edit the information for a saved profile to add my own notes or correct details.
- As a user, I want to delete a profile I'm no longer interested in.
- As a user, I want to drag and drop profiles in either view to change their order and prioritize them.

## 4. Core Features & Requirements

| Feature ID | Feature Name             | Description                                                                                                                                                                     | Priority  |
| ---------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| F-01       | Profile Ingestion        | A primary input field where a user can paste a LinkedIn profile URL.                                                                                                            | Must-have |
| F-02       | Data Population          | Upon pasting a URL, a modal will open with fields like Name, Headline, Company, Profile Photo URL, and LinkedIn URL (pre-filled). The user will manually fill in these details. | Must-have |
| F-03       | Data Storage             | All profile data will be managed in the application's local state. To ensure data persists between sessions, it will be saved to the browser's `localStorage`.                  | Must-have |
| F-04       | Card View                | The default view. Each profile is a card displaying the profile picture, name, headline, and action buttons (Edit, Delete).                                                     | Must-have |
| F-05       | Table View               | An alternative view. Displays profiles in a sortable table with columns for Name, Headline, Company, etc. Also includes action buttons.                                         | Must-have |
| F-06       | View Toggle              | A clear UI control (e.g., a button or switch) to toggle between Card View and Table View.                                                                                       | Must-have |
| F-07       | Edit Profile             | An "Edit" button on each profile opens a modal (similar to F-02) allowing the user to update any saved information.                                                             | Must-have |
| F-08       | Delete Profile           | A "Delete" button on each profile. A confirmation step ("Are you sure?") will be required to prevent accidental deletion.                                                       | Must-have |
| F-09       | Drag-and-Drop Reordering | In both Card and Table views, the user can click and drag a profile to a new position in the list. The new order will be saved automatically.                                   | Must-have |

## 5. Proposed Technical Stack (Revised)

- Framework: Vue 3 + Vite
- Language: TypeScript
- UI Components: shadcn-vue. I will use its CLI to add necessary components like Button, Input, Card, Table, and Dialog (for modals).
- Styling: Tailwind CSS (a dependency of shadcn-vue).
- Local Persistence: Browser localStorage API.
- Drag-and-Drop: A library like Vue.Draggable.
- Backend & Database: Removed for this version. The application will be a standalone frontend app.

---
