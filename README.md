# PROJECT FENRIR v0.1.0
![PROJECT FENRIR](fenrir-banner.png)
A defensive, local-first cybersecurity monitoring prototype for Kali Linux on WSL2.
This starter release provides a FastAPI dashboard, event journal, local health checks,
and a Rust hashing/indicator engine. It does **not** propagate, exploit, or modify
remote systems.

## Requirements
- Kali Linux on WSL2
- Python 3.11+
- Rust stable + Cargo (for the optional Rust core)

## Quick start
```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip cargo rustc
git clone https://github.com/SentraSecurity/FENRIR.git
cd FENRIR
unzip project_fenrir_v0_1.zip
cd project_fenrir_v0_1
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn fenrir.app:app --host 127.0.0.1 --port 8080
```
Open `http://127.0.0.1:8080` in the Windows browser.

## Rust core
```bash
cd rust_core
cargo build --release
cargo run --release -- hash ../README.md
```
The Rust component computes SHA-256 and checks a local text indicator list.
It does not execute samples.

## Configuration
Copy `.env.example` to `.env`. The default bind address is localhost only.
Do not expose the dashboard to the public internet.

## Current scope
- Dashboard status and event journal
- Local machine/interface inventory
- File hashing (read-only)
- Local indicator matching (SHA-256)
- Manual event recording

## Not yet implemented
- Packet capture, active network scanning, quarantine, sandbox execution,
  autonomous remediation, remote scanning, or self-updating behavior.
These require explicit scope controls, audit logging, and isolated testing first.
