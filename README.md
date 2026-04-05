# PANDUAN LENGKAP: AI ASSISTANT & BUSINESS BOT SERVICE
## Dari Nol Menjadi Service Provider

**Version 3.0 | April 2026**

---

## 📑 DAFTAR ISI

### BAGIAN 1: PENDIDIKAN
1. [Apa Itu AI?](#1-apa-itu-ai-basic-understanding)
2. [Apa Itu AI Assistant?](#2-apa-itu-ai-assistant)
3. [Apa Itu Business Bot?](#3-apa-itu-business-bot)
4. [Perbedaan AI Assistant vs Business Bot](#4-perbedaan-ai-assistant-vs-business-bot)
5. [Two Numbers Concept](#5-two-numbers-concept)
6. [Platform yang Didukung](#6-platform-yang-didukung)

### BAGIAN 2: AI CONCEPTS & LEVELS (NEW!)
7. [Jenis-Jenis AI Berdasarkan Kemampuan](#7-jenis-jenis-ai-berdasarkan-kemampuan)
8. [AI Agentic: Apa Itu & Bedanya](#8-ai-agentic-apa-itu--bedanya)
9. [Automation: Levels & Types](#9-automation-apa-itu--levels)
10. [AI + Automation Perspective](#10-ai--automation-perspective)
11. [Service Offering berdasarkan AI Level](#11-service-offerings-berdasarkan-ai-level)
12. [Pricing Reference](#12-pricing-reference)
13. [Future Proofing](#13-future-proofing-trends)
14. [Glossary: AI Terms](#14-glossary-ai-terms)

### BAGIAN 3: VPS & SERVER
15. [Apa Itu VPS?](#15-apa-itu-vps)
16. [Rekomendasi Provider VPS](#16-rekomendasi-provider-vps)
17. [Cara Beli VPS](#17-cara-beli-vps)
18. [SSH: Connect ke VPS](#18-ssh-connect-ke-vps)
19. [Update & Setup Awal Server](#19-update--setup-awal-server)

### BAGIAN 4: INSTALASI
20. [Install Node.js](#20-install-nodejs)
21. [Install OpenClaw](#21-install-openclaw)
22. [Setup Auto-Start (PM2)](#22-setup-auto-start-pm2)
23. [Setup DNS & Web Interface](#23-setup-dns--web-interface)

### BAGIAN 5: CHANNEL SETUP
24. [Setup WhatsApp Gateway](#24-setup-whatsapp-gateway)
25. [Setup Telegram Bot](#25-setup-telegram-bot)
26. [Setup Multiple Bots](#26-setup-multiple-bots)

### BAGIAN 6: AI MODELS
27. [Jenis-Jenis AI Model](#27-jenis-jenis-ai-model)
28. [Perbandingan & Pricing](#28-perbandingan--pricing)
29. [Cara Pilih AI Model](#29-cara-pilih-ai-model)
30. [Setup di OpenClaw](#30-setup-di-openclaw)

### BAGIAN 7: BUSINESS BOT
31. [Konfigurasi Business Bot](#31-konfigurasi-business-bot)
32. [Contoh per Industri](#32-contoh-per-industri)
33. [Personality & Tone](#33-personality--tone)
34. [Knowledge Base](#34-knowledge-base)
35. [Automation Rules](#35-automation-rules)

### BAGIAN 8: SKILLS
36. [Apa Itu Skills?](#36-apa-itu-skills)
37. [Install Skills](#37-install-skills)
38. [Rekomendasi Skills](#38-rekomendasi-skills)

### BAGIAN 9: SECURITY
39. [VPS Security](#39-vps-security)
40. [API Key Security](#40-api-key-security)
41. [Client Data Security](#41-client-data-security)

### BAGIAN 10: BISNIS
42. [Business Model](#42-business-model)
43. [Pricing Packages](#43-pricing-packages)
44. [Cara Get Clients](#44-cara-get-clients)

### BAGIAN 11: TROUBLESHOOTING
45. [Common Issues](#45-common-issues)
46. [Commands Reference](#46-commands-reference)

---

## BAGIAN 1: PENDIDIKAN

---

### 1. APA ITU AI? (Basic Understanding)

```
AI = Artificial Intelligence (Kecerdasan Buatan)

AI adalah computer/sistem yang bisa:
- Understand bahasa manusia
- Generate text/responses
- Make decisions
- Learn dari data
- Solve problems

Tapi AI itu ada LEVELS:
├── Chatbot Sederhana (rule-based)
├── AI Assistant (conversational)
├── AI Agentic (autonomous actions)
├── AGI (human-level intelligence)
└── ASI (beyond human)
```

---

### 2. APA ITU AI ASSISTANT?

AI Assistant adalah AI yang membantumu dalam kegiatan sehari-hari melalui chat.

```
Contoh:
- Kamu chat: "Buatkan email balasan ke client"
- AI jawab: Email lengkap
- Kamu copy paste
```

**Sama seperti chat dengan saya (Aira) sekarang, tapi bisa di-SETUP untuk kebutuhan spesifik.**

---

### 3. APA ITU BUSINESS BOT?

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

### 4. PERBEDAAN AI ASSISTANT VS BUSINESS BOT

| Aspek | AI Assistant | Business Bot |
|-------|-------------|--------------|
| **Pengguna** | Kamu sendiri | Banyak customer |
| **Tujuan** | Productivity personal | CS/Sales Otomatis |
| **Akses** | Private (kamu aja) | Public (siapa aja) |
| **Platform** | WhatsApp/Telegram | WhatsApp/Telegram |
| **Nomor HP** | Utama atau kedua | Kedua (terpisah) |

---

### 5. TWO NUMBERS CONCEPT

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

### 6. PLATFORM YANG DIDUKUNG

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

## BAGIAN 2: AI CONCEPTS & LEVELS

---

### 7. JENIS-JENIS AI BERDASARKAN KEMAMPUAN

#### Level 1: Chatbot Sederhana

```
Kemampuan:
- Respon berdasarkan rules/text yang udah predefined
- Keyword detection
- Fixed responses

Contoh:
- Auto-reply sederhana
- FAQ bot
- Scripted responses

Keterbatasan:
- Gak bisa understand konteks
- Gak bisa learn
- Harus diinput manual setiap response
```

#### Level 2: AI Assistant (yang kita pakai sekarang)

```
Kemampuan:
- Conversational (ngobrol natural)
- Understand context
- Generate responses based on training
- Learn patterns dari data besar

Contoh:
- ChatGPT, Claude, Gemini
- AI Assistant via WhatsApp/Telegram

Keterbatasan:
- Kamu chat → AI respond
- AI gak bisa take actions sendiri
- Butuh prompt dari manusia
```

#### Level 3: AI AGENTIC (Next Level!)

```
Kemampuan:
- Autonomous (bisa bertindak sendiri)
- Plan dan execute tasks
- Use tools (browse web, send emails, dll)
- Make decisions based on goals
- Multi-step reasoning

Bedanya sama AI Assistant:
AI Assistant: "ChatGPT, buatin email"
AI Agentic: "ChatGPT, buatin email DAN KIRIM ke client"

Contoh AI Agentic:
- Auto-reply email + send
- Monitor harga + auto buy
- Research + generate report + send
- Schedule meeting + send invites
```

#### Level 4: AGI (Artificial General Intelligence)

```
Kemampuan:
- Se-intelligent manusia
- Bisa do ANY intellectual task
- Self-aware
- Continual learning
- Transfer learning (apply knowledge from one domain to another)

Status:
- BELUM EXISTS
- Masih theoretical/future
- Mungkin 5-20 tahun lagi
- Banyak company yang bilang "almost AGI" tapi belum

Warning:
- Jangan percaya klaim "AGI" yang udah ada sekarang
- Yang ada sekarang semua masih AI, bukan AGI
```

#### Level 5: ASI (Artificial Superintelligence)

```
Kemampuan:
- Beyond human intelligence
- Self-improving
- Could solve problems manusia gak bisa

Status:
- Purely theoretical
- Science fiction territory
- No timeline
```

---

### 8. AI AGENTIC: APA ITU & BEDANYA

#### Definisi AI Agentic

```
AI AGENTIC = AI yang bisa TAKE ACTIONS sendiri

"Agentic" = ability to act autonomously

AI Biasa:
User: "Bantu belikan iPhone 15"
AI: "Berikut info iPhone 15..."

AI Agentic:
User: "Bantu belikan iPhone 15"
AI: "Oke, saya check harga..."
AI: "Nemukan harga terbaik di Tokopedia"
AI: "Membeli sekarang..."
AI: "Selesai! Order #12345 confirmed"
```

#### Components AI Agentic

```
AI AGENTIC SYSTEM:

1. LLM (Brain)
   ├── Understand user goals
   ├── Generate responses
   └── Make decisions

2. Planning Module
   ├── Break down tasks
   ├── Create steps
   └── Prioritize actions

3. Tools/Function Calling
   ├── Web browsing
   ├── Send emails
   ├── Make purchases
   └── API integrations

4. Memory
   ├── Remember past interactions
   ├── Store context
   └── Learn from feedback

5. Execution
   ├── Take real-world actions
   ├── Interact with external systems
   └── Complete tasks
```

#### AI Agentic vs AI biasa di OpenClaw

```
OPENCLAW SAAT INI:
├── AI Assistant level (conversational)
├── Responds to messages
├── Generate text/responses
├── Use skills (like tools)

OPENCLAW FUTURE (Agentic):
├── Autonomous task completion
├── Multi-step planning
├── Real-world actions
├── Self-initiated workflows
```

---

### 9. AUTOMATION: APA ITU & LEVELS

#### Definisi Automation

```
AUTOMATION = tugas yang execute TANPA manusia intervention

Manual:
User → Click → Send email → Done

Automated:
System → Trigger → Action → Done

Contoh:
- Email auto-reply (otomatis respond)
- Scheduled posts (posting tanpa human)
- Auto-save files (save tanpa click)
- Trading bots (buy/sell otomatis)
```

#### Levels of Automation

```
LEVEL 1: RULE-BASED (Basic)
├── IFTTT-style automation
├── If this → Then that
├── No AI involved
├── Example:
   If price drops below $100 → Send alert

LEVEL 2: AI-ENHANCED (Current)
├── AI assists automation
├── Smart decisions based on context
├── Example:
   If customer asks "harga?" → AI generates response

LEVEL 3: AI AGENTIC (Advanced)
├── AI plans AND executes
├── Autonomous decision making
├── Example:
   If price drops + volume spikes → AI buys + monitors + sells

LEVEL 4: FULL AUTONOMY (Future)
├── Human sets goals only
├── AI handles everything else
├── Minimal human oversight
├── Example:
   "Maximize my portfolio" → AI does everything
```

---

### 10. AI + AUTOMATION: SERVICE OFFERINGS

#### Tier 1: AI Assistant (Basic)

```
Description:
- Conversational interface
- Personal or business use
- Responds to queries
- Information retrieval

Use Cases:
- Personal productivity
- Basic customer service
- Information answering
- Drafting assistance

Setup Complexity: Easy
Cost: Low
AI Level: Assistant
```

#### Tier 2: AI Automation (Intermediate)

```
Description:
- Rule-based workflows
- Automated responses
- Scheduled tasks
- Multi-step sequences

Use Cases:
- Email automation
- Social media scheduling
- Auto-responders
- Data processing

Setup Complexity: Medium
Cost: Medium
AI Level: AI + Rules
```

#### Tier 3: AI Agentic (Advanced)

```
Description:
- Autonomous task completion
- Multi-step planning
- Tool use
- Self-initiated actions

Use Cases:
- Autonomous trading
- Research agents
- Personal secretary
- Complex automation

Setup Complexity: High
Cost: High
AI Level: Agentic (emerging)
```

---

### 11. PRICING REFERENCE BERDASARKAN COMPLEXITY

| Tier | Description | Setup | Monthly | Time to Build |
|-------|-------------|-------|---------|---------------|
| **Basic** | AI Assistant personal | Rp 200-400rb | Rp 100rb | 1-2 hours |
| **Standard** | Business automation | Rp 500rb-1jt | Rp 150-250rb | 2-5 hours |
| **Premium** | AI Agentic | Rp 1.5-3jt | Rp 300-500rb | 5-20 hours |
| **Enterprise** | Custom solution | Rp 5jt+ | Negotiable | Weeks |

**Note:** Monthly = maintenance/support, VPS + AI API costs excluded.

---

### 12. FUTURE PROOFING: TRENDS TO WATCH

```
EMERGING TRENDS (2026):

1. AI Agentic Features
   - More tools integration
   - Better autonomous actions
   - Multi-modal capabilities

2. Better Reasoning
   - Improved logical thinking
   - Better problem-solving
   - More accurate responses

3. Lower Costs
   - AI models getting cheaper
   - More competition
   - Better efficiency

4. Easier Setup
   - No-code platforms
   - Pre-built templates
   - Faster deployment

5. Regulation
   - More AI governance
   - Privacy concerns
   - Compliance needs
```

---

### 13. GLOSSARY: AI TERMS

```
AI = Artificial Intelligence (Kecerdasan Buatan)
LLM = Large Language Model (GPT, Claude, Gemini)
AGI = Artificial General Intelligence (AI se-human)
ASI = Artificial Superintelligence (AI beyond human)
Agentic = AI yang bisa take actions sendiri
Automation = Tugas yang execute otomatis
Prompt = Instruksi ke AI
Token = Unit text yang diproses AI (1 word ~ 1.3 tokens)
API = Application Programming Interface
Chatbot = Program yang chat secara otomatis
```

---

## BAGIAN 3: VPS & SERVER

---

### 15. APA ITU VPS?

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

### 16. REKOMENDASI PROVIDER VPS

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

### 17. CARA BELI VPS (DigitalOcean)

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

---

### 18. SSH: CONNECT KE VPS

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

---

### 19. UPDATE & SETUP AWAL SERVER

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

## BAGIAN 4: INSTALASI

---

### 20. INSTALL NODE.JS

```bash
# Install Node.js 18.x
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

# Verify
node --version
npm --version
```

---

### 21. INSTALL OPENCLAW

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

### 22. SETUP AUTO-START (PM2)

```bash
# Install PM2
npm install -g pm2

# Start OpenClaw dengan PM2
pm2 start openclaw --name openclaw

# Setup auto-start saat server reboot
pm2 startup
pm2 save
```

---

### 23. SETUP DNS & WEB INTERFACE

```bash
# Install Nginx
apt install -y nginx

# Configure
nano /etc/nginx/sites-available/default
```

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

---

## BAGIAN 5: CHANNEL SETUP

---

### 24. SETUP WHATSAPP GATEWAY

```
1. Buka dashboard OpenClaw: http://IP_VPS:18789
2. Navigate ke: Settings > Channels > WhatsApp
3. Klik "Enable"
4. Scan QR Code dengan nomor yang mau dipakai
5. WhatsApp connected!
```

---

### 25. SETUP TELEGRAM BOT

#### Step 1: Buat Bot di Telegram

```
1. Buka Telegram
2. Search: @BotFather
3. Klik "Start"
4. Ketik: /newbot
5. Beri Nama Bot: (contoh: "AI Assistant Fajar")
6. Beri Username: (contoh: fajar_ai_bot)
7. BotFather kasih TOKEN: 123456789:ABCdefGHIjklMNOpqrsTUVwxyz123456
```

#### Step 2: Configure di OpenClaw

```
1. Buka dashboard OpenClaw
2. Navigate ke: Settings > Channels > Telegram
3. Masukkan TOKEN dari BotFather
4. Klik "Enable"
```

---

### 26. SETUP MULTIPLE BOTS

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

---

## BAGIAN 6: AI MODELS

---

### 27. JENIS-JENIS AI MODEL

| Tipe | Fungsi | Contoh |
|------|--------|---------|
| **LLM** | Text generation, conversation | GPT-4, Claude, Gemini |
| **Vision** | Image analysis | GPT-4V, Claude Vision |
| **Audio** | Speech to text, TTS | Whisper, ElevenLabs |
| **Multimodal** | Text + Image + Audio | GPT-4o, Gemini Pro |

| Provider | Models | Harga |
|----------|--------|-------|
| **OpenAI** | GPT-4o, GPT-4o Mini, GPT-3.5 | 💰💰-💰💰💰 |
| **Anthropic** | Claude 3.5 Sonnet, Claude 3 Haiku | 💰💰-💰💰💰 |
| **Google** | Gemini 2.0 Flash, Gemini 1.5 Pro | 💰-💰💰 |
| **MiniMax** | MiniMax M2.7, MiniMax M2 | 💰 |
| **Meta (Open Source)** | Llama 3.1, Qwen 2.5, DeepSeek | FREE* |

*Free jika self-host, tapi butuh VPS powerful (RAM 64GB+)

---

### 28. PERBANDINGAN & PRICING

| Model | Input | Output | Context Window |
|-------|-------|--------|----------------|
| GPT-4o | $2.50/1M | $10.00/1M | 128K |
| GPT-4o Mini | $0.15/1M | $0.60/1M | 128K |
| Claude 3.5 Sonnet | $3.00/1M | $15.00/1M | 200K |
| Claude 3 Haiku | $0.25/1M | $1.25/1M | 200K |
| Gemini 2.0 Flash | $0.10/1M | $0.40/1M | 1M |
| Gemini 1.5 Flash | $0.075/1M | $0.30/1M | 128K |
| MiniMax M2.7 | $0.20/1M | $0.70/1M | 32K |

---

### 29. CARA PILIH AI MODEL

| Budget | Model Pilihan | Cocok Untuk |
|--------|---------------|-------------|
| **Free** | Llama 3.1 (self-host) | Tech-savvy, privacy |
| **$1-5/bulan** | Gemini Flash, MiniMax M2 | Simple bots |
| **$5-15/bulan** | GPT-4o Mini, Claude Haiku | General purpose |
| **$15-50/bulan** | GPT-4o, Claude 3.5 Sonnet | Premium tasks |

---

### 30. SETUP DI OPENCLAW

```javascript
{
  "ai": {
    "model": "minimax/MiniMax-M2.7"  // Default
  }
}
```

---

## BAGIAN 7: BUSINESS BOT

---

### 31. KONFIGURASI BUSINESS BOT

```javascript
{
  "business": {
    "name": "Nama Toko Bot",
    "industry": "E-commerce",
    "personality": {
      "role": "Customer Service",
      "tone": "Friendly, professional",
      "language": "Bahasa Indonesia"
    },
    "knowledge": {
      "products": ["List produk"],
      "prices": {"Produk": "Harga"},
      "faq": ["Pertanyaan umum"]
    },
    "rules": [
      "Selalu sopan",
      "Escalate ke manusia untuk komplain besar"
    ]
  }
}
```

---

### 32. CONTOH PER INDUSTRI

**Restaurant:**
```javascript
{
  "menu": [
    {"name": "Nasi Goreng", "price": "Rp 25.000"},
    {"name": "Mie Goreng", "price": "Rp 23.000"}
  ],
  "hours": "10 pagi - 10 malam",
  "location": "Jl. Merdeka No. 123, Jakarta"
}
```

**E-commerce:**
```javascript
{
  "categories": ["HP", "Laptop", "Aksesoris"],
  "brands": ["Apple", "Samsung", "Xiaomi"],
  "warranty": "1 tahun resmi",
  "paymentMethods": ["Transfer", "COD", "Midtrans"]
}
```

---

### 33. PERSONALITY & TONE

| Role | Tone | Contoh |
|------|------|--------|
| **Casual Shop** | Friendly, casual | "Halo! Mau cari apa nih?" |
| **Premium Brand** | Professional, formal | "Selamat datang. Ada yang bisa saya bantu?" |
| **Tech Support** | Technical, patient | "Saya pahami issue-nya. Mari kita check." |

---

### 34. KNOWLEDGE BASE

```
KNOWLEDGE BASE TERDIRI DARI:

1. PRODUCTS/SERVICES
2. PRICING
3. FAQ
4. POLICIES
```

---

### 35. AUTOMATION RULES

```
RULES UNTUK BUSINESS BOT:

1. Greeting - Auto-reply untuk salam
2. FAQ Handling - Instant untuk pertanyaan umum
3. Order Processing - Collect info, confirm order
4. Escalation - Complex issues → human agent
5. Closing - Thank you message
```

---

## BAGIAN 8: SKILLS

---

### 36. APA ITU SKILLS?

Skills adalah kemampuan tambahan untuk AI.

```
CONTOH:
- marketing - Content creation
- github - Manage repos
- weather - Cek cuaca
- healthcheck - Server security
```

---

### 37. INSTALL SKILLS

```bash
# Lihat skills
openclaw skills list

# Install skill
openclaw skills install marketing

# Update
openclaw skills update
```

---

### 38. REKOMENDASI SKILLS

| Skill | Fungsi | Worth |
|-------|--------|-------|
| **marketing** | Content creation | ⭐⭐⭐ |
| **github** | Manage repos | ⭐⭐ |
| **weather** | Cek cuaca | ⭐ |
| **healthcheck** | Server security | ⭐⭐⭐ |

---

## BAGIAN 9: SECURITY

---

### 39. VPS SECURITY

```bash
# Update regularly
apt update && apt upgrade -y

# Install fail2ban
apt install -y fail2ban

# Setup firewall
ufw allow 22
ufw allow 80
ufw allow 443
ufw enable
```

---

### 40. API KEY SECURITY

```
DO:
✅ Use API keys with limited permissions
✅ Store in environment variables
✅ Rotate keys periodically

DON'T:
❌ Share keys in plain text
❌ Commit keys to git
```

---

### 41. CLIENT DATA SECURITY

```
PRINCIPLE: Minimal Access

EMAIL:
- Use app password (not main password)
- Enable 2FA

SOCIAL MEDIA:
- Use platform API tokens
- Read-only when possible
```

---

## BAGIAN 10: BISNIS

---

### 42. BUSINESS MODEL

```
LAYANAN YANG BISA DITAWARKAN:

1. PERSONAL AI ASSISTANT
2. BUSINESS BOT (CS Automation)
3. TELEGRAM/WHATSAPP BOT
4. AUTOMATION SERVICES
```

---

### 43. PRICING PACKAGES

| Paket | Setup | Monthly | Include |
|-------|-------|---------|---------|
| **Basic** | Rp 200rb | Rp 100rb | Telegram/WhatsApp, basic AI |
| **Standard** | Rp 400rb | Rp 150rb | + Email integration, FAQ |
| **Premium** | Rp 750rb | Rp 250rb | + Multi-platform, advanced |

---

### 44. CARA GET CLIENTS

```
STRATEGY:

1. PORTFOLIO - Buat sample bots
2. CHANNEL - Twitter, Discord, groups
3. OFFER - Free trial untuk first clients
4. PRICING - Start low, naik seiring portfolio
```

---

## BAGIAN 11: TROUBLESHOOTING

---

### 45. COMMON ISSUES

| Problem | Solution |
|---------|----------|
| VPS can't connect | Check IP, password, firewall |
| Bot offline | Check PM2 logs, restart |
| WhatsApp disconnected | Re-scan QR |
| Telegram not responding | Check token, chats |

---

### 46. COMMANDS REFERENCE

```bash
# VPS
ssh root@IP_VPS
exit

# OpenClaw
openclaw start/stop/restart
openclaw status
openclaw logs

# PM2
pm2 list
pm2 logs name --lines 50
pm2 restart name

# System
apt update && apt upgrade -y
htop
```

---

## 📞 SUPPORT

```
Questions?
Via GitHub Issues atau DM
```

---

**© 2026 AI Service Guide**
**Version 3.0**
