# MVP Evaluation Workflow State Machine

```mermaid
state_machine
    [*] --> DatasetCreation
    DatasetCreation --> RunInference : 50-100 Test Cases
    RunInference --> AutomatedMetrics : RAGAS / DeepEval
    AutomatedMetrics --> ManualReview : Spot check (10-20%)
    ManualReview --> ReportGeneration : Weekly Summary
    ReportGeneration --> [*]
    
    ManualReview --> DatasetCreation : Identify Gaps
```

## Description
The MVP workflow is a linear, weekly process designed for simplicity. It starts with a small "Golden Dataset," runs inference, applies basic automated metrics, and concludes with a brief manual review to ensure the metrics align with human intuition.
