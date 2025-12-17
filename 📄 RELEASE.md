# MGaut Ark System – Release Process

This document defines the governed, reproducible process for cutting and publishing releases of the MGaut Ark System.  
It applies to all covenant branches, with scope and deployment rules defined per covenant.

---

## 🌳 Covenant Release Rules

- **Public Covenant (`main`)**  
  - Tagged with standard Semantic Versioning: `vMAJOR.MINOR.PATCH`  
  - Example: `v1.2.0`  
  - Changelog: Updated in `CHANGELOG.md`  
  - Deployment: Auto‑deploy to GitHub Pages  

- **Enterprise Covenant (`enterprise`)**  
  - Tagged with suffix: `-ent`  
  - Example: `v1.2.0-ent`  
  - Changelog: Maintained privately under enterprise license  
  - Deployment: Auto‑deploy to private host (Netlify/Vercel)  

- **Sovereign Covenant (`sovereign`)**  
  - Tagged with suffix: `-sov`  
  - Example: `v1.2.0-sov`  
  - Changelog: Sealed, private, never published  
  - Deployment: Build only, no public release  

---

## 🚀 Release Checklist

1. **Prepare Branch**  
   - Ensure branch is clean and all tests pass.  
   - Confirm accessibility checks (visual, auditory, language‑based learning support).  
   - Verify audit‑grade commit history.  

2. **Update Documentation**  
   - Update `CHANGELOG.md` (public covenant only).  
   - Confirm `ROADMAP.md` reflects current direction.  
   - Verify `VERSIONING.md` alignment.  

3. **Tag Release**  
   - Public: `git tag vX.Y.Z`  
   - Enterprise: `git tag vX.Y.Z-ent`  
   - Sovereign: `git tag vX.Y.Z-sov`  
   - Push tags: `git push origin --tags`  

4. **Trigger Deployment**  
   - Public: GitHub Actions deploys to GitHub Pages.  
   - Enterprise: GitHub Actions deploys to private host.  
   - Sovereign: Build completes locally or in CI, no deployment.  

5. **Verify Deployment**  
   - Confirm public URL is live for `main`.  
   - Confirm enterprise host is updated for `enterprise`.  
   - Confirm sovereign build artifacts are sealed.  

---

## 📜 Operator Notes

- Each release is a governed milestone.  
- Public covenant releases are transparent but limited.  
- Enterprise and sovereign releases remain sealed under their respective governance.  
- This process is reproducible, auditable, and aligned with the covenant model.  
