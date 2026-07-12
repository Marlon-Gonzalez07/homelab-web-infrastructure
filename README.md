# 💻 Homelab Web Infrastructure

A browser-based Linux course built on Proxmox. The goal was to create a professional learning environment accessible from anywhere without any local setup required.

> Built as a side project to help colleagues prepare for their Linux exam while also serving as the foundation for a reusable web infrastructure.

## 📖 Full Documentation in German

[Dokumentation](https://brawny-dracorex-d4b.notion.site/Homelab-Web-Infrastructure-31ac8d95942180329215e5b1df903215)

## 📖 Full Documentation in English

[Documentation](https://brawny-dracorex-d4b.notion.site/Homelab-Web-Infrastructure-English-371c8d959421801baaa0f9fbafdbf6f2)

## 📦 Tech Stack

- Proxmox VE
- Debian 12
- Nginx (Reverse Proxy)
- MkDocs + Material Theme
- Apache Guacamole
- Docker Compose
- Cloudflare Tunnel
- MySQL

## 🦄 Features

- Browser-based terminal access via Apache Guacamole
- Dedicated VM per apprentice
- No password login required (credentials stored in Guacamole)
- Accessible from anywhere via Cloudflare Tunnel
- 8 course chapters in MkDocs
- VM reset capability via Proxmox snapshots

## 🎯 Architecture

<img width="676" height="929" alt="image" src="https://github.com/user-attachments/assets/8bfc0a53-d738-4fbe-98a4-c4170e4e9cf6" />

Internet → Cloudflare Tunnel → Nginx Reverse Proxy → MkDocs / Guacamole → Apprentice VMs → Proxmox Host

## 🍿 Video

https://github.com/user-attachments/assets/938a8462-f7a6-43ec-9d51-009618ef0a28

## 🔁 Reusable Infrastructure

This project serves as a base infrastructure for multiple web projects. Adding a new service is as simple as:

1. Create a new VM or project
2. Add a new location block in Nginx
3. Add a new subdomain in Cloudflare
4. Done! 

**Already running:**

- 🐧 Linux Course (this project)

**Planned:**

- 📝 CTF Writeups
- 🌐 Portfolio Website
- 📚 Documentation Wiki

## 📚 What I Learned

- Setting up and managing multiple Linux VMs on Proxmox
- Configuring Nginx as a Reverse Proxy including WebSocket support
- Deploying services with Docker and Docker Compose
- Setting up Cloudflare Tunnel for secure external access
- WebSocket configuration for real-time browser applications
- Network fundamentals in a homelab environment

## 💭 How can it be improved?

- Add a another course
- Add a monitoring dashboard
- Add more course chapters

## 🚦 Requirements

- Proxmox Server (min. 16GB RAM depending on how many VMs)
- Cloudflare Account (Free)
- Domain (recommended)
- Debian 12 ISO
