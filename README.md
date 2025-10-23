# shift-left-arch-qa
&gt; OCI-hosted, open-source LLM pipeline that automatically reviews Pull-Requests for **architectural violations** – modularity breaches, cyclic dependencies, pattern drift – **before** code reaches main.

---

## 🚀 5-Min Quick Start (OCI Always-Free ARM VM, Ubuntu 22.04)
```bash
# 1. Provision VM (4 GB RAM) and open ports 22, 5678, 8000
# 2. Clone & fire-up
git clone https://github.com/asferrasool/shift-left-arch-qa.git
cd shift-left-arch-qa
docker compose up -d
# 3. Import workflow
open http://&lt;VM-IP&gt;:5678  → Settings → Import → choose n8n/workflows/arch-qa.json
# 4. Add GitHub webhook
Repo → Settings → Webhooks → http://&lt;VM-IP&gt;:5678/webhook/github/arch-qa
