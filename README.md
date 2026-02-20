# 🔄 n8n Workflows Backup

<div align="center">

![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

Automated backups of workflows from the **[kkulebaev-n8n.ru](https://kkulebaev-n8n.ru)** platform

*Backups run daily at 10:00 (Moscow Time)*

</div>

---

## 📁 Repository Structure

```
n8n/
├── 📂 workflows/          # JSON export of all workflows
├── 📂 credentials/        # Credential metadata (no secrets)
└── 📂 backups/            # Full workspace backups
```

---

## 🔐 Credentials

Only **metadata** is stored in this repository (name, type, workflow bindings). Secrets and tokens are never exported or stored here.

---

## 🚀 How to Restore a Workflow

1. Open [kkulebaev-n8n.ru](https://kkulebaev-n8n.ru)
2. Go to the **Workflows** section
3. Click **Import** → **From file**
4. Select the desired `.json` file from the `workflows/` folder
5. Configure credentials in the imported workflow

---

## 🔄 How Auto-Backup Works

The **Backup workspaces for n8n** workflow runs every day at **10:00 (Moscow Time)** and:

1. Connects to the n8n API at [kkulebaev-n8n.ru](https://kkulebaev-n8n.ru)
2. Exports all workflows and credentials
3. Pushes the files to this repository via the GitHub API
4. A commit is created automatically with a date timestamp

```
⏰ 10:00 → n8n API → Export → GitHub Commit ✅
```

---

## 🔗 Links

- 🌐 **n8n Platform:** [kkulebaev-n8n.ru](https://kkulebaev-n8n.ru)
- 📖 **n8n Documentation:** [docs.n8n.io](https://docs.n8n.io)

---

<div align="center">
  <sub>🤖 Backups are created automatically via n8n</sub>
</div>








