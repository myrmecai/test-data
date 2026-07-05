# React UI Guidelines

## Components
- Use functional components with hooks only. No class components.
- Props interface named `{ComponentName}Props`.
- Export component as default, types as named exports.

## State
- Local UI state: `useState`.
- Server state: TanStack Query (`useQuery`, `useMutation`).
- Form state: React Hook Form with Zod validation.

## Styling
- Use Tailwind CSS utility classes. No inline styles.
- Consistent spacing scale: 4, 8, 12, 16, 24, 32.
- Never hardcode hex colors — use theme tokens.

## Accessibility
- Every interactive element must have an accessible name.
- Use `aria-label` for icon-only buttons.
- Forms: associate `<Label>` with `<Input>` via `htmlFor` / `id`.