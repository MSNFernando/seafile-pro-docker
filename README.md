# SeaFile Pro + MinIO Deployment (Docker)

This repository contains a ready-to-deploy setup for **SeaFile Pro** using Docker Compose with **MinIO** as the S3-compatible storage backend.

---

## 🔧 Requirements

- Docker & Docker Compose
- A running MinIO server
- A bucket called `seafile-data` created on MinIO
- Valid SeaFile Pro license (upload via web UI after setup)

---

## ⚙️ Configuration

Edit the following files to match your environment:

### `seafile.env`
- Set `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` for MinIO
- Point `S3_ENDPOINT` to your MinIO API address
- Change `SEAFILE_SERVER_HOSTNAME`, email, password, etc.

---

## 🚀 Deployment

```bash
git clone https://github.com/MSNFernando/seafile-pro-docker.git
cd seafile-pro-docker

# Optional: edit seafile.env

docker compose up -d
