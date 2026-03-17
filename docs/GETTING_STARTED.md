# Getting Started with n8n Workflows

Welcome! This guide helps you go from zero to running your first workflow in minutes.

## 1) Choose Your n8n Setup

### Option A: n8n Cloud (fastest)
1. Create a workspace at https://n8n.io.
2. Open your n8n dashboard.

### Option B: Self‑host with Docker (recommended for power users)
```bash
mkdir n8n-data
sudo docker run -it --rm \
  -p 5678:5678 \
  -v $PWD/n8n-data:/home/node/.n8n \
  n8nio/n8n
```
Open: http://localhost:5678

> Tip: For production, add HTTPS, environment variables, and a reverse proxy.

## 2) Import a Workflow
1. Open your n8n instance.
2. Go to **Workflows → Import from File**.
3. Choose a workflow JSON file from this repository.

## 3) Configure Credentials
Many workflows require credentials (API keys, OAuth, etc.).
1. Open **Credentials** in n8n.
2. Add the required credentials for the services used by the workflow.
3. Return to the workflow and map credentials on the nodes.

> Always keep secrets out of workflow JSON files. Use n8n’s credential manager.

## 4) Test and Activate
1. Click **Execute Workflow** to test.
2. Verify outputs and fix any missing credentials.
3. Toggle **Active** to run on a schedule or via webhooks.

## 5) Customize for Your Use Case
- Replace example endpoints with your real data sources.
- Update prompts, filters, and conditions.
- Add notifications (Slack, Email, etc.) to capture results.

## 6) Need Help?
Check the [Troubleshooting Guide](TROUBLESHOOTING.md) or open an issue with:
- Workflow name
- n8n version
- Error messages
- Steps to reproduce
