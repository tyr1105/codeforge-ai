# Vue 3 + Nuxt Cursor Rules

## Project Structure
- Nuxt 3 directory convention (pages/, components/, composables/, server/)
- Auto-imports enabled (no need to import ref, computed, etc.)
- Components auto-registered from components/ directory
- Use TypeScript with strict mode

## Component Patterns
- <script setup lang="ts"> syntax only
- Define props with defineProps<T>()
- Emit events with defineEmits<T>()
- Use composables for reusable logic (use* naming)
- Template refs: use ref() with template ref attribute

## Styling
- Scoped styles by default
- Tailwind CSS via @nuxtjs/tailwind
- Use <style scoped> for component-specific overrides
- CSS modules for complex components

## Data Fetching
- useFetch() for GET requests (auto-cached)
- useLazyFetch() for non-blocking fetches
- $fetch() for server-side or non-reactive fetches
- Server routes in server/api/
- Use nitro event handler patterns

## State
- useState() for cross-component state
- Pinia via @pinia/nuxt for complex state
- useCookie() for cookie-based state

## Testing
- Vitest with @vue/test-utils
- Nuxt test utils for integration
- Test composables independently
