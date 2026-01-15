# Senior React.js Coding Test - Artificially

Welcome to the frontend stage of our recruitment process at **Artificially**. This test evaluates your proficiency in React.js architecture, state management, API integration, and **UI/UX design quality**.

Our website: [artificially.io](https://artificially.io)

---

## Objective

Build a **File Management Dashboard** that interacts with a backend API. This application should allow users to upload, view, download, and delete files through a polished, professional interface.

---

## Requirements

### 1. Core Features

#### File Listing
- Display files in a well-designed table or card layout
- Show for each file:
  - Name
  - File type icon
  - Size (human readable)
  - Upload date (formatted)
  - Processing status (with visual indicator)
  - Action buttons (download, delete)
- Implement sorting and filtering options
- Handle empty states gracefully

#### File Upload
- Drag-and-drop upload zone + click to browse
- File type and size validation before upload
- Upload progress indicator
- Support multiple file uploads

#### File Actions
- **Download**: Trigger download with loading state
- **Delete**: Confirmation dialog before deletion
- Visual feedback for all actions (loading, success, error)

---

### 2. Technical Requirements

#### State Management
- Use React Query for server state management
- Optimistic updates for delete actions
- Proper cache invalidation after mutations

#### API Integration
- Centralized API configuration
- Axios interceptors for auth headers (`Authorization: Bearer artificially-token`)
- Proper error handling and retry logic

#### TypeScript
- Full TypeScript implementation
- Proper interfaces for API responses and component props

---

### 3. UI/UX Requirements (Critical)

**This is not a simple UI task.** Your design choices will be heavily evaluated.

#### Material UI Implementation
- Use Material UI (MUI) v5 as the component library
- Customize the default theme (do not use default MUI styling)
- Create a cohesive design system with:
  - Custom color palette
  - Typography scale
  - Consistent spacing
  - Border radius tokens
  - Shadow definitions

#### Design Quality Checklist

| Aspect | Expectation |
|--------|-------------|
| **Color Palette** | Thoughtful primary/secondary colors, proper contrast ratios, consistent use of grays |
| **Typography** | Clear hierarchy, appropriate font weights, readable line heights |
| **Spacing** | Consistent padding/margins, proper component breathing room |
| **Borders & Shadows** | Subtle, consistent use to create depth and separation |
| **Icons** | Consistent icon set, appropriate sizing |
| **Micro-interactions** | Hover states, transitions, loading states |
| **Responsiveness** | Fully functional on mobile, tablet, and desktop |
| **Empty & Error States** | Well-designed fallback UI for all edge cases |

#### Layout Requirements
- Responsive sidebar or header navigation
- Proper content max-width on large screens
- Mobile-first approach

---

### 4. Project Structure
```
src/
├── api/
│   ├── client.ts
│   └── files.ts
├── components/
│   ├── common/
│   │   ├── Button/
│   │   ├── Dialog/
│   │   └── DropZone/
│   └── files/
│       ├── FileList/
│       ├── FileCard/
│       ├── FileUpload/
│       └── FileActions/
├── hooks/
│   └── useFiles.ts
├── theme/
│   ├── palette.ts
│   ├── typography.ts
│   └── index.ts
├── types/
│   └── file.ts
├── pages/
│   └── Dashboard.tsx
└── App.tsx
```

---

### 5. Bonus Points

- Dark mode toggle with persisted preference
- File preview modal (images, PDFs)
- Keyboard shortcuts (e.g., `Del` to delete selected)
- Skeleton loaders during data fetching
- Toast notifications for actions

---

## Setup Instructions
```bash
git clone git@github.com:ArtificiallyLTD/React-Coding-Test.git
cd React-Coding-Test

npm install
npm start
```

### API Configuration

Update `src/api/client.ts`:
```typescript
export const API_BASE_URL = "http://your-backend-api-url";
```

---

## Submission

1. Push to a **private** GitHub repository
2. Invite `contact@artificially.io` as collaborator
3. Include README with:
   - Setup instructions
   - Design decisions explanation
   - Screenshots of your implementation

---

## Evaluation Criteria

| Criteria | Weight |
|----------|--------|
| **UI/UX Design Quality** | 30% |
| Code architecture & organization | 25% |
| Functionality & completeness | 20% |
| TypeScript & type safety | 15% |
| Error handling & edge cases | 10% |

---

## Important Notes

**Design matters.** A functional but poorly designed submission will score lower than a polished, thoughtful implementation.

We are evaluating:
- Your eye for design details
- Ability to create professional, production-ready interfaces
- Understanding of modern UI/UX patterns

---

## Time Expectation

This task is designed for **3-4 hours**. Focus on quality over quantity - a well-designed subset of features beats a complete but ugly implementation.

Good luck!
