# cc-stream-cribl-internal-telemetry

Processes Cribl internal logs and native CriblMetrics events with reusable pipeline logic.

## Pipelines

- `cribl_internal` preserves the event and supplies `index=cribl_internal` and a fallback `sourcetype` based on the CriblLogs or CriblMetrics input.
- `cribl_metrics_to_splunk` stamps the configurable Splunk metrics index and preserves an existing `sourcetype`, defaulting to `cribl:metrics`.

The `splunk_metrics_index` Pack variable defaults to `host_metrics`.

## Integration

This pack contains processing logic. The consuming deployment routes input events into the pipelines and binds the destination.

## Development

Use `bun run lint`, `bun run typecheck`, and `bun run test` for checks. Use `make build` to produce the `.crbl` artifact.
