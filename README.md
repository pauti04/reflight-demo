# Reflight — hosted demo

**▶ https://pauti04.github.io/reflight-demo/**

This repo is the deployed static build of the [Reflight](https://github.com/pauti04/reflight)
timeline UI with pre-recorded agent runs baked in — a flaky-agent fleet with
auto-labeled failures (loops, wrong tool args, cascades), governor kills, run
diffs, and the cost dashboard. Read-only, zero backend.

Things to try:
- click **flaky-01** → the loop findings banner and the timeline
- pick **flaky-00** + **flaky-02** on the runs list → **diff** → the first
  divergence, highlighted (`"query"` vs `"q"`)
- **runaway-budget** → a $0.50 budget kill recorded in the run
- **costs** → the anomaly flagged at 173× the task median

Built from the main repo with `reflight export-static` +
`STATIC_EXPORT=1 NEXT_PUBLIC_STATIC_DEMO=1 npm run build`.
