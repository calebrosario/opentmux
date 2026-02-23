# Approach 1: MVP Implementation Plan

## Phase 1: Foundation (Week 1)
1. **Identify Core Use Cases:** Select the top 3-5 user intents.
2. **Curate Golden Dataset:** Manually write 50-100 pairs of (Question, Ground Truth Answer).
3. **Setup Environment:** Install `ragas` or `deepeval` in the development environment.

## Phase 2: Automation (Week 2)
1. **Integrate Metrics:** Implement scripts to calculate:
    - Faithfulness
    - Answer Relevance
    - Context Precision
2. **Baseline Run:** Execute the evaluation against the current production model.
3. **Manual Calibration:** Review 10 results to ensure automated scores match human judgment.

## Phase 3: Operationalization (Ongoing)
1. **Weekly Eval Cadence:** Schedule a recurring task to run the evaluation suite every Friday.
2. **Tracking:** Log results in a shared spreadsheet to monitor performance over time.
3. **Feedback Loop:** Use low-scoring examples to improve prompts or retrieval logic.

## Tools Required
- Python
- RAGAS / DeepEval
- Google Sheets / Excel
