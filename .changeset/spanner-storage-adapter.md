---
'@mastra/spanner': major
---

Added a Google Cloud Spanner storage adapter (`@mastra/spanner`) targeting the GoogleSQL dialect. The adapter implements the `memory`, `workflows`, `scores`, `backgroundTasks`, `agents`, `mcpClients`, `mcpServers`, `skills`, `blobs`, `promptBlocks`, `scorerDefinitions`, and `schedules` storage domains and works with both managed Cloud Spanner instances and the local Spanner emulator. The `schedules` domain plugs into Mastra's built-in `WorkflowScheduler` for cron-driven workflow triggers.

```typescript
import { SpannerStore } from '@mastra/spanner';

const storage = new SpannerStore({
  id: 'spanner-storage',
  projectId: process.env.SPANNER_PROJECT_ID!,
  instanceId: process.env.SPANNER_INSTANCE_ID!,
  databaseId: process.env.SPANNER_DATABASE_ID!,
});
```
