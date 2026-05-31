# SvelteKit Cursor Rules

## Project Structure
- SvelteKit conventions: src/routes/, src/lib/, src/components/
- +page.svelte, +page.ts, +page.server.ts pattern
- $lib alias for src/lib
- Static assets in static/

## Component Patterns
- .svelte files with <script>, <style>, and template
- Use runes ($state, $derived, $effect) in Svelte 5
- Props via let keyword or $props()
- Slots for composition
- Use {#each}, {#if}, {#await} blocks

## Data Loading
- +page.server.ts for server-side data loading
- +page.ts for client-side data loading
- Use form actions for mutations
- Load function return typed data
- parent() for layout data access

## Styling
- Scoped styles by default (no :global unless necessary)
- Tailwind via @svelte-add/tailwindcss
- CSS variables for theming
- Transition and animation directives

## State
- Svelte stores for global state
- URL state via page.url.searchParams
- Form state with form action responses
- Cookies for server-side state
