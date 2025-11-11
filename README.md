# Job Applications Tracker (n8n)

Automatically logs job application emails into Google Sheets using AI parsing.

## Workflow Diagram

```mermaid
graph LR
  A[Microsoft Outlook Trigger] --> B[Message a model]
  B --> C{If job-related?}
  C -- yes --> D[AI Agent]
  D --> E[Append row in Google Sheets]
  D -. uses .-> M((Google Gemini Chat Model))
  C -- no --> X[Stop]
