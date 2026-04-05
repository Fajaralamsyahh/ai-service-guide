# PANDUAN LENGKAP: AI ASSISTANT & BUSINESS BOT SERVICE
## Dari Nol Menjadi Service Provider

**Version 1.0 | April 2026**
**By: Aira ⚡ (AI Assistant)**

---

# 📋 DAFTAR ISI

1. [Pendahuluan](#1-pendahuluan)
2. [apa Itu AI Assistant & Business Bot](#2-apa-itu-ai-assistant--business-bot)
3. [Hardware & Software Requirements](#3-hardware--software-requirements)
4. [Tutorial VPS](#4-tutorial-vps)
5. [Install OpenClaw](#5-install-openclaw)
6. [Setup WhatsApp Gateway](#6-setup-whatsapp-gateway)
7. [Setup Telegram Bot](#7-setup-telegram-bot)
8. [AI Assistant Setup](#8-ai-assistant-setup)
9. [Business Bot Configuration](#9-business-bot-configuration)
10. [Skill Installation](#10-skill-installation)
11. [Security Best Practices](#11-security-best-practices)
12. [Business Model & Pricing](#12-business-model--pricing)
13. [Troubleshooting](#13-troubleshooting)
14. [Lampiran](#14-lampiran)

---

# 1. PENDAHULUAN

## 1.1 Siapa Panduan Ini Untuk?

Panduan ini untuk kamu yang ingin:

- ✅ Membuat AI Assistant personal
- ✅ Membuat Business Bot untuk client
- ✅ Menjual jasa setup AI Bot
- ✅ Memulai bisnis AI Service

## 1.2 Apa Yang Akan Kamu Dapat?

Setelah membaca panduan ini, kamu akan bisa:

- Membeli dan setup VPS dengan benar
- Menginstall dan mengkonfigurasi OpenClaw
- Setup WhatsApp sebagai AI gateway
- Setup Telegram Bot multiple untuk client
- Membuat AI Assistant personal atau business
- Menawarkan jasa setup AI Bot

## 1.3 Prerequisites (Yang Dibutuhkan)

```
Hardware:
- Laptop/Komputer dengan koneksi internet
- Smartphone (untuk WhatsApp)

Software:
- Browser (Chrome/Firefox)
- SSH Client (Windows: PuTTY/Android: Termius)
- Text Editor (VS Code)

Budget:
- VPS: Rp 50.000 - 150.000/bulan
- Domain (optional): Rp 50.000-100.000/tahun
```

---

# 2. APA ITU AI ASSISTANT & BUSINESS BOT?

## 2.1 Definisi

```
AI ASSISTANT (Personal):
- AI yang membantumu dalam日常工作
- Chat dengan kamu secara PRIVAT
- Bisa automation tugas repetitif
- Contoh: reminds, drafting, research

BUSINESS BOT:
- AI untuk bisnis/client
- Auto-reply customer
- CS automation
- Bisa public (siapa aja bisa chat)
```

## 2.2 Perbedaan Penting

| Aspek | AI Assistant | Business Bot |
|-------|--------------|--------------|
| **Akses** | Private (kamu sendiri) | Public (siapa aja) |
| **Pengguna** | Kamu saja | Banyak user |
| **Tujuan** | Productivity | Customer Service |
| **Platform** | WhatsApp/Telegram | WhatsApp/Telegram |
| **Nomor HP** | Utama/Pribadi | Terpisah |

## 2.3 Two Numbers Concept

```
NOMOR UTAMA (Pribadi):
├── Untuk komunikasi normal
├── Chat dengan keluarga/teman
└── JANGAN digabungkan dengan AI

NOMOR KEDUA (Untuk AI):
├── Untuk AI Assistant atau Business Bot
├── Terpisah dari nomor utama
└── Bisa: second SIM, eSIM, virtual number
```

---

# 3. HARDWARE & SOFTWARE REQUIREMENTS

## 3.1 VPS (Virtual Private Server)

VPS adalah server yang kamu sewa untuk menjalankan bot 24/7.

### Rekomendasi VPS Provider:

| Provider | Harga/Bulan | Spec | Link |
|----------|-------------|------|------|
| DigitalOcean | Rp 60rb | 1 vCPU, 1GB RAM | digitalocean.com |
| Vultr | Rp 70rb | 1 vCPU, 1GB RAM | vultr.com |
| Linode | Rp 60rb | 1 vCPU, 2GB RAM | linode.com |
| Hetzner | Rp 50rb | 2 vCPU, 4GB RAM | hetzner.com |

### Spec Minimal:

```
CPU: 1 vCPU
RAM: 1 GB (2 GB recommended)
Storage: 20 GB SSD
Bandwidth: 1 TB
OS: Ubuntu 22.04 LTS
```

## 3.2 SSH Client

### Untuk Windows:
```
Download: PuTTY (https://putty.org)
Atau: Windows Terminal (built-in)
```

### Untuk Android:
```
Download: Termius (Play Store)
Atau: JuiceSSH (Play Store)
```

### Untuk Mac/Linux:
```
Sudah built-in: Terminal
Buka via: Applications > Utilities > Terminal
```

## 3.3 Text Editor

```
Recommended: VS Code (https://code.visualstudio.com)
- Free
- Support banyak bahasa
- Extension untuk everything
```

---

# 4. TUTORIAL VPS

## 4.1 Langkah 1: Beli VPS

### Di DigitalOcean:

```
1. Buka https://www.digitalocean.com
2. Sign Up / Login
3. Klik "Create" > "Droplets"
4. Pilih:
   - Region: Singapore (terdekat)
   - OS: Ubuntu 22.04 LTS
   - Plan: $6/month (Rp 60rb)
   - Authentication: SSH Keys (recommended)
5. Klik "Create Droplet"
6. Tunggu 1-2 menit
7. Droplet ready!
```

### Di Vultr:

```
1. Buka https://www.vultr.com
2. Sign Up / Login
3. Klik "+" > Deploy Server
4. Pilih:
   - Location: Singapore
   - Server Type: Cloud Compute
   - OS: Ubuntu 22.04 LTS
   - Size: $5/month
5. Klik "Deploy Now"
```

## 4.2 Langkah 2: Dapatkan SSH Credentials

Setelah droplet/server dibuat, kamu akan dapat:

```
IP Address: contoh: 143.198.xx.xx
Username: root
Password: (dikirim via email) ATAU
SSH Key: (jika dipilih saat setup)
```

**SIMPAN CREDENTIALS INI!**

## 4.3 Langkah 3: Connect ke VPS

### Menggunakan Windows (PuTTY):

```
1. Download & Install PuTTY
2. Buka PuTTY
3. Host Name: IP VPS kamu (contoh: 143.198.xx.xx)
4. Port: 22
5. Connection Type: SSH
6. Klik "Open"
7. Login as: root
8. Enter password: (paste dari email)
9. Done! Kamu sudah di server VPS
```

### Menggunakan Windows Terminal (CMD):

```
1. Buka Command Prompt (CMD)
2. Ketik:
   ssh root@143.198.xx.xx
3. Enter
4. Paste password
5. Done!
```

### Menggunakan Android (Termius):

```
1. Download Termius dari Play Store
2. Buka Termius
3. Klik "+" > New Host
4. Fill in:
   - Hostname: IP VPS kamu
   - Username: root
   - Password: (isi password)
5. Save & Connect
```

## 4.4 Langkah 4: Update Server

Setelah login, jalankan:

```bash
# Update package list
apt update

# Upgrade all packages
apt upgrade -y

# Install essentials
apt install -y curl wget git unzip
```

---

# 5. INSTALL OPENCLAW

## 5.1 Install Node.js & npm

```bash
# Install Node.js 18.x
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Verify installation
node --version
npm --version
```

## 5.2 Install OpenClaw

```bash
# Install OpenClaw globally
npm install -g openclaw

# Verify installation
openclaw --version
```

## 5.3 Initialize OpenClaw

```bash
# Initialize OpenClaw
openclaw init

# Start OpenClaw
openclaw start
```

## 5.4 Setup Service (Auto-start)

```bash
# Create systemd service
sudo nano /etc/systemd/system/openclaw.service

# Paste ini:
[Unit]
Description=OpenClaw Service
After=network.target

[Service]
Type=simple
User=root
WorkingDirectory=/root
ExecStart=/usr/bin/openclaw start
Restart=on-failure

[Install]
WantedBy=multi-user.target

# Save: Ctrl+X > Y > Enter

# Enable service
sudo systemctl daemon-reload
sudo systemctl enable openclaw
sudo systemctl start openclaw

# Check status
sudo systemctl status openclaw
```

## 5.5 Setup DNS (Optional untuk Web Interface)

```bash
# Install Nginx
apt install -y nginx

# Configure Nginx
sudo nano /etc/nginx/sites-available/default

# Paste:
server {
    listen 80;
    server_name YOUR_DOMAIN_OR_IP;

    location / {
        proxy_pass http://localhost:18789;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

# Save: Ctrl+X > Y > Enter

# Restart Nginx
sudo systemctl restart nginx
```

---

# 6. SETUP WHATSAPP GATEWAY

## 6.1 Enable WhatsApp Plugin

```bash
# Buka dashboard (biasanya http://IP:18789)
# Atau gunakan command line
openclaw config
```

## 6.2 Generate QR Code

```
1. Buka dashboard OpenClaw
2. Navigate ke: Settings > Channels
3. Klik "WhatsApp"
4. Klik "Enable"
5. Scan QR Code dengan HP
6. WhatsApp connected!
```

## 6.3 Authorized Senders

```javascript
// Dalam config, atur authorized senders:
{
  "channels": {
    "whatsapp": {
      "enabled": true,
      "authorizedSenders": [
        "+6281234567890"  // Nomor HP yang boleh chat
      ]
    }
  }
}
```

## 6.4 Two WhatsApp Strategy

```
STRATEGI 2 NOMOR:

Nomor Utama (0888...):
├── WhatsApp normal
├── Chat dengan semua orang
└── JANGAN digabungkan dengan AI

Nomor Kedua (0899...):
├── WhatsApp untuk AI
├── Pair dengan OpenClaw
├── AI respond ke chat
└── Bisa untuk personal AI atau business
```

---

# 7. SETUP TELEGRAM BOT

## 7.1 Buat Bot Baru

```
1. Buka Telegram
2. Search: @BotFather
3. Klik "Start"
4. Ketik: /newbot
5. Beri Nama Bot: (contoh: "Fajar AI")
6. Beri Username: (contoh: fajar_ai_bot)
7. BotFather kasih TOKEN:
   1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
8. SIMPAN TOKEN INI!
```

## 7.2 Configure OpenClaw dengan Token

```bash
# Buka dashboard atau config
openclaw config

# Navigate ke: Settings > Channels > Telegram
# Masukkan TOKEN dari BotFather
# Klik "Enable"
```

## 7.3 Set Authorized Chats

```javascript
// Dalam config:
{
  "channels": {
    "telegram": {
      "enabled": true,
      "botToken": "YOUR_BOT_TOKEN",
      "authorizedChats": [
        "123456789"  // Your Telegram Chat ID
      ]
    }
  }
}
```

## 7.4 Multiple Telegram Bots (Multiple Clients)

```javascript
// Setup per client berbeda port:

// Bot Client A
{
  "channels": {
    "telegram": {
      "enabled": true,
      "bots": {
        "clientA": {
          "token": "TOKEN_CLIENT_A",
          "authorizedChats": ["CHAT_ID_A"]
        },
        "clientB": {
          "token": "TOKEN_CLIENT_B",
          "authorizedChats": ["CHAT_ID_B"]
        }
      }
    }
  }
}
```

---

# 8. AI ASSISTANT SETUP

## 8.1 Apa Itu AI Assistant?

```
AI ASSISTANT = ChatGPT-like experience via WhatsApp/Telegram

Kamu chat ke bot
Bot AI jawab
Seperti chat biasa
Tapi AI yang jawab
```

## 8.2 Configuration

```javascript
// Dalam OpenClaw config:
{
  "ai": {
    "model": "minimax/MiniMax-M2.7",
    "personality": "helpful, friendly assistant",
    "context": "You are a helpful AI assistant"
  }
}
```

## 8.3 Personal AI Setup

```
UNTUK PERSONAL USE:

1. Siapkan nomor kedua (untuk WhatsApp)
   ATAU
   Setup Telegram Bot (lebih mudah)

2. Tentukan use case:
   - Research assistant
   - Writing assistant
   - Personal secretary
   - Knowledge base

3. Konfigurasi personality

4. Setup skills yang relevan

5. Test dengan chat
```

## 8.4 Personal AI via Telegram (Recommended)

```
STEP BY STEP:

1. Buat bot baru di @BotFather
   - Nama: "Personal AI"
   - Username: yourname_ai_bot

2. Dapatkan TOKEN

3. Share TOKEN ke service provider (lo sendiri)

4. Lo setup di OpenClaw

5. Bot jadi AI assistant lo

6. Lo chat ke @yourname_ai_bot

7. AI respond!
```

---

# 9. BUSINESS BOT CONFIGURATION

## 9.1 Apa Itu Business Bot?

```
BUSINESS BOT = AI-powered Customer Service

- Auto reply ke customer
- Answer FAQs
- Handle orders
- 24/7 available
- Professional responses
```

## 9.2 Business Bot Components

```javascript
// Konfigurasi Business Bot:

{
  "business": {
    "name": "Toko ABC Bot",
    "industry": "E-commerce",
    "personality": "Friendly, professional CS",
    "tone": "Casual but professional",
    
    "knowledge": {
      "products": ["Laptop", "HP", "Aksesoris"],
      "prices": {
        "Laptop": "Rp 5jt - 20jt",
        "HP": "Rp 1jt - 15jt"
      },
      "faq": [
        "Jam buka: 9 pagi - 9 malam",
        "Garansi: 1 tahun",
        "Pengiriman: 2-5 hari kerja"
      ]
    },
    
    "rules": [
      "Always be polite",
      "Escalate complex issues to human",
      "Don't make up prices",
      "Redirect to website for detailed info"
    ],
    
    "autoResponses": {
      "greeting": "Halo! Terima kasih sudah menghubungi Toko ABC. Ada yang bisa saya bantu?",
      "afterHours": "Maaf, kami sedang tutup. Jam operasional 9 pagi - 9 malam.早晨留言!"
    }
  }
}
```

## 9.3 Business Bot Setup Steps

```
STEP 1: Tentukan Business Type
- E-commerce
- Restaurant
- Consulting
- Healthcare
- dll

STEP 2: Kumpulkan Information
- Products/Services
- Prices
- FAQs
- Policies
- Tone/Personality

STEP 3: Konfigurasi AI
- Set personality
- Input knowledge base
- Set rules
- Configure auto-responses

STEP 4: Testing
- Test various scenarios
- Fix responses
- Refine answers

STEP 5: Deploy
- Go live
- Monitor conversations
- Adjust as needed
```

## 9.4 Industry-Specific Examples

### Contoh: Restaurant Bot

```javascript
{
  "business": {
    "name": "Warung Nusantara Bot",
    "industry": "Restaurant",
    "personality": "Friendly Indonesian waiter",
    
    "knowledge": {
      "menu": [
        {"name": "Nasi Goreng", "price": "Rp 25.000"},
        {"name": "Mie Goreng", "price": "Rp 23.000"},
        {"name": "Ayam Geprek", "price": "Rp 28.000"}
      ],
      "hours": "10 pagi - 10 malam",
      "location": "Jl. Merdeka No. 123, Jakarta",
      "delivery": "Grab/Gojek only"
    },
    
    "rules": [
      "Recommend popular dishes",
      "Ask if customer wants delivery or dine-in",
      "Confirm order before closing",
      "Always say thank you!"
    ]
  }
}
```

### Contoh: E-commerce Bot

```javascript
{
  "business": {
    "name": "GadgetStore Bot",
    "industry": "E-commerce Electronics",
    "personality": "Knowledgeable sales person",
    
    "knowledge": {
      "categories": ["HP", "Laptop", "Aksesoris"],
      "brands": ["Apple", "Samsung", "Xiaomi", "Asus"],
      "warranty": "1 tahun resmi",
      "paymentMethods": ["Transfer", "COD", "Midtrans"],
      "shipping": "JNE, J&T, SiCepat"
    },
    
    "rules": [
      "Help customers find products",
      "Compare specs when asked",
      "Inform about warranty clearly",
      "Redirect to human for complaints"
    ]
  }
}
```

---


# 10. AI MODELS: TYPES, PRICING & COMPARISON

## 10.1 Apa Itu AI Model?

```
AI MODEL = "Otak" dari AI Assistant

Model menentukan:
- Kualitas response
- Kecepatan
- Bahasa yang didukung
- Harga
- Limitasi
```

## 10.2 Jenis-Jenis AI Model

### Kategori Berdasarkan Fungsi:

```
LLM (Large Language Model):
├── Text generation
├── Conversation
├── Writing
└── Analysis
Contoh: GPT-4, Claude, Gemini

VISION MODELS:
├── Image analysis
├── OCR
├── Face recognition
└── Contoh: GPT-4V, Claude Vision

AUDIO MODELS:
├── Speech to text
├── Text to speech
└── Contoh: Whisper, ElevenLabs

MULTIMODAL:
├── Text + Image + Audio
├── Semua dalam satu
└── Contoh: GPT-4o, Gemini Pro Vision
```

### Kategori Berdasarkan Provider:

```
OPENAI:
├── GPT-4o (latest, fastest)
├── GPT-4 Turbo
├── GPT-3.5 Turbo
└── Whisper (audio)

ANTHROPIC:
├── Claude 3.5 Sonnet (best for coding)
├── Claude 3 Opus
├── Claude 3 Haiku (fastest)
└── Claude AI

GOOGLE:
├── Gemini 2.0 Flash (fastest)
├── Gemini 1.5 Pro
├── Gemini 1.5 Flash
└── Gemini 2.0 Flash Thinking

MISTRAL:
├── Mistral Large
├── Mistral Medium
├── Mistral Small
└── Open source options

MINIMAX:
├── MiniMax M2.7
├── MiniMax M2
└── Fast & affordable

OPEN SOURCE (FREE):
├── Llama 3.1 (Meta)
├── Qwen 2.5 (Alibaba)
├── DeepSeek V3
└── Bisa self-host
```

## 10.3 Perbandingan AI Models

### Tabel Perbandingan:

| Model | Provider | Speed | Quality | Price | Best For |
|-------|----------|-------|----------|-------|----------|
| GPT-4o | OpenAI | ⚡⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Everything |
| GPT-4 Turbo | OpenAI | ⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Coding, analysis |
| GPT-3.5 | OpenAI | ⚡⚡⚡⚡ | ⭐⭐⭐ | 💰 | Simple tasks |
| Claude 3.5 | Anthropic | ⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Coding, writing |
| Claude 3 | Anthropic | ⚡⚡ | ⭐⭐⭐⭐ | 💰💰 | Balanced |
| Gemini 2.0 | Google | ⚡⚡⚡⚡ | ⭐⭐⭐⭐ | 💰💰 | Fast tasks |
| MiniMax M2 | MiniMax | ⚡⚡⚡⚡ | ⭐⭐⭐ | 💰 | Budget-friendly |
| Llama 3.1 | Meta | ⚡⚡ | ⭐⭐⭐ | FREE | Self-host |

### Legenda:

```
Speed: ⚡⚡⚡⚡ = fastest, ⚡ = slow
Quality: ⭐⭐⭐⭐⭐ = best
Price: 💰💰💰 = expensive, 💰 = cheap
```

## 10.4 Pricing Comparison (per 1M tokens)

### OpenAI:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| GPT-4o | $2.50 | $10.00 | 128K |
| GPT-4o Mini | $0.15 | $0.60 | 128K |
| GPT-4 Turbo | $10.00 | $30.00 | 128K |
| GPT-3.5 Turbo | $0.50 | $2.00 | 16K |

### Anthropic:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Claude 3.5 Sonnet | $3.00 | $15.00 | 200K |
| Claude 3 Opus | $15.00 | $75.00 | 200K |
| Claude 3 Haiku | $0.25 | $1.25 | 200K |

### Google:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Gemini 2.0 Flash | $0.10 | $0.40 | 1M |
| Gemini 1.5 Pro | $1.25 | $5.00 | 128K |
| Gemini 1.5 Flash | $0.075 | $0.30 | 128K |

### MiniMax:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| MiniMax M2.7 | $0.20 | $0.70 | 32K |
| MiniMax M2 | $0.35 | $1.20 | 32K |

### Open Source (FREE):

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Llama 3.1 70B | FREE* | FREE* | 128K |
| Llama 3.1 8B | FREE* | FREE* | 128K |
| Qwen 2.5 72B | FREE* | FREE* | 128K |
| DeepSeek V3 | FREE* | FREE* | 128K |

* FREE jika self-host (butuh VPS dengan RAM besar)

## 10.5 Calculator Contoh Biaya

### Contoh 1: ChatGPT-like (1000 chats/bulan)

```
Per chat: ~500 tokens input + 300 tokens output
Per hari: 1000 chats × 800 tokens = 800,000 tokens
Per bulan: 800,000 × 30 = 24,000,000 tokens (24M)

Dengan GPT-4o Mini:
- Input: 24M × $0.15/1M = $3.60
- Output: 24M × $0.60/1M = $14.40
- Total: ~$18/bulan

Dengan Claude Haiku:
- Input: 24M × $0.25/1M = $6.00
- Output: 24M × $1.25/1M = $30.00
- Total: ~$36/bulan
```

### Contoh 2: Business Bot (500 chats/hari)

```
Per chat: ~200 tokens input + 150 tokens output
Per hari: 500 × 350 = 175,000 tokens
Per bulan: 175,000 × 30 = 5,250,000 tokens (5.25M)

Dengan Gemini Flash:
- Input: 5.25M × $0.075/1M = $0.39
- Output: 5.25M × $0.30/1M = $1.58
- Total: ~$2/bulan

Dengan GPT-4o Mini:
- Input: 5.25M × $0.15/1M = $0.79
- Output: 5.25M × $0.60/1M = $3.15
- Total: ~$4/bulan
```

## 10.6 Rekomendasi Berdasarkan Use Case

### Personal AI Assistant:

```
REKOMENDASI: MiniMax M2 atau GPT-4o Mini

Alasan:
- Affordable
- Fast response
- Good quality
- Cukup untuk daily tasks

Budget: ~$5-10/bulan
```

### Business Bot (Customer Service):

```
REKOMENDASI: Gemini 1.5 Flash atau GPT-4o Mini

Alasan:
- Fast (customer gak mau nunggu lama)
- Affordable
- Good enough untuk FAQ & simple queries

Budget: ~$2-5/bulan
```

### Coding Assistant:

```
REKOMENDASI: Claude 3.5 Sonnet

Alasan:
- Best for code generation
- Good debugging
- Long context (200K)

Budget: ~$20-50/bulan
```

### Complex Analysis / Research:

```
REKOMENDASI: GPT-4o atau Claude 3.5 Sonnet

Alasan:
- Highest quality
- Long context
- Complex reasoning

Budget: ~$30-100/bulan
```

## 10.7 Open Source vs Paid API

### Self-Host (Open Source):

```
MODELS:
├── Llama 3.1 70B (Meta)
├── Qwen 2.5 72B (Alibaba)
├── DeepSeek V3
└── Mistral Large

KEUNTUNGAN:
✅ FREE (tiap generate)
✅ No rate limits
✅ Full control
✅ Data privacy (all locally)

KEKURANGAN:
❌ Butuh VPS powerful (RAM 64GB+)
❌ Setup complex
❌ Maintenance sendiri
❌ Speed tergantung hardware

VPS untuk Self-Host:
- RAM: 64GB minimum
- CPU: 8+ cores
- Storage: 100GB+ SSD
- Cost: $50-100/bulan
```

### Paid API:

```
PROVIDERS:
├── OpenAI (GPT-4, GPT-3.5)
├── Anthropic (Claude)
├── Google (Gemini)
├── MiniMax
└── Lainnya

KEUNTUNGAN:
✅ Gak butuh VPS powerful
✅ Setup simpel
✅ Ready pakai
✅ Support dari provider

KEKURANGAN:
❌有料 (tiap token berbayar)
❌ Rate limits
❌ Data pergi ke server lain

BIASA UNTUK:
- Individual / small business
- Production apps
- Quick deployment
```

## 10.8 Cara Memilih AI Model

### Decision Tree:

```
START
  ↓
Budget under $10/month?
  ↓ YES → MiniMax atau Gemini Flash
  ↓ NO ↓
Need coding support?
  ↓ YES → Claude 3.5 Sonnet
  ↓ NO ↓
Need fastest response?
  ↓ YES → GPT-4o Mini atau Gemini Flash
  ↓ NO ↓
Need highest quality?
  ↓ YES → GPT-4o atau Claude 3.5 Sonnet
  ↓ NO ↓
Use case apa?
  ↓
Simple chatbot → GPT-4o Mini
Customer service → Gemini Flash
Research/Analysis → GPT-4o
Coding → Claude 3.5 Sonnet
```

### Checklist Pemilihan:

```
PILIH MODEL BERDASARKAN:

□ Budget
  └── Berapa budget per bulan?

□ Use Case
  └── Chatbot? Coding? Writing? Analysis?

□ Volume
  └── Berapa banyak chat per bulan?

□ Quality vs Speed
  └── Prioritas quality atau speed?

□ Privacy
  └── Data harus lokal atau boleh di-cloud?

□ Technical Skill
  └── Bisa self-host atau perlu managed?
```

## 10.9 OpenClaw Default Models

### OpenClaw Supports:

```
MiniMax:
├── minimax/MiniMax-M2.7 (current)
├── minimax/MiniMax-M2
└── Fast, affordable

OpenAI:
├── openai/gpt-4o
├── openai/gpt-4o-mini
├── openai/gpt-4-turbo
└── openai/gpt-3.5-turbo

Anthropic:
├── anthropic/claude-3.5-sonnet
├── anthropic/claude-3-opus
└── anthropic/claude-3-haiku

Google:
├── google/gemini-2.0-flash
├── google/gemini-1.5-pro
└── google/gemini-1.5-flash
```

### Setup di OpenClaw:

```javascript
// Dalam config:
{
  "ai": {
    "model": "minimax/MiniMax-M2.7",  // Default
    // Atau pilih model lain:
    // "openai/gpt-4o-mini"
    // "google/gemini-1.5-flash"
    // "anthropic/claude-3-haiku"
  }
}
```

## 10.10 Tips Optimasi Biaya

### 1. Use Smaller Models for Simple Tasks:

```
Simple FAQ → Use Haiku/GPT-3.5/Gemini Flash
Complex analysis → Use GPT-4/Claude 3.5
```

### 2. Implement Caching:

```
Same question within 5 min
  → Return cached response
  → No API call needed
  → SAVE COST
```

### 3. Optimize Prompt Length:

```
BAD: "You are a helpful assistant. You are designed to be helpful."
GOOD: "You are a helpful assistant."

Shorter prompt = fewer tokens = lower cost
```

### 4. Use System Prompts Efficiently:

```
System prompt → loaded once per conversation
User messages → cost setiap kali

Minimize user message length when possible
```

### 5. Batch Similar Requests:

```
Instead of 100 separate API calls
  → Batch into fewer calls
  → Save on connection overhead
```

## 10.11 Ringkasan Pricing Guide

### Budget Options:

```
$0-5/bulan:
├── Self-host Llama/Qwen (VPS $50+/bulan)
├── Gemini 1.5 Flash (very cheap)
└── MiniMax M2 (affordable)

$5-20/bulan:
├── GPT-4o Mini
├── Claude 3 Haiku
└── Gemini 1.5 Pro

$20-50/bulan:
├── Claude 3.5 Sonnet
├── GPT-4 Turbo
└── Gemini 1.5 Pro (high volume)

$50+/bulan:
├── GPT-4o
├── Claude 3 Opus
└── High volume production
```

### Quick Reference:

| Budget | Model Pilihan | Cocok Untuk |
|--------|---------------|-------------|
| FREE | Llama 3.1 (self-host) | Tech-savvy, privacy |
| $2/bulan | Gemini Flash | Simple bots |
| $5/bulan | GPT-4o Mini | General purpose |
| $20/bulan | Claude 3.5 Sonnet | Coding, writing |
| $50+/bulan | GPT-4o | Premium quality |

---

# 10. SKILL INSTALLATION

## 10.1 Apa Itu Skills?

```
SKILLS = Kemampuan tambahan untuk AI

Contoh:
- Weather skill: Cek cuaca
- Healthcheck skill: Server security
- Marketing skill: Content creation
- GitHub skill: Manage repos
- dll
```

## 10.2 Install Skills via CLI

```bash
# Check installed skills
openclaw skills list

# Search for skills
openclaw skills search "marketing"

# Install a skill
openclaw skills install marketing

# Update all skills
openclaw skills update
```

## 10.3 Recommended Skills

### Wajib untuk Trading Bot:

```bash
# Install这些 skills:
openclaw skills install healthcheck
openclaw skills install node-connect
```

### Untuk Business:

```bash
# Install这些 skills:
openclaw skills install marketing
openclaw skills install github
openclaw skills install notion-skill
```

## 10.4 Available Skills (2026)

| Skill | Fungsi | Worth |
|-------|--------|-------|
| weather | Cek cuaca | ⭐ |
| healthcheck | Server security audit | ⭐⭐⭐ |
| node-connect | VPS diagnosis | ⭐⭐ |
| tmux | Terminal management | ⭐⭐ |
| marketing | Content creation | ⭐⭐⭐ |
| github | Manage repos | ⭐⭐ |
| notion-skill | Notes integration | ⭐⭐ |
| crypto-news | Crypto news | ⭐⭐⭐ |
| nansen-smart-money-tracker | Whale tracking | ⭐⭐⭐ |

---

# 11. SECURITY BEST PRACTICES

## 11.1 VPS Security

```bash
# 1. Update регулярно
apt update && apt upgrade -y

# 2. Install fail2ban (prevents brute force)
apt install -y fail2ban

# 3. Setup firewall
ufw allow 22    # SSH
ufw allow 80    # HTTP
ufw allow 443   # HTTPS
ufw enable

# 4. Disable root login (advanced)
# Edit /etc/ssh/sshd_config
PermitRootLogin no

# 5. Use SSH keys instead of password
# Generate on local machine:
ssh-keygen -t rsa
# Copy to server:
ssh-copy-id root@YOUR_IP
```

## 11.2 API Key Security

```
DO:
✅ Use API keys with limited permissions
✅ Store in environment variables
✅ Rotate keys periodically
✅ Use read-only when possible

DON'T:
❌ Share keys in plain text
❌ Use same key for everything
❌ Commit keys to git
❌ Give full access when not needed
```

## 11.3 Client Data Security

```
PRINCIPLE: Minimal Access

For email automation:
- Use app password (not main password)
- Enable 2FA on email account
- Give only send/read permissions

For social media:
- Use platform API tokens
- Read-only when possible
- No full account access
```

## 11.4 Contract Template

```markdown
# SERVICE AGREEMENT

ANTAR ...
```

(Content truncated - full document is very long)

---

# 12. BUSINESS MODEL & PRICING

## 12.1 Cost Structure

```
FIXED COSTS (Lo sebagai provider):

Hardware:
- VPS lo: Rp 100.000/bulan (1 VPS bisa handle 5-10 clients)
- Domain (optional): Rp 100.000/tahun

Tools:
- OpenClaw: FREE (open source)
- Skills: FREE (community)
- AI Model: varies

VPS Client:
- Rp 60.000-100.000/bulan (client tanggung)
```

## 12.2 Pricing Packages

### Package 1: Basic Personal AI

```
Description: AI Assistant untuk personal use

Included:
- Setup Telegram/WhatsApp bot
- Basic AI configuration
- Personality setup
- Basic skills

Investment:
- Setup Fee: Rp 200.000 (one-time)
- Monthly: Rp 100.000 (maintenance)
```

### Package 2: Business Bot Starter

```
Description: Business bot untuk SME

Included:
- Everything in Basic
- Business knowledge base
- FAQ configuration
- Auto-response setup
- Professional tone

Investment:
- Setup Fee: Rp 400.000 (one-time)
- Monthly: Rp 150.000 (maintenance)
```

### Package 3: Full Business Automation

```
Description: Complete business solution

Included:
- Everything in Business Bot Starter
- Multi-platform integration
- (Email, Twitter, Instagram, Calendar)
- Advanced automation
- Priority support

Investment:
- Setup Fee: Rp 750.000 - 1.000.000
- Monthly: Rp 250.000 - 400.000
```

## 12.3 Monthly Retainer Model

```
RETAINER: Rp 150.000 - 300.000/bulan

Included:
- Monitoring
- Updates
- Troubleshooting
- Basic adjustments
- Email support

Lo dapat:
- Passive income
- Long-term client relationship
- Upsell opportunities
```

## 12.4 Success Metrics

```
KPI untuk bisnis:

Monthly:
- New clients: target 1-2
- Revenue: target Rp 500.000 - 2.000.000
- Client satisfaction: > 90%

Growth:
- Month 1: 2 clients
- Month 3: 5 clients  
- Month 6: 10 clients
- Month 12: 20 clients
```

---

# 13. TROUBLESHOOTING

## 13.1 Common VPS Issues

| Problem | Solution |
|---------|----------|
| Can't SSH | Check IP, password, firewall |
| Server slow | Upgrade RAM/CPU |
| Bot offline | Check PM2 logs |
| Domain not working | Check DNS propagation |

## 13.2 OpenClaw Issues

```bash
# Check status
openclaw status

# View logs
openclaw logs

# Restart service
openclaw restart

# Reset configuration
openclaw reset
```

## 13.3 WhatsApp Issues

```
Problem: WhatsApp disconnected
Solution:
1. Delete session file
2. Re-scan QR code
3. Check if phone has internet

Problem: QR not scanning
Solution:
1. Clear WhatsApp cache
2. Use WhatsApp Web first
3. Try different phone
```

## 13.4 Telegram Issues

```
Problem: Bot not responding
Solution:
1. Check bot token
2. Verify authorized chats
3. Check bot is started (/start)
4. Restart bot

Problem: Wrong responses
Solution:
1. Check AI configuration
2. Update knowledge base
3. Clear conversation context
```

---

# 14. LAMPIRAN

## 14.1 Glossary

```
AI - Artificial Intelligence
API - Application Programming Interface
Bot - Software application that runs automated tasks
Chat ID - Unique identifier for Telegram chat
Droplet - VPS instance on DigitalOcean
Gateway - Bridge between platforms
OpenClaw - AI assistant platform
PM2 - Process manager for Node.js
SSH - Secure Shell for remote access
Token - API authentication key
VPS - Virtual Private Server
```

## 14.2 Useful Commands

```bash
# VPS
ssh root@IP_VPS                    # Connect to VPS
exit                               # Disconnect

# OpenClaw
openclaw start                     # Start
openclaw stop                      # Stop
openclaw restart                   # Restart
openclaw status                    # Check status
openclaw logs                      # View logs

# PM2 (Process Manager)
pm2 list                          # List all processes
pm2 logs name --lines 50         # View logs
pm2 restart name                   # Restart process
pm2 stop name                     # Stop process

# System
apt update && apt upgrade -y       # Update system
htop                              # Monitor resources
nano file.txt                     # Edit file
cat file.txt                      # View file
```

## 14.3 Recommended Resources

```
LEARNING:
- OpenClaw Docs: https://docs.openclaw.ai
- ClawHub: https://clawhub.ai (skill marketplace)
- Solana Dev Docs: https://docs.solana.com

TOOLS:
- PuTTY: https://putty.org
- Termius: https://termius.com
- VS Code: https://code.visualstudio.com

VPS:
- DigitalOcean: https://digitalocean.com
- Vultr: https://vultr.com
- Linode: https://linode.com
```

## 14.4 Version History

```
Version 1.0 (April 2026)
- Initial release
- VPS setup guide
- OpenClaw installation
- WhatsApp/Telegram setup
- Business bot configuration
- Security best practices
- Business model & pricing
```

---

# 📞 SUPPORT

```
Questions about this guide?
Contact: (your contact info)

Found errors or want to contribute?
Submit PR to: (GitHub repo)
```

---

**DISCLAIMER:**

```
Panduan ini disusun berdasarkan pengalaman dan knowledge.
Hasil bisa vary tergantung implementation.
Author tidak bertanggung jawab untuk damages.
Use at your own risk.
```

---

**© 2026 Panduan AI Assistant Service**
**All Rights Reserved**
# 10. AI MODELS: TYPES, PRICING & COMPARISON

## 10.1 Apa Itu AI Model?

```
AI MODEL = "Otak" dari AI Assistant

Model menentukan:
- Kualitas response
- Kecepatan
- Bahasa yang didukung
- Harga
- Limitasi
```

## 10.2 Jenis-Jenis AI Model

### Kategori Berdasarkan Fungsi:

```
LLM (Large Language Model):
├── Text generation
├── Conversation
├── Writing
└── Analysis
Contoh: GPT-4, Claude, Gemini

VISION MODELS:
├── Image analysis
├── OCR
├── Face recognition
└── Contoh: GPT-4V, Claude Vision

AUDIO MODELS:
├── Speech to text
├── Text to speech
└── Contoh: Whisper, ElevenLabs

MULTIMODAL:
├── Text + Image + Audio
├── Semua dalam satu
└── Contoh: GPT-4o, Gemini Pro Vision
```

### Kategori Berdasarkan Provider:

```
OPENAI:
├── GPT-4o (latest, fastest)
├── GPT-4 Turbo
├── GPT-3.5 Turbo
└── Whisper (audio)

ANTHROPIC:
├── Claude 3.5 Sonnet (best for coding)
├── Claude 3 Opus
├── Claude 3 Haiku (fastest)
└── Claude AI

GOOGLE:
├── Gemini 2.0 Flash (fastest)
├── Gemini 1.5 Pro
├── Gemini 1.5 Flash
└── Gemini 2.0 Flash Thinking

MISTRAL:
├── Mistral Large
├── Mistral Medium
├── Mistral Small
└── Open source options

MINIMAX:
├── MiniMax M2.7
├── MiniMax M2
└── Fast & affordable

OPEN SOURCE (FREE):
├── Llama 3.1 (Meta)
├── Qwen 2.5 (Alibaba)
├── DeepSeek V3
└── Bisa self-host
```

## 10.3 Perbandingan AI Models

| Model | Provider | Speed | Quality | Price | Best For |
|-------|----------|-------|----------|-------|----------|
| GPT-4o | OpenAI | ⚡⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Everything |
| GPT-4 Turbo | OpenAI | ⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Coding, analysis |
| GPT-3.5 | OpenAI | ⚡⚡⚡⚡ | ⭐⭐⭐ | 💰 | Simple tasks |
| Claude 3.5 | Anthropic | ⚡⚡ | ⭐⭐⭐⭐⭐ | 💰💰💰 | Coding, writing |
| Claude 3 | Anthropic | ⚡⚡ | ⭐⭐⭐⭐ | 💰💰 | Balanced |
| Gemini 2.0 | Google | ⚡⚡⚡⚡ | ⭐⭐⭐⭐ | 💰💰 | Fast tasks |
| MiniMax M2 | MiniMax | ⚡⚡⚡⚡ | ⭐⭐⭐ | 💰 | Budget-friendly |
| Llama 3.1 | Meta | ⚡⚡ | ⭐⭐⭐ | FREE | Self-host |

## 10.4 Pricing Comparison (per 1M tokens)

### OpenAI:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| GPT-4o | $2.50 | $10.00 | 128K |
| GPT-4o Mini | $0.15 | $0.60 | 128K |
| GPT-4 Turbo | $10.00 | $30.00 | 128K |
| GPT-3.5 Turbo | $0.50 | $2.00 | 16K |

### Anthropic:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Claude 3.5 Sonnet | $3.00 | $15.00 | 200K |
| Claude 3 Opus | $15.00 | $75.00 | 200K |
| Claude 3 Haiku | $0.25 | $1.25 | 200K |

### Google:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Gemini 2.0 Flash | $0.10 | $0.40 | 1M |
| Gemini 1.5 Pro | $1.25 | $5.00 | 128K |
| Gemini 1.5 Flash | $0.075 | $0.30 | 128K |

### MiniMax:

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| MiniMax M2.7 | $0.20 | $0.70 | 32K |
| MiniMax M2 | $0.35 | $1.20 | 32K |

### Open Source (FREE):

| Model | Input | Output | Context |
|-------|-------|--------|---------|
| Llama 3.1 70B | FREE* | FREE* | 128K |
| Llama 3.1 8B | FREE* | FREE* | 128K |
| Qwen 2.5 72B | FREE* | FREE* | 128K |
| DeepSeek V3 | FREE* | FREE* | 128K |

* FREE jika self-host (butuh VPS dengan RAM besar)

## 10.5 Calculator Contoh Biaya

### Contoh 1: ChatGPT-like (1000 chats/bulan)

```
Per chat: ~500 tokens input + 300 tokens output
Per hari: 1000 chats x 800 tokens = 800,000 tokens
Per bulan: 800,000 x 30 = 24,000,000 tokens (24M)

Dengan GPT-4o Mini:
- Input: 24M x $0.15/1M = $3.60
- Output: 24M x $0.60/1M = $14.40
- Total: ~$18/bulan

Dengan Claude Haiku:
- Input: 24M x $0.25/1M = $6.00
- Output: 24M x $1.25/1M = $30.00
- Total: ~$36/bulan
```

### Contoh 2: Business Bot (500 chats/hari)

```
Per chat: ~200 tokens input + 150 tokens output
Per hari: 500 x 350 = 175,000 tokens
Per bulan: 175,000 x 30 = 5,250,000 tokens (5.25M)

Dengan Gemini Flash:
- Input: 5.25M x $0.075/1M = $0.39
- Output: 5.25M x $0.30/1M = $1.58
- Total: ~$2/bulan

Dengan GPT-4o Mini:
- Input: 5.25M x $0.15/1M = $0.79
- Output: 5.25M x $0.60/1M = $3.15
- Total: ~$4/bulan
```

## 10.6 Rekomendasi Berdasarkan Use Case

### Personal AI Assistant:

```
REKOMENDASI: MiniMax M2 atau GPT-4o Mini

Alasan:
- Affordable
- Fast response
- Good quality
- Cukup untuk daily tasks

Budget: ~$5-10/bulan
```

### Business Bot (Customer Service):

```
REKOMENDASI: Gemini 1.5 Flash atau GPT-4o Mini

Alasan:
- Fast (customer gak mau nunggu lama)
- Affordable
- Good enough untuk FAQ & simple queries

Budget: ~$2-5/bulan
```

### Coding Assistant:

```
REKOMENDASI: Claude 3.5 Sonnet

Alasan:
- Best for code generation
- Good debugging
- Long context (200K)

Budget: ~$20-50/bulan
```

### Complex Analysis / Research:

```
REKOMENDASI: GPT-4o atau Claude 3.5 Sonnet

Alasan:
- Highest quality
- Long context
- Complex reasoning

Budget: ~$30-100/bulan
```

## 10.7 Open Source vs Paid API

### Self-Host (Open Source):

```
MODELS:
├── Llama 3.1 70B (Meta)
├── Qwen 2.5 72B (Alibaba)
├── DeepSeek V3
└── Mistral Large

KEUNTUNGAN:
+ FREE (tiap generate)
+ No rate limits
+ Full control
+ Data privacy (all locally)

KEKURANGAN:
- Butuh VPS powerful (RAM 64GB+)
- Setup complex
- Maintenance sendiri
- Speed tergantung hardware

VPS untuk Self-Host:
- RAM: 64GB minimum
- CPU: 8+ cores
- Storage: 100GB+ SSD
- Cost: $50-100/bulan
```

### Paid API:

```
PROVIDERS:
+ OpenAI (GPT-4, GPT-3.5)
+ Anthropic (Claude)
+ Google (Gemini)
+ MiniMax
+ Lainnya

KEUNTUNGAN:
+ Gak butuh VPS powerful
+ Setup simpel
+ Ready pakai
+ Support dari provider

KEKURANGAN:
-有料 (tiap token berbayar)
- Rate limits
- Data pergi ke server lain

BIASA UNTUK:
- Individual / small business
- Production apps
- Quick deployment
```

## 10.8 Cara Memilih AI Model

### Decision Tree:

```
START
  |
Budget under $10/month?
  |--YES--> MiniMax atau Gemini Flash
  |--NO-->|
Need coding support?
  |--YES--> Claude 3.5 Sonnet
  |--NO-->|
Need fastest response?
  |--YES--> GPT-4o Mini atau Gemini Flash
  |--NO-->|
Need highest quality?
  |--YES--> GPT-4o atau Claude 3.5 Sonnet
  |--NO-->|
Use case apa?
  |
Simple chatbot --> GPT-4o Mini
Customer service --> Gemini Flash
Research/Analysis --> GPT-4o
Coding --> Claude 3.5 Sonnet
```

### Checklist Pemilihan:

```
PILIH MODEL BERDASARKAN:

[ ] Budget
     Berapa budget per bulan?

[ ] Use Case
     Chatbot? Coding? Writing? Analysis?

[ ] Volume
     Berapa banyak chat per bulan?

[ ] Quality vs Speed
     Prioritas quality atau speed?

[ ] Privacy
     Data harus lokal atau boleh di-cloud?

[ ] Technical Skill
     Bisa self-host atau perlu managed?
```

## 10.9 OpenClaw Default Models

### OpenClaw Supports:

```
MiniMax:
- minimax/MiniMax-M2.7 (current)
- minimax/MiniMax-M2
- Fast, affordable

OpenAI:
- openai/gpt-4o
- openai/gpt-4o-mini
- openai/gpt-4-turbo
- openai/gpt-3.5-turbo

Anthropic:
- anthropic/claude-3.5-sonnet
- anthropic/claude-3-opus
- anthropic/claude-3-haiku

Google:
- google/gemini-2.0-flash
- google/gemini-1.5-pro
- google/gemini-1.5-flash
```

### Setup di OpenClaw:

```javascript
// Dalam config:
{
  "ai": {
    "model": "minimax/MiniMax-M2.7",  // Default
    // Atau pilih model lain:
    // "openai/gpt-4o-mini"
    // "google/gemini-1.5-flash"
    // "anthropic/claude-3-haiku"
  }
}
```

## 10.10 Tips Optimasi Biaya

### 1. Use Smaller Models for Simple Tasks:

```
Simple FAQ --> Use Haiku/GPT-3.5/Gemini Flash
Complex analysis --> Use GPT-4/Claude 3.5
```

### 2. Implement Caching:

```
Same question within 5 min
  --> Return cached response
  --> No API call needed
  --> SAVE COST
```

### 3. Optimize Prompt Length:

```
BAD: "You are a helpful assistant. You are designed to be helpful."
GOOD: "You are a helpful assistant."

Shorter prompt = fewer tokens = lower cost
```

### 4. Use System Prompts Efficiently:

```
System prompt --> loaded once per conversation
User messages --> cost setiap kali

Minimize user message length when possible
```

### 5. Batch Similar Requests:

```
Instead of 100 separate API calls
  --> Batch into fewer calls
  --> Save on connection overhead
```

## 10.11 Ringkasan Pricing Guide

### Budget Options:

```
$0-5/bulan:
- Self-host Llama/Qwen (VPS $50+/bulan)
- Gemini 1.5 Flash (very cheap)
- MiniMax M2 (affordable)

$5-20/bulan:
- GPT-4o Mini
- Claude 3 Haiku
- Gemini 1.5 Pro

$20-50/bulan:
- Claude 3.5 Sonnet
- GPT-4 Turbo
- Gemini 1.5 Pro (high volume)

$50+/bulan:
- GPT-4o
- Claude 3 Opus
- High volume production
```

### Quick Reference:

| Budget | Model Pilihan | Cocok Untuk |
|--------|---------------|-------------|
| FREE | Llama 3.1 (self-host) | Tech-savvy, privacy |
| $2/bulan | Gemini Flash | Simple bots |
| $5/bulan | GPT-4o Mini | General purpose |
| $20/bulan | Claude 3.5 Sonnet | Coding, writing |
| $50+/bulan | GPT-4o | Premium quality |
