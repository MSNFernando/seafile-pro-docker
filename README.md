# SeaFile Pro + MinIO Deployment (Docker)

This repository contains a ready-to-deploy setup for **SeaFile Pro** using Docker Compose with **MinIO** as the S3-compatible storage backend.

---

## 🔧 Requirements

- Docker & Docker Compose
- A running MinIO server
- 3 buckets created on MinIO called
  - `seafile-commit`
  - `seafile-block`
  - `seafile-fs`
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
wget https://raw.githubusercontent.com/MSNFernando/seafile-pro-easy-install/refs/heads/main/install-seafile-v2.sh -o install-seafile.sh
chmod +x install-seafile.sh
./install-seafile.sh
```
Update the .env file with your relevant information. The easy install script will copy the seafile.env into .env which is required to run the docker
After updating the .env file
```bash
docker compose up -d
```
