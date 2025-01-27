# Silent Navigation Failure in Next.js 15 Non-Page Components

This repository demonstrates an uncommon bug in Next.js 15 related to client-side navigation (`next/navigation`) within components that are not directly rendered by a `Page` component.  The navigation functions appear to fail silently without providing helpful error messages.

## Bug Description

When using the `useRouter` hook and navigation functions (like `router.push`) inside a component that's not part of the main page's render tree (e.g., a modal, dialog, or a component rendered conditionally), the navigation might not work as expected. This can lead to unexpected behavior or silent failures.

## Solution

The solution involves ensuring that the navigation happens within the context of a component that's part of the main page component hierarchy. This often requires rethinking the component structure or using a different approach to trigger navigation.