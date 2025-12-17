# MGaut Ark System – Versioning Policy

The MGaut Ark System follows **Semantic Versioning (SemVer)** for the **public covenant** (`main` branch).  
Enterprise and sovereign covenants extend this scheme with suffixes to ensure clarity and separation.

---

## 🌳 Covenant Versioning

- **Public Covenant (`main`)**  
  - Uses standard Semantic Versioning: `MAJOR.MINOR.PATCH`  
  - Example: `v1.2.0`  
  - Public releases are tagged and documented in `CHANGELOG.md`.  

- **Enterprise Covenant (`enterprise`)**  
  - Inherits from the public covenant version.  
  - Tagged with `-ent` suffix to indicate enterprise build.  
  - Example: `v1.2.0-ent`  
  - Enterprise changelog is sealed and maintained privately.  

- **Sovereign Covenant (`sovereign`)**  
  - Inherits from the enterprise covenant version.  
  - Tagged with `-sov` suffix to indicate sovereign build.  
  - Example: `v1.2.0-sov`  
  - Sovereign changelog is sealed, private, and never published.  

---

## 🔐 Versioning Principles

1. **MAJOR** → Incremented for covenant‑level changes that break compatibility.  
2. **MINOR** → Incremented for new features that are backward compatible.  
3. **PATCH** → Incremented for backward‑compatible bug fixes or refinements.  
4. **Suffixes** → `-ent` and `-sov` suffixes ensure enterprise and sovereign builds are never confused with public releases.  

---

## 🚀 Release Process

1. Develop features in feature branches.  
2. Merge into the appropriate covenant branch (`main`, `enterprise`, or `sovereign`).  
3. Tag the release according to the covenant versioning scheme.  
4. Update the appropriate changelog (`CHANGELOG.md` for public covenant only).  
5. Deploy according to covenant rules:  
   - `main` → GitHub Pages (public)  
   - `enterprise` → Private host (Netlify/Vercel)  
   - `sovereign` → Build only, no deployment  

---

## 📬 Contact

For enterprise licensing or release inquiries:  
**Maximum Input, LLC**  
[Insert your preferred contact email or website here]

---

## ⚡ Operator Notes

This `VERSIONING.md` is itself a governed artifact.  
It ensures that every release of the MGaut Ark System is sealed, auditable, and covenant‑aligned.  
