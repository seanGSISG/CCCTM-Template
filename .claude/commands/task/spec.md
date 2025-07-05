# End-to-End Feature Implementation Guide

## Context

- When implementing new end-to-end features
- When planning feature development workflow
- When ensuring consistent architecture

## Requirements

- Follow the implementation steps in order
- Use the appropriate standards for each step
- Ensure consistency across all implementation layers
- Test each phase before moving to the next

## Implementation Steps

1. **Schema Definition** → Use rule @.cursor/rules/2101-schema-prisma.mdc

   - Define Prisma schema with standard fields
   - Add proper relations and indexes
   - Use correct field types and constraints
   - Follow naming conventions

2. **Router Implementation** → Use rule @.cursor/rules/2102-router.mdc

   - Create protected tRPC router
   - Add input validation with Zod
   - Implement cursor-based pagination
   - Handle security and responses

3. **React Query Integration** → Use rule @.cursor/rules/2103-trpc-react-query.mdc

   - Set up queries with queryOptions
   - Handle loading states
   - Implement optimistic updates
   - Manage cache invalidation

4. **CRUD Implementation** → Use rule @.cursor/rules/2105-crud.mdc

   - Follow phased implementation approach
   - Start with Create & Read operations
   - Add Update & Delete operations
   - Implement advanced features last

5. **Authentication** → Use rule @.cursor/rules/2106-auth.mdc
   - Use protectedProcedure for routes
   - Add session checks in components
   - Implement auth guards
   - Handle unauthorized states

## Examples

<example>
```typescript
// Implementation follows all steps in order
// 1. Schema defined in prisma/schema.prisma
// 2. Router implemented in src/server/api/routers/item.ts
// 3. React Query integration in src/components/ItemList.tsx
// 4. CRUD operations implemented in phases
// 5. Authentication checks in all appropriate places
```
Complete feature implementation following all steps in order
</example>

<example type="invalid">
```typescript
// Implementation skips steps or does them out of order
// Missing schema definition
// Incomplete router implementation
// Using old tRPC patterns instead of React Query
// Missing error handling
// Implementing all CRUD operations at once
// Missing authentication checks
```
Incomplete or out-of-order implementation missing critical steps
</example>
