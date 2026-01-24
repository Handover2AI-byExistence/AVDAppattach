# AVD App Attach Automation

![PSScriptAnalyzer](https://github.com/Handover2AI/AVDAppattach/actions/workflows/ci-workflow-psscriptanalyzer.yml/badge.svg)

This repository provides PowerShell scripts to **export, create, and manage Azure Virtual Desktop (AVD) App Attach apps** at scale. It is organized into three main folders:

---

## 📂 Repository Structure

- **CreateMultipleApps/**
  - `Create-MultipleAppAttach.ps1` – Bulk creation and assignment of App Attach apps from a CSV file.
  - `AppAttachApps_Complete.csv` – Example CSV schema used by the script.
  - `readme.md` – Detailed documentation for bulk creation.

- **CreateSingleApps/**
  - `Create-SingleAppAttach.ps1` – Create and assign a single App Attach app.
  - `readme.md` – Detailed documentation for single app creation.

- **GetAllApps/**
  - `Get-AllAppAttachStep1.ps1` – Fast export of existing App Attach apps (IDs only).
  - `Get-AllAppAttachStep2.ps1` – Enrichment step to resolve user group names via Graph.
  - `readme.md` – Documentation for the two‑step export workflow.

- **LICENSE** – License information for this repository.

---

## 🚀 How to Use

1. **Export existing apps**  
   Run scripts in `GetAllApps/` to generate a CSV of current App Attach apps.

2. **Edit CSV**  
   Fill in required fields (`hostpool_packagepull`, `resourcegroup_hostpool_packagepull`) before import.

3. **Create apps**  
   - Use `CreateSingleApps/` for one app at a time.  
   - Use `CreateMultipleApps/` for bulk creation from the CSV.

4. **Manage apps**  
   Scripts include optional sections to unassign host pools, unassign user groups, or remove apps entirely.

---

## 🤝 Contributing

Contributions are welcome!  
- Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.  
- Follow the [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) when interacting in issues and pull requests.

---

## ✍️ Author

Created and maintained by **Handover2AI-byExistence**.  
If you find this useful, feel free to star ⭐ the repo or open issues for improvements.

---
