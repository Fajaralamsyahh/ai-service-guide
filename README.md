# PANDUAN LENGKAP: AI ASSISTANT & BUSINESS BOT SERVICE
## Dari Nol Menjadi Service Provider

**Version 2.0 | April 2026**

---

## 📑 DAFTAR ISI

### BAGIAN 1: PENDIDIKAN
1. [Apa Itu AI Assistant?](#1-apa-itu-ai-assistant)
2. [Apa Itu Business Bot?](#2-apa-itu-business-bot)
3. [Perbedaan AI Assistant vs Business Bot](#3-perbedaan-ai-assistant-vs-business-bot)
4. [Two Numbers Concept](#4-two-numbers-concept)
5. [Platform yang Didukung](#5-platform-yang-didukung)

### BAGIAN 2: VPS & SERVER
6. [Apa Itu VPS?](#6-apa-itu-vps)
7. [Rekomendasi Provider VPS](#7-rekomendasi-provider-vps)
8. [Cara Beli VPS](#8-cara-beli-vps)
9. [SSH: Connect ke VPS](#9-ssh-connect-ke-vps)
10. [Update & Setup Awal Server](#10-update--setup-awal-server)

### BAGIAN 3: INSTALASI
11. [Install Node.js](#11-install-nodejs)
12. [Install OpenClaw](#12-install-openclaw)
13. [Setup Auto-Start (PM2)](#13-setup-auto-start-pm2)
14. [Setup DNS & Web Interface](#14-setup-dns--web-interface)

### BAGIAN 4: CHANNEL SETUP
15. [Setup WhatsApp Gateway](#15-setup-whatsapp-gateway)
16. [Setup Telegram Bot](#16-setup-telegram-bot)
17. [Setup Multiple Bots](#17-setup-multiple-bots)

### BAGIAN 5: AI MODELS
18. [Jenis-Jenis AI Model](#18-jenis-jenis-ai-model)
19. [Perbandingan & Pricing](#19-perbandingan--pricing)
20. [Cara Pilih AI Model](#20-cara-pilih-ai-model)
21. [Setup di OpenClaw](#21-setup-di-openclaw)

### BAGIAN 6: BUSINESS BOT
22. [Konfigurasi Business Bot](#22-konfigurasi-business-bot)
23. [Contoh per Industri](#23-contoh-per-industri)
24. [Personality & Tone](#24-personality--tone)
25. [Knowledge Base](#25-knowledge-base)
26. [Automation Rules](#26-automation-rules)

### BAGIAN 7: SKILLS
27. [Apa Itu Skills?](#27-apa-itu-skills)
28. [Install Skills](#28-install-skills)
29. [Rekomendasi Skills](#29-rekomendasi-skills)

### BAGIAN 8: SECURITY
30. [VPS Security](#30-vps-security)
31. [API Key Security](#31-api-key-security)
32. [Client Data Security](#32-client-data-security)

### BAGIAN 9: BISNIS
33. [Business Model](#33-business-model)
34. [Pricing Packages](#34-pricing-packages)
35. [Cara Get Clients](#35-cara-get-clients)

### BAGIAN 10: TROUBLESHOOTING
36. [Common Issues](#36-common-issues)
37. [Commands Reference](#37-commands-reference)

---

## BAGIAN 1: PENDIDIKAN

---

### 1. APA ITU AI ASSISTANT?

AI Assistant adalah AI yang membantumu dalam kegiatan sehari-hari melalui chat.

```
Contoh:
- Kamu chat: "Buatin email balasan ke client"
- AI jawab: Email lengkap
- Kamu copy paste
```

**Sama seperti chat dengan saya (Aira) sekarang, tapi bisa di-SETUP untuk kebutuhan spesifik.**

---

### 2. APA ITU BUSINESS BOT?

Business Bot adalah AI yang menangani customer service atau sales secara otomatis.

```
Contoh:
- Customer chat: "Harga iPhone berapa?"
- AI jawab: "iPhone 15 = Rp 15.900.000"
- Customer chat: "Ready stock?"
- AI jawab: "Ya, ready. Mau order?"
```

**24/7 auto-respond, tanpa perlu manusia standby.**

---

### 3. PERBEDAAN AI ASSISTANT VS BUSINESS BOT

| Aspek | AI Assistant | Business Bot |
|-------|-------------|--------------|
| **Pengguna** | Kamu sendiri | Banyak customer |
| **Tujuan** | Productivity personal | CS/Sales Otomatis |
| **Akses** | Private (kamu aja) | Public (siapa aja) |
| **Platform** | WhatsApp/Telegram | WhatsApp/Telegram |
| **Nomor HP** | Utama atau kedua | Kedua (terpisah) |

---

### 4. TWO NUMBERS CONCEPT

```
NOMOR UTAMA (0888...):
├── WhatsApp normal
├── Chat dengan keluarga/teman
└── JANGAN digabungkan dengan AI

NOMOR KEDUA (0899...):
├── Untuk AI (Assistant atau Business Bot)
├── Terpisah dari nomor utama
└── Bisa: second SIM, eSIM, virtual number
```

**PENTING: Satu nomor = satu WhatsApp. Jika diparingan ke AI, WhatsApp normal di nomor itu tidak bisa digunakan.**

---

### 5. PLATFORM YANG DIDUKUNG

| Platform | Status | Setup | Biaya |
|----------|--------|-------|-------|
| **WhatsApp** | ✅ Available | QR Scan | Free* |
| **Telegram** | ✅ Available | Bot Token | Free* |
| **Discord** | ✅ Available | Bot Token | Free* |
| **Slack** | ✅ Available | Bot Token | Free* |
| **Line** | ✅ Available | Bot Token | Free* |
| **Signal** | ✅ Available | Bot Token | Free* |

*Free dari platform, tapi AI model berbayar per usage.

---

## BAGIAN 2: VPS & SERVER

---

### 6. APA ITU VPS?

VPS = Virtual Private Server

```
VPS = Server di cloud yang kamu SEWA
- Bisa running 24/7
- Bisa install software
- Bisa buka port
- Bisa akses dari mana aja
- Seperti komputer sendiri di internet
```

**Bot harus running terus, jadi butuh VPS (bukan laptop/komputer rumah yang bisa mati).**

---

### 7. REKOMENDASI PROVIDER VPS

| Provider | Harga/Bulan | Spec | Lokasi |
|----------|--------------|------|--------|
| **DigitalOcean** | Rp 60rb | 1 vCPU, 1GB RAM | Singapore |
| **Vultr** | Rp 70rb | 1 vCPU, 1GB RAM | Singapore |
| **Linode** | Rp 60rb | 1 vCPU, 2GB RAM | Singapore |
| **Hetzner** | Rp 50rb | 2 vCPU, 4GB RAM | Nuremberg |

**Spec Minimal:**
```
CPU: 1 vCPU
RAM: 1 GB (2 GB lebih baik)
Storage: 20 GB SSD
Bandwidth: 1 TB/bulan
OS: Ubuntu 22.04 LTS
```

---

### 8. CARA BELI VPS (DigitalOcean)

```
1. Buka https://digitalocean.com
2. Sign Up / Login
3. Klik "Create" > "Droplets"
4. Pilih:
   - Region: Singapore (terdekat)
   - OS: Ubuntu 22.04 LTS
   - Plan: $6/month
   - Authentication: SSH Keys (atau Password)
5. Klik "Create Droplet"
6. Tunggu 1-2 menit
7. Dapat IP Address (contoh: 143.198.xx.xx)
8. Simpan IP + credentials
```

**Credentials yang didapat:**
```
IP Address: 143.198.xx.xx
Username: root
Password: xxxxxxxx (dikirim via email)
```

---

### 9. SSH: CONNECT KE VPS

#### Dari Windows (CMD):

```bash
ssh root@143.198.xx.xx
# Enter password saat diminta
```

#### Dari Android (Termius - Play Store):

```
1. Download Termius
2. Klik "+" > New Host
3. Isi:
   - Hostname: 143.198.xx.xx
   - Username: root
   - Password: (password dari email)
4. Save > Connect
```

#### Dari Mac/Linux:

```bash
ssh root@143.198.xx.xx
# Enter password saat diminta
```

---

### 10. UPDATE & SETUP AWAL SERVER

Setelah connect, jalankan:

```bash
# Update package list
apt update

# Upgrade semua packages
apt upgrade -y

# Install tools dasar
apt install -y curl wget git unzip
```

---

## BAGIAN 3: INSTALASI

---

### 11. INSTALL NODE.JS

```bash
# Install Node.js 18.x
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Verify
node --version
npm --version
```

---

### 12. INSTALL OPENCLAW

```bash
# Install OpenClaw globally
npm install -g openclaw

# Verify
openclaw --version

# Initialize
openclaw init

# Start
openclaw start

# Buka dashboard
# http://IP_VPS:18789
```

---

### 13. SETUP AUTO-START (PM2)

```bash
# Install PM2
npm install -g pm2

# Start OpenClaw dengan PM2
pm2 start openclaw --name openclaw

# Setup auto-start saat server reboot
pm2 startup
pm2 save
```

**Commands PM2 berguna:**

```bash
pm2 list                    # Lihat semua process
pm2 logs openclaw --lines 50  # Lihat logs
pm2 restart openclaw       # Restart
pm2 stop openclaw          # Stop
pm2 delete openclaw        # Delete
```

---

### 14. SETUP DNS & WEB INTERFACE

#### Install Nginx:

```bash
apt install -y nginx
```

#### Configure:

```bash
sudo nano /etc/nginx/sites-available/default
```

Paste ini:

```nginx
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
```

```bash
# Restart Nginx
sudo systemctl restart nginx
```

Sekarang bisa akses: `http://IP_VPS`

---

## BAGIAN 4: CHANNEL SETUP

---

### 15. SETUP WHATSAPP GATEWAY

```
1. Buka dashboard OpenClaw: http://IP_VPS:18789
2. Navigate ke: Settings > Channels > WhatsApp
3. Klik "Enable"
4. Scan QR Code dengan nomor yang mau dipakai
5. WhatsApp connected!
```

**Catatan:**
- Gunakan nomor khusus untuk AI (bukan nomor utama)
- WhatsApp hanya bisa di-pair ke 1 device dalam satu waktu
- Jika nomor utama mau digunakan untuk AI, WhatsApp biasa tidak bisa dipakai

---

### 16. SETUP TELEGRAM BOT

#### Step 1: Buat Bot di Telegram

```
1. Buka Telegram
2. Search: @BotFather
3. Klik "Start"
4. Ketik: /newbot
5. Beri Nama Bot: (contoh: "AI Assistant Fajar")
6. Beri Username: (contoh: fajar_ai_bot) - harus diakhiri "_bot"
7. BotFather kasih TOKEN: 123456789:ABCdefGHIjklMNOpqrsTUVwxyz123456
8. SIMPAN TOKEN INI!
```

#### Step 2: Configure di OpenClaw

```
1. Buka dashboard OpenClaw
2. Navigate ke: Settings > Channels > Telegram
3. Masukkan TOKEN dari BotFather
4. Klik "Enable"
```

#### Step 3: Get Chat ID

```
1. Buka Telegram
2. Chat ke bot yang baru dibuat (@username_bot)
3. Ketik: /start
4. Kirim pesan apapun
5. Buka: https://api.telegram.org/botYOUR_TOKEN/getUpdates
6. Cari "chat": {"id": 123456789 }
7. Itu Chat ID kamu
```

---

### 17. SETUP MULTIPLE BOTS

#### Multiple Telegram Bots (Multiple Clients):

```bash
# Buka config
openclaw config
```

Edit config:

```javascript
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

**Tiap client = bot Telegram berbeda = token berbeda.**

---

## BAGIAN 5: AI MODELS

---

### 18. JENIS-JENIS AI MODEL

#### Berdasarkan Fungsi:

| Tipe | Fungsi | Contoh |
|------|--------|---------|
| **LLM** | Text generation, conversation | GPT-4, Claude, Gemini |
| **Vision** | Image analysis | GPT-4V, Claude Vision |
| **Audio** | Speech to text, TTS | Whisper, ElevenLabs |
| **Multimodal** | Text + Image + Audio | GPT-4o, Gemini Pro |

#### Berdasarkan Provider:

| Provider | Models | Harga |
|----------|--------|-------|
| **OpenAI** | GPT-4o, GPT-4o Mini, GPT-3.5 | 💰💰-💰💰💰 |
| **Anthropic** | Claude 3.5 Sonnet, Claude 3 Haiku | 💰💰-💰💰💰 |
| **Google** | Gemini 2.0 Flash, Gemini 1.5 Pro | 💰-💰💰 |
| **MiniMax** | MiniMax M2.7, MiniMax M2 | 💰 |
| **Meta (Open Source)** | Llama 3.1, Qwen 2.5, DeepSeek | FREE* |

*Free jika self-host, tapi butuh VPS powerful (RAM 64GB+)

---

### 19. PERBANDINGAN & PRICING

#### Perbandingan Quick Reference:

| Model | Provider | Speed | Quality | Harga/1M Tokens | Cocok Untuk |
|-------|----------|-------|---------|------------------|-------------|
| GPT-4o | OpenAI | ⚡⚡⚡ | ⭐⭐⭐⭐⭐ | $2.50 input | Premium tasks |
| GPT-4o Mini | OpenAI | ⚡⚡⚡⚡ | ⭐⭐⭐⭐ | $0.15 input | General purpose |
| Claude 3.5 Sonnet | Anthropic | ⚡⚡ | ⭐⭐⭐⭐⭐ | $3.00 input | Coding, writing |
| Claude 3 Haiku | Anthropic | ⚡⚡⚡⚡ | ⭐⭐⭐ | $0.25 input | Fast, cheap |
| Gemini 2.0 Flash | Google | ⚡⚡⚡⚡ | ⭐⭐⭐⭐ | $0.10 input | Fast, cheap |
| Gemini 1.5 Flash | Google | ⚡⚡⚡⚡ | ⭐⭐⭐ | $0.075 input | Very cheap |
| MiniMax M2.7 | MiniMax | ⚡⚡⚡⚡ | ⭐⭐⭐ | $0.20 input | Budget-friendly |

#### Perbandingan Detail (per 1M tokens):

| Model | Input | Output | Context Window |
|-------|-------|--------|----------------|
| GPT-4o | $2.50 | $10.00 | 128K |
| GPT-4o Mini | $0.15 | $0.60 | 128K |
| Claude 3.5 Sonnet | $3.00 | $15.00 | 200K |
| Claude 3 Haiku | $0.25 | $1.25 | 200K |
| Gemini 2.0 Flash | $0.10 | $0.40 | 1M |
| Gemini 1.5 Flash | $0.075 | $0.30 | 128K |
| MiniMax M2.7 | $0.20 | $0.70 | 32K |

#### Contoh Kalkulasi Biaya:

**Business Bot (500 chats/hari, 30 hari):**

```
Per chat: ~200 tokens input + 150 tokens output = 350 tokens
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

---

### 20. CARA PILIH AI MODEL

#### Berdasarkan Budget:

| Budget/Bulan | Model Pilihan | Notes |
|--------------|---------------|-------|
| **Free** | Llama 3.1 (self-host) | Butuh VPS RAM 64GB+ |
| **$1-5** | Gemini Flash, MiniMax M2 | Sangat affordable |
| **$5-15** | GPT-4o Mini, Claude Haiku | Balanced |
| **$15-50** | GPT-4o, Claude 3.5 Sonnet | Premium |

#### Berdasarkan Use Case:

| Use Case | Rekomendasi | Budget |
|----------|-------------|--------|
| **Personal Assistant** | GPT-4o Mini | $5-10/bulan |
| **Business CS Bot** | Gemini Flash, GPT-4o Mini | $2-5/bulan |
| **Coding Assistant** | Claude 3.5 Sonnet | $20-50/bulan |
| **Research/Analysis** | GPT-4o | $30-100/bulan |
| **Simple FAQ Bot** | Gemini Flash | $1-3/bulan |

---

### 21. SETUP DI OPENCLAW

#### Config di OpenClaw:

```javascript
// Dalam dashboard atau config file:
{
  "ai": {
    "model": "minimax/MiniMax-M2.7"  // Default
    // Atau pilih model lain:
    // "openai/gpt-4o-mini"
    // "google/gemini-1.5-flash"
    // "anthropic/claude-3-haiku"
  }
}
```

#### Model Aliases di OpenClaw:

```
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

MiniMax:
- minimax/MiniMax-M2.7
- minimax/MiniMax-M2
```

---

## BAGIAN 6: BUSINESS BOT

---

### 22. KONFIGURASI BUSINESS BOT

Business Bot butuh konfigurasi lebih dari AI Assistant:

```javascript
{
  "business": {
    "name": "Nama Toko Bot",
    "industry": "E-commerce / Restaurant / Healthcare / dll",
    
    "personality": {
      "role": "Customer Service",
      "tone": "Friendly, professional",
      "language": "Bahasa Indonesia",
      "description": "Kamu adalah customer service yang helpful"
    },
    
    "knowledge": {
      "products": ["List produk"],
      "prices": {"Produk": "Harga"},
      "faq": ["Pertanyaan umum"],
      "policies": ["Pengiriman", "Garansi", "Retur"]
    },
    
    "rules": [
      "Selalu sopan",
      "Escalate ke manusia untuk komplain besar",
      "Jangan invent harga sendiri",
      "Redirect ke website untuk detail"
    ],
    
    "autoResponses": {
      "greeting": "Halo! Terima kasih menghubungi [Nama]. Ada yang bisa saya bantu?",
      "afterHours": "Maaf, kami sedang tutup. Jam operasional: 9 pagi - 9 malam.",
      "unknown": "Maaf, saya tidak memahami pertanyaan tersebut. Bisa diulang atau hubungi human agent?"
    }
  }
}
```

---

### 23. CONTOH PER INDUSTRI

#### Restaurant:

```javascript
{
  "business": {
    "name": "Warung Nusantara Bot",
    "industry": "Restaurant",
    
    "knowledge": {
      "menu": [
        {"name": "Nasi Goreng", "price": "Rp 25.000", "desc": "Nasi digoreng dengan bumbu special"},
        {"name": "Mie Goreng", "price": "Rp 23.000", "desc": "Mie digoreng kering"},
        {"name": "Ayam Geprek", "price": "Rp 28.000", "desc": "Ayam crispy dengan sambal"}
      ],
      "hours": "10 pagi - 10 malam",
      "location": "Jl. Merdeka No. 123, Jakarta",
      "delivery": "Grab/Gojek only"
    },
    
    "rules": [
      "Rekomendasikan dish populer",
      "Tanya delivery atau dine-in",
      "Konfirmasi order sebelum closing",
      "Always say thank you!"
    ]
  }
}
```

#### E-commerce:

```javascript
{
  "business": {
    "name": "GadgetStore Bot",
    "industry": "E-commerce Electronics",
    
    "knowledge": {
      "categories": ["HP", "Laptop", "Aksesoris"],
      "brands": ["Apple", "Samsung", "Xiaomi", "Asus", "Lenovo"],
      "warranty": "1 tahun resmi distributor",
      "paymentMethods": ["Transfer BCA", "COD", "Midtrans"],
      "shipping": ["JNE", "J&T", "SiCepat"]
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

### 24. PERSONALITY & TONE

#### Tentukan Personality:

```
ROLES:
- Customer Service
- Sales Representative
- Technical Support
- Order Taker
- Appointment Scheduler
- Consultant
- Personal Assistant
```

#### Tone Examples:

| Role | Tone | Contoh |
|------|------|--------|
| **Casual Shop** | Friendly, casual | "Halo! Mau cari apa nih?" |
| **Premium Brand** | Professional, formal | "Selamat datang. Ada yang bisa saya bantu?" |
| **Tech Support** | Technical, patient | "Saya pahami issue-nya. Mari kita check step by step." |
| **Restaurant** | Warm, welcoming | "Hai! Mau makan apa hari ini?" |

---

### 25. KNOWLEDGE BASE

```
KNOWLEDGE BASE TERDIRI DARI:

1. PRODUCTS/SERVICES
   - List lengkap produk/jasa
   - Deskripsi singkat
   - Variants

2. PRICING
   - Harga each product
   - Promo/diskon
   - Bundle packages

3. FAQ (Frequently Asked Questions)
   - Jam operasional
   - Cara order
   - Info pengiriman
   - Kebijakan retur

4. POLICIES
   - Garansi
   - Pengiriman
   - Pembayaran
   - Complaint handling
```

---

### 26. AUTOMATION RULES

```
RULES UNTUK BUSINESS BOT:

1. Greeting
   - Auto-reply untuk salam pembuka
   - Sesuaikan jam operasional

2. FAQ Handling
   - Jawaban instant untuk pertanyaan umum
   - Link ke resources

3. Order Processing
   - Collect necessary info
   - Confirm order
   - Send to human for final approval

4. Escalation
   - Complex issues → human agent
   - Complaints → human agent
   - Urgent matters → human agent

5. Closing
   - Thank you message
   - Follow-up reminder (optional)
```

---

## BAGIAN 7: SKILLS

---

### 27. APA ITU SKILLS?

Skills adalah kemampuan tambahan untuk AI:

```
CONTOH SKILLS:

marketing      → Content creation, social media
github         → Manage repos, issues
weather         → Cek cuaca
healthcheck    → Server security audit
notion         → Notes integration
crypto-news    → Crypto news aggregation
```

---

### 28. INSTALL SKILLS

```bash
# Lihat installed skills
openclaw skills list

# Search skills
openclaw skills search "marketing"

# Install skill
openclaw skills install marketing

# Update all skills
openclaw skills update
```

---

### 29. REKOMENDASI SKILLS

| Skill | Fungsi | Worth |
|-------|--------|-------|
| **marketing** | Content creation | ⭐⭐⭐ |
| **github** | Manage repos | ⭐⭐ |
| **weather** | Cek cuaca | ⭐ |
| **healthcheck** | Server security | ⭐⭐⭐ |
| **notion** | Notes integration | ⭐⭐ |

---

## BAGIAN 8: SECURITY

---

### 30. VPS SECURITY

```bash
# 1. Update regularly
apt update && apt upgrade -y

# 2. Install fail2ban (prevents brute force)
apt install -y fail2ban

# 3. Setup firewall
ufw allow 22    # SSH
ufw allow 80    # HTTP
ufw allow 443   # HTTPS
ufw enable

# 4. Disable root login (advanced)
nano /etc/ssh/sshd_config
# Edit: PermitRootLogin no
systemctl restart sshd
```

---

### 31. API KEY SECURITY

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

---

### 32. CLIENT DATA SECURITY

```
PRINCIPLE: Minimal Access

EMAIL AUTOMATION:
- Use app password (not main password)
- Enable 2FA on email account
- Give only send/read permissions

SOCIAL MEDIA:
- Use platform API tokens
- Read-only when possible
- No full account access
```

---

## BAGIAN 9: BISNIS

---

### 33. BUSINESS MODEL

```
LAYANAN YANG BISA DITAWARKAN:

1. PERSONAL AI ASSISTANT
   - Setup untuk individu
   - Private, personal use
   - Based on needs

2. BUSINESS BOT
   - CS automation
   - Sales automation
   - 24/7 customer service

3. TELEGRAM/WHATSAPP BOT
   - Custom bot untuk business
   - Auto-reply
   - Information retrieval

4. AUTOMATION SERVICES
   - Email automation
   - Social media automation
   - Calendar integration
```

---

### 34. PRICING PACKAGES

| Paket | Harga Setup | Monthly | Include |
|-------|-------------|---------|---------|
| **Basic** | Rp 200rb | Rp 100rb | Telegram/WhatsApp bot, basic AI |
| **Standard** | Rp 400rb | Rp 150rb | + Email integration, FAQ setup |
| **Premium** | Rp 750rb | Rp 250rb | + Multi-platform, advanced automation |

**Note:** Biaya VPS dan AI model ditanggung client terpisah.

---

### 35. CARA GET CLIENTS

```
STRATEGY:

1. PORTFOLIO
   - Buat sample bots
   - Document process
   - Show before/after

2. CHANNEL
   - Twitter/X
   - Discord communities
   - Crypto/Tech groups
   - Local business groups

3. OFFER
   - Free trial (1 minggu)
   - Discount for first 5 clients
   - Testimonial-driven

4. PRICING
   - Start low untuk dapat testimonial
   - Naik harga seiring portfolio grow
```

---

## BAGIAN 10: TROUBLESHOOTING

---

### 36. COMMON ISSUES

| Problem | Solution |
|---------|----------|
| VPS can't connect | Check IP, password, firewall |
| Bot offline | Check PM2 logs, restart |
| WhatsApp disconnected | Re-scan QR code |
| Telegram bot not responding | Check token, authorized chats |
| AI responses slow | Check model, consider faster model |

---

### 37. COMMANDS REFERENCE

```bash
# VPS
ssh root@IP_VPS              # Connect
exit                        # Disconnect

# OpenClaw
openclaw start              # Start
openclaw stop               # Stop
openclaw restart            # Restart
openclaw status            # Check status
openclaw logs             # View logs

# PM2
pm2 list                  # List processes
pm2 logs name --lines 50  # View logs
pm2 restart name          # Restart
pm2 stop name            # Stop

# System
apt update && apt upgrade -y   # Update system
htop                         # Monitor resources
```

---

## 📞 SUPPORT

```
Questions?
Contact: via GitHub Issues atau DM

Found errors atau want to contribute?
Submit PR ke repository
```

---

**© 2026 AI Service Guide**
**Version 2.0**
