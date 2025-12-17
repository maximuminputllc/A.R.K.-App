# MGaut Ark System – Workflow Governance

This document defines the governance of GitHub Actions workflows used in the MGaut Ark System.  
Workflows are treated as governed, sealed artifacts, subject to the same covenant model as source code and documentation.

---

## 🌳 Covenant Workflow Rules

- **Public Covenant (`main`)**  
  - Workflows: `deploy-main.yml`  
  - Purpose: Auto‑deploy to GitHub Pages.  
  - Governance: Transparent, auditable, and visible to all.  
  - Secrets: None required beyond GitHub’s default token.  

- **Enterprise Covenant (`enterprise`)**  
  - Workflows: `deploy-enterprise.yml`  
  - Purpose: Auto‑deploy to private host (Netlify/Vercel).  
  - Governance: Sealed under commercial license.  
  - Secrets: Managed via GitHub Secrets (`NETLIFY_AUTH_TOKEN`, `NETLIFY_SITE_ID`, or Vercel equivalents).  
  - Visibility: Workflow file is visible, but secrets remain encrypted and inaccessible.  

- **Sovereign Covenant (`sovereign`)**  
  - Workflows: `build-sovereign.yml`  
  - Purpose: Build only, no deployment.  
  - Governance: Fully private, sealed, and unshared.  
  - Secrets: None.  
  - Visibility: Workflow file is visible, but execution is private to the operator.  

---

## 🔐 Workflow Governance Principles

1. **Sealed Artifacts**  
   - Each workflow is bound to its covenant branch.  
   - No workflow may deploy outside its covenant scope.  

2. **Audit Discipline**  
   - Workflow changes must be semantic, documented, and reviewed by the maintainer.  
   - Commit history for workflows is subject to the same audit standards as code.  

3. **Secrets Management**  
   - All secrets are stored in GitHub Secrets.  
   - Secrets are never committed to the repository.  
   - Secrets are rotated periodically and governed under enterprise agreements.  

4. **Operator Empowerment**  
   - Workflows must provide clear logs for reproducibility.  
   - Failures must surface actionable alerts.  
   - Automation must never bypass governance.  

---

## 🚫 Boundaries

- No external contributors may modify workflows.  
- Enterprise workflows cannot be executed without valid secrets.  
- Sovereign workflows are not open to external execution or review.  

---

## 📬 Governance Contact

For enterprise workflow governance inquiries:  
**Maximum Input, LLC**  
[Insert your preferred contact email or website here]

---

## ⚡ Operator Notes

This `WORKFLOW-GOVERNANCE.md` is itself a governed artifact.  
It ensures that automation is sealed, auditable, and covenant‑aligned.  
