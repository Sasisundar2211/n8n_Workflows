# Troubleshooting

Common issues and quick fixes when importing or running workflows.

## Import Errors
**Symptoms:** “Invalid JSON”, “Unsupported workflow version”.
- Re‑download the file and import again.
- Open the workflow JSON to confirm it is not truncated.
- If your n8n is older, upgrade to the latest version.

## Missing Credentials
**Symptoms:** Nodes show red errors or “Credentials not found”.
- Add the required credentials in **Credentials**.
- Re‑open the workflow and select the right credential on each node.

## Nodes Not Found
**Symptoms:** “Node type not found”.
- Update n8n to the latest version.
- Check if the node belongs to a community package and install it.

## Webhook Doesn’t Trigger
- Confirm the workflow is **Active**.
- Copy the **Production** webhook URL (not test).
- If self‑hosted, ensure your instance is publicly reachable.

## API Rate Limits
- Add **Wait/Delay** nodes.
- Use batch sizes or pagination.
- Retry with exponential backoff.

## Data Looks Wrong
- Inspect each node’s output using **Execution data**.
- Add **Set** nodes to normalize fields.
- Log outputs to a Google Sheet or database for debugging.

## Still Stuck?
Open a GitHub issue with:
- Workflow name + file path
- n8n version
- Error message or screenshot
- Steps to reproduce
