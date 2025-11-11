## Workflow Diagram

```mermaid

graph LR
  A[Microsoft Outlook Trigger] --> B[Message a Model]
  B --> C{Is this job-related?}
  C -- Yes --> D[AI Agent]
  D --> E[Append Row in Google Sheets]
  C -- No --> X[Stop]

  %% Model reference (not linear in flow)
  D -. uses .-> M((Google Gemini Chat Model))
