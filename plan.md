```markdown
# Detailed Implementation Plan for Shipping Company Website

This plan outlines the creation of a modern, responsive shipping company website using the existing Next.js project with Tailwind CSS. All new files will follow best practices including error handling, accessibility, and responsive design.

---

## 1. Create Global Layout

### File: src/app/layout.tsx
- **Purpose:** Wrap all pages with a consistent header and footer.
- **Steps:**
  - Create the file `src/app/layout.tsx`.
  - Import the Header and Footer components from `src/components/Header.tsx` and `src/components/Footer.tsx`.
  - Wrap the `{children}` with `<Header />` at the top and `<Footer />` at the bottom.
  - Ensure the layout uses responsive containers with Tailwind CSS classes.

---

## 2. Build Header Navigation Component

### File: src/components/Header.tsx
- **Purpose:** Provide a navigation bar with links to main pages.
- **Steps:**
  - Create the file `src/components/Header.tsx`.
  - Implement a functional component that returns a `<header>` element with a `<nav>` inside.
  - Include navigation links for "Home", "Services", "Tracking", and "Contact".
  - Use semantic HTML and Tailwind CSS for styling (e.g., `flex`, `justify-between`, `py-4`, `text-lg`).
  - Ensure accessibility by using proper ARIA roles and keyboard navigation.

---

## 3. Build Footer Component

### File: src/components/Footer.tsx
- **Purpose:** Provide footer information and contact details.
- **Steps:**
  - Create the file `src/components/Footer.tsx`.
  - Implement a functional component that returns a `<footer>` element with company info, copyright, and contact details.
  - Style using Tailwind CSS ensuring proper padding and font styling.

---

## 4. Create Homepage with Hero Section

### File: src/app/page.tsx
- **Purpose:** Serve as the landing page with a hero section and call-to-action.
- **Steps:**
  - Create the file `src/app/page.tsx`.
  - Design a hero section with a prominent headline (e.g., “Leading Shipping Solutions”) and a descriptive subtext.
  - Add two call-to-action buttons: one linking to the Tracking page (`/tracking`) and one linking to the Contact page (`/contact`). Use Tailwind CSS for modern typography and spacing.
  - Ensure the page is responsive with ample whitespace and clear visual hierarchy.

---

## 5. Develop Services Page

### File: src/app/services/page.tsx
- **Purpose:** Detail the shipping services offered.
- **Steps:**
  - Create the file `src/app/services/page.tsx`.
  - Layout a grid or card-based list of services (e.g., International Shipping, Freight Forwarding, Customs Clearance).
  - For each service, provide a heading, brief description, and use a clean list/bullet design. Avoid using external icons or image services.
  - Ensure that the UI is clean and uses adequate typography and spacing.

---

## 6. Implement Shipment Tracking Page

### File: src/app/tracking/page.tsx
- **Purpose:** Allow users to track shipments.
- **Steps:**
  - Create the file `src/app/tracking/page.tsx`.
  - Add `"use client"` at the top to enable interactivity.
  - Import and embed the `TrackingForm` component (to be created) that handles user input.
  - Ensure error handling for empty or invalid tracking numbers and display proper error messages.

### File: src/components/TrackingForm.tsx
- **Purpose:** Handle the tracking number input and simulate a lookup.
- **Steps:**
  - Create the file `src/components/TrackingForm.tsx` and add `"use client"` at the top.
  - Use `react-hook-form` for form state management.
  - Create an input field for the tracking number and a submit button.
  - Implement a simulated API call (using `setTimeout`) to validate the tracking number.
  - Provide UI feedback: show errors if the field is empty or invalid, and display a success message or "not found" response.
  - Use Tailwind CSS for styling, ensuring clear error messages and responsive UX.

---

## 7. Develop Contact Page with Form

### File: src/app/contact/page.tsx
- **Purpose:** Allow users to contact the shipping company.
- **Steps:**
  - Create the file `src/app/contact/page.tsx` and add `"use client"` at the top.
  - Implement a contact form with fields: Name, Email, Phone, and Message.
  - Use `react-hook-form` for robust form handling and validation.
  - Validate input fields with proper error messages (e.g., required field warnings and proper email format).
  - On form submission, simulate an API call (or use a dummy endpoint) to send form data and display a success or error message.
  - Incorporate Tailwind CSS classes to ensure the form is modern, clean, and responsive.

---

## Additional Integration & Best Practices

- **Error Handling:**  
  Ensure each form includes client-side validation and error messages. For simulated API calls, use try/catch blocks to catch exceptions and display user-friendly error notifications.

- **Styling & Responsiveness:**  
  Leverage Tailwind CSS for all UI elements, ensuring mobile responsiveness with Flexbox and Grid layouts. Maintain a modern visual design with ample whitespace, consistent typography, and a clear color palette defined in `globals.css`.

- **Code Quality:**  
  Use proper TypeScript types, functional React components, and React hooks where necessary. Maintain separation of concerns by keeping layout, form handling, and UI components in separate files.

---

## Summary

- Created a global layout (`src/app/layout.tsx`) to wrap pages with a header and footer.
- Developed Header (`src/components/Header.tsx`) and Footer (`src/components/Footer.tsx`) components with semantic, responsive design.
- Designed key pages: Homepage (`src/app/page.tsx`), Services (`src/app/services/page.tsx`), Tracking (`src/app/tracking/page.tsx` with `TrackingForm.tsx`), and Contact (`src/app/contact/page.tsx`).
- Integrated client-side forms using `react-hook-form` with proper validation and error handling.
- Emphasized modern UI/UX with clear typography, spacing, and responsive layouts using Tailwind CSS.
