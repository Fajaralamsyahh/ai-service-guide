# AI POWER AUTOMATION SERVICE
## Panduan Lengkap dari Nol Menjadi AI Service Provider

**Version 5.0 | April 2026**
**By: Aira ⚡ (AI Assistant)**

---

# 📋 DAFTAR ISI

## BAGIAN A: PENGENALAN (untuk pemula yang belum tahu apa-apa)
- [A1. Apa Itu AI?](#a1-apa-itu-ai)
- [A2. Level AI: AI Biasa vs AI Agentic vs AGI vs ASI](#a2-level-ai)
- [A3. Perbedaan AI Assistant, AI untuk Business, AI Agentic](#a3-perbedaan-jenis-ai)
- [A4. Istilah-Istilah Penting dalam AI](#a4-istilah-penting)

## BAGIAN B: TOOLS & INFRASTRUKTUR
- [B1. Apa Saja yang Dibutuhkan](#b1-tools-yang-dibutuhkan)
- [B2. VPS (Virtual Private Server)](#b2-vps)
- [B3. AI Model (Otak AI)](#b3-ai-model)
- [B4. OpenClaw (Platform Utama)](#b4-openclaw)
- [B5. Channel: WhatsApp & Telegram](#b5-channel-whatsapp-telegram)

## BAGIAN C: BUDGET & BIAYA
- [C1. Budget untuk Client (Yang Pakai Bot)](#c1-budget-untuk-client)
- [C2. Budget untuk Service Provider (Yang Bikinin Bot)](#c2-budget-untuk-provider)
- [C3. Detail Biaya AI Model per Bulan](#c3-biaya-ai-model)
- [C4. Tabel Ringkasan Semua Biaya](#c4-tabel-ringkesan-biaya)

## BAGIAN D: SETUP DARI 0 - DI LAPTOP
- [D1. Setup VPS (Server)](#d1-beli-dan-setup-vps)
- [D2. Connect ke VPS dari Windows](#d2-connect-vps-dari-windows)
- [D3. Connect ke VPS dari Mac/Linux](#d3-connect-vps-dari-maclinux)
- [D4. Install OpenClaw di VPS](#d4-install-openclaw)
- [D5. Setup Auto-Start dengan PM2](#d5-setup-auto-start)
- [D6. Verifikasi Bot Berjalan](#d6-verifikasi-bot)

## BAGIAN E: SETUP DARI 0 - DI HP
- [E1. Connect ke VPS dari Android](#e1-connect-vps-dari-android)
- [E2. Connect ke VPS dari iPhone](#e2-connect-vps-dari-iphone)
- [E3. Manage Bot dari HP](#e3-manage-bot-dari-hp)

## BAGIAN F: CHANNEL SETUP
- [F1. Setup WhatsApp Gateway](#f1-setup-whatsapp)
- [F2. Setup Telegram Bot](#f2-setup-telegram)
- [F3. Setup Multiple Bot untuk Multiple Client](#f3-setup-multiple-bot)

## BAGIAN G: AI MODEL SETUP
- [G1. Cara Pilih AI Model](#g1-pilih-ai-model)
- [G2. Perbandingan AI Model](#g2-perbandingan-ai-model)
- [G3. Setup API Key AI Model](#g3-setup-api-key)
- [G4. Konfigurasi Model di OpenClaw](#g4-konfigurasi-model)

## BAGIAN H: KONFIGURASI BOT
- [H1. Setup AI Assistant Personal](#h1-setup-ai-assistant)
- [H2. Setup Business Bot (CS Bot)](#h2-setup-business-bot)
- [H3. Setup Automation (Cron/Scheduled Tasks)](#h3-setup-automation)
- [H4. Setup AI Agentic (Auto Actions)](#h4-setup-agentic)

## BAGIAN I: CONTOH REAL
- [I1. Contoh: E-commerce Fashion](#i1-contoh-ecommerce)
- [I2. Contoh: Restaurant/Warteg](#i2-contoh-restaurant)
- [I3. Contoh: Freelance Service](#i3-contoh-freelance)
- [I4. Contoh: Crypto Trading Bot](#i4-contoh-crypto)
- [I5. Contoh: Personal Assistant](#i5-contoh-personal-assistant)

## BAGIAN J: SERVICE & PRICING
- [J1. Paket Service untuk Client](#j1-paket-service)
- [J2. Contoh Quotation Lengkap](#j2-contoh-quotation)
- [J3. Cara Get Clients](#j3-cara-get-clients)
- [J4. Strategy Pricing](#j4-pricing-strategy)

## BAGIAN K: TROUBLESHOOTING & SECURITY
- [K1. Common Issues & Solutions](#k1-troubleshooting)
- [K2. VPS Security Best Practices](#k2-security)
- [K3. API Key Security](#k3-api-security)
- [K4. Commands Reference](#k4-commands-reference)

---

# BAGIAN A: PENGENALAN

---

## A1. APA ITU AI?

### Definisi Singkat

**AI = Artificial Intelligence (Kecerdasan Buatan)**

Sederhananya: Komputer yang bisa "berpikir", "bicara", dan "bertindak" seperti manusia.

### Dalam Konteks Bot/Service

Ketika kita ngomongin "AI Bot", yang kita maksud adalah:

```
AI Bot = Software yang bisa:
1. Terima pesan (dari WhatsApp, Telegram, dll)
2. Pahami maksud pesan
3. Generate response yang sesuai
4. Lakukan aksi tertentu (jika needed)
```

### Analogi Sederhana

```
AI Bot itu kayak:

Kamu punya assistant (manusia) yang:
- Duduk di belakang meja
- Terima pertanyaan dari client
- Jawab berdasarkan pengetahuan dia
- Bisa bertindak sesuai instruksi

AI Bot ituassistant-nya yang BONAFIT:
- Kerja 24/7 tanpa capek
- Gak perlu gaji
- Gak perlu training ulang
- Bisa handle banyak client sekaligus
```

---

## A2. LEVEL AI

AI punya tingkatan. Mulai dari yang paling sederhana sampai yang masih theoretical.

### Level 1: AI Biasa (Narrow AI / Weak AI)

```
Apa itu: AI yang jago SATU hal saja

Contoh yang ada sekarang:
- ChatGPT (jago generate text)
- AlphaFold (jago fold protein)
- Tesla Autopilot (jago nyupir)

Ciri-ciri:
✅ SANGAT jago di 1 bidang
❌ Gak bisa generalize ke bidang lain
❌ Gak punya "consciousness"
❌ Gak bisa "think" seperti manusia
```

### Level 2: AI Agentic (Agentic AI)

```
Apa itu: AI yang bisa AMBIL TINDAKAN sendiri

Bedanya dari AI Biasa:

AI Biasa:
User: "ChatGPT, buatin email ke client"
AI: *kasih draft email*
(USER yang harus copy-paste dan send manual)

AI Agentic:
User: "ChatGPT, handle email dari client"
AI: *baca inbox* → *generate response* → *send email* → *confirm ke user*
(SEMUA OTOMATIS, user cuma supervise)

Kemampuan:
✅ Bisa bikin plan (rencana langkah2)
✅ Bisa execute (lakuin tindakan)
✅ Bisa use tools (browse web, send email, dll)
✅ Bisa multi-step reasoning
✅ Bisa loop (ulangin langkah sampai selesai)

Status April 2026: SUDAH ADA tapi masih "light" version
- OpenAI GPT-4 with Tools
- Anthropic Claude with Tools
- OpenClaw (yang lo pake sekarang)
```

### Level 3: AGI (Artificial General Intelligence)

```
Apa itu: AI se-pintar manusia di SEMUA bidang

Artinya:
✅ Bisa doing ANY intellectual task yang manusia bisa
✅ Bisa belajar skill baru sendiri
✅ Bisa apply knowledge across domains
✅ Bisa self-improve
✅ Gak ada limitasi seperti AI sekarang

STATUS: BELUM ADA (per April 2026)
- Semua yang bilang "AGI sudah ada" = MARKETING HYPE
- Reality: masih AI biasa / AI agentic yang limited
- Estimasi para expert: 5-20 tahun lagi (kalau bisa)
```

### Level 4: ASI (Artificial Superintelligence)

```
Apa itu: AI yang LEBIH PINTAR dari manusia di semua hal

Artinya:
✅ Lebih pintar dari Einstein + semua scientist digabung
✅ Bisa solve problems yang manusia gak mampu
✅ Self-improving (terus jadi lebih pintar sendiri)
✅ Could threatens human existence (ini concern banyak orang)

STATUS: MASIH THEORETICAL ONLY
- Gak ada timeline yang jelas
- More like science fiction saat ini
- Banyak expert concerned about this
```

### Ringkasan Level AI

| Level | Nama | Status 2026 | Contoh |
|-------|------|-------------|--------|
| 1 | AI Biasa (Narrow AI) | ✅ ADA | ChatGPT, Gemini, Claude |
| 2 | AI Agentic | ✅ ADA (light) | GPT-4+Tools, OpenClaw |
| 3 | AGI | ❌ BELUM ADA | - |
| 4 | ASI | ❌ THEORETICAL | - |

---

## A3. PERBEDAAN JENIS AI

### 1. AI ASSISTANT (Personal AI)

```
Untuk: Kamu sendiri / personal use
Tujuan: Membantu pekerjaan & kebutuhan personal
Contoh penggunaan:
- "Buatin email ke client"
- "Rangkum artikel panjang 50 halaman"
- "Cari info soal crypto"
- "Bantu coding script"
- "Draft proposal bisnis"
- "Jelaskan topik сложный"

Ciri-ciri:
🔒 PRIVATE - cuma kamu yang pake
🎭 PERSONALIZED - sesuai gaya & preferensi kamu
📁 SECURE - data personal aman
👤 SINGLE USER - untuk 1 orang
```

### 2. AI UNTUK BUSINESS (Business Bot / CS Bot)

```
Untuk: Customer / Client bisnis
Tujuan: Customer Service Otomatis, Sales, Automation
Contoh penggunaan:
- Auto-reply pertanyaan harga produk
- Info stock &ETA pengiriman
- Booking appointment
- Handle complaints
- Generate quotes
- Follow-up customer

Ciri-ciri:
🌐 PUBLIC - siapa aja bisa chat
🏢 PROFESSIONAL - sesuai brand bisnis
📈 SCALABLE - bisa handle unlimited customer
⏰ 24/7 - nyala terus tanpa off
🔄 CONSISTENT - jawaban standard sama
```

### 3. AI AGENTIC (Autonomous AI)

```
Untuk: Automating complex workflows
Tujuan: HAPUS manual work sepenuhnya
Contoh penggunaan:
- Auto-reply email + follow-up
- Research + report generation + delivery
- Social media posting + monitoring + engagement
- Trading (buy/sell based on signals)
- Appointment scheduling + reminders + confirmations

Bedanya dari Business Bot:

Business Bot:
- User tanya → Bot jawab
- Tiap langkah butuh trigger dari user

AI Agentic:
- User kasih GOAL → Bot eksekusi semua langkah
- Bot autonomously takes actions
- User cuma receive confirmation/result
```

### Tabel Perbandingan

| Aspek | AI Personal | AI Business | AI Agentic |
|-------|-------------|-------------|-------------|
| **Pengguna** | 1 orang (kamu) | Banyak customer | 1 orang atau banyak |
| **Akses** | Private | Public | Private atau Public |
| **Trigger** | User chat | User chat | User give goal |
| **Actions** | Jawab saja | Jawab saja | Execute semua langkah |
| **Complexity** | Simpel | Medium | High |
| **Setup** | Basic | Medium | Advanced |
| **Maintenance** | Low | Ongoing | Medium-High |

---

## A4. ISTILAH PENTING

### Tokens

```
Apa itu: Unit terkecil dari text yang diproses AI

Analoginya:
- 1 token ≈ 1 kata (untuk bahasa Inggris)
- 1 token ≈ 1-2 karakter (untuk Bahasa Indonesia)

Contoh:
"Hello world" = 2 tokens
"Halo dunia" = 4-5 tokens (karena karakter per karakter)

Kenapa penting:
- AI model dijual per 1 juta tokens
- Makin banyak text = makin mahal
- Context window = max tokens yang bisa diproses sekaligus
```

### Context Window

```
Apa itu: "Memori" AI untuk 1 conversation

Contoh:
- MiniMax M2.7: 32K tokens (32.000 tokens)
- GPT-4o Mini: 128K tokens
- Claude 3.5 Sonnet: 200K tokens

Artinya:
- Context 32K = bisa hold ~20-30 halaman text sekaligus
- Lewat dari itu = AI "lupa" yang awal

Kenapa penting:
- Conversation panjang = perlu context besar
- Budget = context besar = mahal
```

### API

```
Apa itu: Application Programming Interface

Sederhananya: "Jembatan" untuk ngobrolin software

Contoh:
AI Model API:
- Software lo → kirim pesan → AI Model → dapat response
- Lewat APIendpoint (URL khusus)

OpenClaw itu MEMANG AI Gateway yang pake API
- Lo bicara ke OpenClaw (via WhatsApp/Telegram)
- OpenClaw ngomong ke AI Model (via API)
- AI Model jawab → OpenClaw balikin ke lo
```

### VPS (Virtual Private Server)

```
Apa itu: Komputer远程 (di cloud) yang nyala 24/7

Bedanya dari komputer biasa:

Komputer biasa:
- Nyala kalau lo nyalain
- Lo pegang langsung
- Kalo mati = lo harus restart manual

VPS:
- Nyala 24/7 (karena di data center)
- Diakses dari jauh (remote)
- Kalo mati = auto-restart (kalau dikonfigur)

Gunanya untuk bot:
- Bot butuh komputer yang nyala terus
- VPS = komputer "always-on" di cloud
- Lo akses dari mana aja
```

### PM2 (Process Manager)

```
Apa itu: Software untuk manage Node.js apps

Gunanya:
- Bot jalan otomatis pas server boot
- Bot auto-restart kalau crash
- Monitor bot status

Bedanya tanpa PM2:
- Server reboot = bot mati = lo harus start manual
- Bot crash = mati = lo harus start manual

Dengan PM2:
- Server reboot = bot auto-start
- Bot crash = auto-restart
- Lo tidur nyenyak 😴
```

### OpenClaw

```
Apa itu: Platform AI Gateway (yang lo pake sekarang)

Fungsinya:
- Hubungin AI Model dengan Channel (WhatsApp/Telegram)
- Manage conversation
- Handle plugins & skills
- Running 24/7 di VPS

Kenapa pake OpenClaw:
✅ Gak perlu coding dari 0
✅ Setup easy (1-2 jam)
✅ Support banyak channel
✅ Support banyak AI model
✅ Open source & community-driven
```

### Skills

```
Apa itu: Kemampuan tambahan untuk AI

Contoh:
- Weather skill: Bisa cek cuaca
- GitHub skill: Bisa manage repo
- Marketing skill: Bikin konten
- Healthcheck skill: Security audit

Bedanya sama basic AI:
- Basic AI: Jawab pertanyaan umum
- Skills: Bisa LAKUKAN sesuatu yang spesifik
```

---

# BAGIAN B: TOOLS & INFRASTRUKTUR

---

## B1. TOOLS YANG DIBUTUHKAN

### Untuk Client (Yang Akan Pakai AI Bot)

```
DIBUTUHKAN:

1. Nomor HP (untuk WhatsApp - OPSIONAL)
   - Utama atau kedua
   - Bisa second SIM / eSIM / virtual number
   - CATATAN: 1 nomor = 1 WhatsApp Bot

2. VPS (WAJIB)
   - Sewa server di cloud
   - Buat running bot 24/7
   - Harga: Rp 50.000 - 150.000/bulan

3. AI Model API Key (WAJIB)
   - "Otak" dari AI-nya
   - Ada yang FREE (MiniMax, Gemini Flash)
   - Ada yang PAID ($5-50/bulan)
```

### Untuk Service Provider (Yang Bikinin Bot)

```
DIBUTUHKAN:

1. Laptop atau HP
   - Buat remote ke VPS
   - Install & configure

2. SSH Client
   - Windows: PuTTY / Windows Terminal / Termius
   - Mac: Terminal (built-in)
   - Android: Termius / JuiceSSH
   - iPhone: Termius / ShellFire

3. Akun Cloud Provider (VPS)
   - DigitalOcean / Vultr / Linode / Hetzner
   - Credit card atau payment method

4. Akun AI Provider (API Key)
   - MiniMax (free tier ada)
   - OpenAI (free tier ada)
   - Google AI (free tier ada)

5. Knowledge & Waktu
   - Belajar: Dari panduan ini + practice
   - Waktu setup: 2-5 jam per project
```

### Ringkasan Tools

| Tool | Untuk | Harga | Wajib? |
|------|-------|-------|--------|
| VPS | Running bot 24/7 | Rp 50-150k/bulan | ✅ WAJIB |
| AI Model API | Otak AI | Free - Rp 500k/bulan | ✅ WAJIB |
| SSH Client | Remote access | Free | ✅ WAJIB |
| WhatsApp Number | Channel | Free - varies | ⚡ Opsional |
| Domain | Web interface | Rp 50-150k/tahun | ❌ Optional |

---

## B2. VPS (VIRTUAL PRIVATE SERVER)

### Apa Itu VPS?

```
VPS = Virtual Private Server

Analogi:
VPS itu kayak... apartemen di hotel
- Hotel = Data Center (selalu nyala, internet cepat)
- Apartemen = VPS lo (space sendiri,的配置)
- Lo bisa akses dari mana aja
- Portier = SSH (lo connect remote)

VS Komputer Biasa:
- Komputer lo = Rumah sendiri (mati kalau mati)
- VPS = Apartemen hotel (selalu nyala)
```

### Rekomendasi VPS Provider

| Provider | Harga/Bulan | Spec | Lokasi | Link |
|----------|-------------|------|--------|------|
| **DigitalOcean** | Rp 60.000 | 1 vCPU, 1GB RAM | Singapore | digitalocean.com |
| **Vultr** | Rp 70.000 | 1 vCPU, 1GB RAM | Singapore | vultr.com |
| **Linode** | Rp 60.000 | 1 vCPU, 2GB RAM | Singapore | linode.com |
| **Hetzner** | Rp 50.000 | 2 vCPU, 4GB RAM | Finland | hetzner.com |
| **AWS Lightsail** | Rp 70.000 | 1 vCPU, 1GB RAM | Singapore | aws.amazon.com |

### Rekomendasi Untuk AI Bot

```
SPESIFIKASI MINIMAL:
- 1 vCPU
- 1 GB RAM
- 25 GB SSD
- 1 TB bandwidth

CUKUP UNTUK:
- 1-3 bots running
- 50-100 conversations/day
- Light automation tasks

JIKA LEBIH BANYAK:
- 2+ bots → upgrade ke 2GB RAM
- 500+ conversations → upgrade ke 2 vCPU
- Heavy processing → consider dedicated GPU nodes
```

### Cara Beli VPS (Step-by-Step)

#### Step 1: Sign Up

```
1. Buka https://digitalocean.com
2. Klik "Sign Up"
3. Masukkan email & password
4. Verifikasi email
5. Login
```

#### Step 2: Tambah Payment Method

```
1. Klik "Billing" di sidebar
2. Klik "Add credit card"
3. Masukkan data kartu
4.一些小优惠: bisa pake prepaid card juga

CATATAN: 
- Minimal top-up $5 untuk verification
- Accepts: Visa, Mastercard, PayPal
```

#### Step 3: Create Droplet (VPS)

```
1. Klik "Create" → "Droplets"
2.pilihan:
   
   Regions: Singapore (paling dekat & cepat)
   
   OS: Ubuntu 22.04 LTS (recommended)
        atau Ubuntu 24.04 LTS (newer)
   
   Plan: Regular
         - $6/month = cukup untuk mulai
         - $12/month = jika perlu lebih spec
   
   Authentication: Password (simplest)
                  atau SSH Key (more secure, optional)
   
   Additional Options:
   - ☑️ Monitoring (gratis, bagus untuk lihat resource)
   - ☑️ VPC Network (default)
   
   Finalize:
   - Pilih quantity: 1
   - Hostname: openclaw-server (atau apa aja)

3. Klik "Create Droplet"
4. Tunggu 1-2 menit
5. Dapat email dengan:
   - IP Address: contoh 143.198.xx.xx
   - Username: root
   - Password: xxxxxxxx (kalau pilih password auth)
```

---

## B3. AI MODEL (OTAK AI)

### Apa Itu AI Model?

```
AI Model = "Otak" dari AI system

Analogi:

Lo = Body (hardware)
Otak = AI Model (software)

Sama kayak manusia:
- Body sama, otak beda → behavior beda
- body gede, otak kecil → limited
- body kecil, otak gede → bisa accomplish banyak

AI Model itu sama:
- Same platform (OpenClaw), beda model → response beda
- Model advanced → response lebih smart
- Model cheap → response lebih basic
```

### Jenis AI Model

```
1. TEXT GENERATION (yang kita pake)
   - Generate text / nulis
   - Semua AI chat biasa

2. IMAGE GENERATION  
   - Generate gambar
   - Midjourney, DALL-E, Stable Diffusion

3. AUDIO GENERATION
   - Generate suara / music
   - ElevenLabs, AudioLDM

4. MULTIMODAL
   - Bisa text + image + audio
   - GPT-4o, Gemini 1.5

UNTUK BOT: kita fokus TEXT GENERATION
```

### AI Model Providers

#### Free Tier (Mulai dari $0)

```
1. MiniMax (yang lo pake sekarang)
   - Input: $0.20/1M tokens
   - Output: $0.70/1M tokens
   - Free credit: ~$5
   - Context: 32K tokens
   - Speed: ⚡⚡⚡⚡ (FAST)
   - Website: minimax.io

2. Google Gemini 1.5 Flash
   - Input: $0.075/1M tokens
   - Output: $0.40/1M tokens
   - Free tier: 1.5M tokens/bulan
   - Context: 1M tokens ( HUGE!)
   - Speed: ⚡⚡⚡⚡
   - Website: aistudio.google.com

3. OpenAI GPT-3.5 Turbo
   - Input: $0.50/1M tokens
   - Output: $2.00/1M tokens
   - Free tier: $5 credit
   - Context: 16K tokens
   - Speed: ⚡⚡⚡⚡⚡
   - Website: openai.com
```

#### Paid Tier ($5-50/bulan)

```
1. OpenAI GPT-4o Mini ⭐ RECOMMENDED
   - Input: $0.15/1M tokens
   - Output: $0.60/1M tokens
   - Context: 128K tokens
   - Speed: ⚡⚡⚡⚡
   - Best value for most use cases

2. Anthropic Claude 3.5 Haiku
   - Input: $0.25/1M tokens
   - Output: $1.25/1M tokens
   - Context: 200K tokens
   - Speed: ⚡⚡⚡ ( slightly slower)
   - Excellent for coding & writing

3. Google Gemini 1.5 Pro
   - Input: $1.25/1M tokens
   - Output: $5.00/1M tokens
   - Context: 1M tokens
   - Speed: ⚡⚡⚡
   - Best for very long context needs
```

#### Premium ($50+/bulan)

```
1. OpenAI GPT-4o
   - Input: $2.50/1M tokens
   - Output: $10.00/1M tokens
   - Context: 128K tokens
   - Speed: ⚡⚡⚡
   - Best quality for complex tasks

2. Anthropic Claude 3.5 Sonnet
   - Input: $3.00/1M tokens
   - Output: $15.00/1M tokens
   - Context: 200K tokens
   - Speed: ⚡⚡
   - Top tier for coding & analysis
```

### Tabel Perbandingan Lengkap

| Model | Provider | Input$/1M | Output$/1M | Context | Speed | Best For |
|-------|----------|-----------|------------|---------|-------|----------|
| MiniMax M2.7 | MiniMax | $0.20 | $0.70 | 32K | ⚡⚡⚡⚡ | Budget-friendly |
| Gemini Flash | Google | $0.075 | $0.40 | 1M | ⚡⚡⚡⚡ | Long context |
| GPT-3.5 | OpenAI | $0.50 | $2.00 | 16K | ⚡⚡⚡⚡⚡ | Fast & cheap |
| GPT-4o Mini | OpenAI | $0.15 | $0.60 | 128K | ⚡⚡⚡⚡ | ⭐ Best value |
| Claude Haiku | Anthropic | $0.25 | $1.25 | 200K | ⚡⚡⚡ | Fast coding |
| Gemini Pro | Google | $1.25 | $5.00 | 1M | ⚡⚡⚡ | Massive context |
| GPT-4o | OpenAI | $2.50 | $10.00 | 128K | ⚡⚡⚡ | Premium quality |
| Claude Sonnet | Anthropic | $3.00 | $15.00 | 200K | ⚡⚡ | Top tier |

---

## B4. OPENCLAW

### Apa Itu OpenClaw?

```
OpenClaw = Platform AI Gateway

Fungsinya menghubungkan:
- Channel (WhatsApp, Telegram) ← → User
- AI Model (MiniMax, GPT-4, Claude) ← → Brain
- Skills & Tools ← → Capabilities
- Automation ← → Scheduled tasks

Tanpa OpenClaw:
Lo harus coding sendiri semua:
- WhatsApp API integration
- Telegram Bot integration
- AI Model API integration
- Conversation management
- Skill system
- Dan 1000 hal lagi...

Dengan OpenClaw:
- Install → Configure → Done!
- Gak perlu coding
- Gak perlu maintain complex system
```

### Kenapa OpenClaw?

```
KEUNTUNGAN:
✅ Open source & free
✅ Easy to install (1 command)
✅ Support banyak channel (WA, Telegram, Discord, dll)
✅ Support banyak AI model
✅ Built-in skill system
✅ Cron/automation built-in
✅ Active community
✅ Regular updates

GRAFIS:
[User] → [WhatsApp/Telegram] → [OpenClaw] → [AI Model]
                                            ↓
                                      [Skills/Tools]
                                            ↓
                                      [Actions/Automation]
```

### Alternatif OpenClaw

```
1. Botpress
   - More enterprise
   - More complex setup
   - Free tier available
   
2. Flowise
   - Drag-drop AI flows
   - Open source
   
3. Voiceflow
   - Focus on voice
   - More for Alexa/Google Assistant

TAPI untuk use case kita (WhatsApp/Telegram AI Bot):
OpenClaw = ✅ Best choice
- Simpel
- Affordable
- Didukung community
- Spec-built for this use case
```

---

## B5. CHANNEL (WHATSAPP & TELEGRAM)

### Pilihan Channel

```
PRIMARY CHANNELS (yang kita pake):

1. WhatsApp
   - Base user: semua orang
   - Setup: Scan QR Code
   - Limitation: 1 nomor = 1 bot
   - Professionalism: ⭐⭐⭐

2. Telegram
   - Base user: lebih tech-savvy
   - Setup: Bot Token
   - Advantage: unlimited bots
   - Professionalism: ⭐⭐⭐⭐⭐

OTHER CHANNELS (supported by OpenClaw):
- Discord
- Slack
- Line
- Signal
- Web Chat (embed di website)
```

### WhatsApp vs Telegram

| Aspek | WhatsApp | Telegram |
|-------|----------|----------|
| **Setup** | Scan QR (30 detik) | Bot Father (2 menit) |
| **Nomor HP** | Butuh (terpisah) | Gak butuh |
| **Bot Limit** | 1 per nomor | Unlimited |
| **Group Support** | ✅ | ✅ |
| **Media** | ✅ | ✅ |
| **Professional** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **User Base** | Everyone | Tech-savvy |
| **API Limit** | Stringent | More relaxed |
| **Business Ready** | WhatsApp Business API | ✅ Native |

### Rekomendasi

```
UNTUK PERSONAL AI ASSISTANT:
✅ WhatsApp (lo udah familiar)
✅ Telegram (lebih reliable)

UNTUK BUSINESS BOT (multiple clients):
✅ Telegram (bisa unlimited bots)
✅ WhatsApp Business API (if budget ada)

UNTUK STARTING:
1. Setup Telegram dulu (gak perlu nomor baru)
2. Kalo client minta WhatsApp, baru tambah
```

---

# BAGIAN C: BUDGET & BIAYA

---

## C1. BUDGET UNTUK CLIENT

Client = Orang yang mau pake AI Bot

### Budget WAJIB (Per Bulan)

```
1. VPS (Server)
   ─────────────────────────────────────
   Harga: Rp 50.000 - 150.000/bulan
   
   Untuk: Running bot 24/7
   Spec minimal: 1 vCPU, 1GB RAM
   
   Provider: DigitalOcean, Vultr, dll
   
2. AI Model API
   ─────────────────────────────────────
   Mulai dari: FREE (kalau pake free tier)
   Jika perlu: Rp 30.000 - 500.000/bulan
   
   Tergantung:
   - Volume chat
   - Model yang dipilih
   - Usage pattern
```

### Budget OPSIONAL

```
3. Domain (untuk web interface)
   ─────────────────────────────────────
   Harga: Rp 50.000 - 150.000/tahun
   Untuk: Buka bot via browser
   Contoh: bot.tokokue.com
   
4. WhatsApp Business API (enterprise only)
   ─────────────────────────────────────
   Harga: Rp 500.000 - 5.000.000/bulan
   Untuk: Official WhatsApp dengan verified badge
   Necessary only: Large enterprise
   
5. Extra Services
   ─────────────────────────────────────
   - Email automation: included in bot
   - CRM integration: varies
   - Payment integration: depends on provider
```

### Total Budget Client (Per Bulan)

| Tipe | Minimal | Standard | Premium |
|------|---------|----------|---------|
| **VPS** | Rp 50.000 | Rp 100.000 | Rp 150.000 |
| **AI Model** | FREE | Rp 50.000 | Rp 200.000 |
| **Domain** | - | Rp 10.000 | Rp 15.000 |
| **Total** | **~GRATIS** | **~Rp 160.000** | **~Rp 365.000** |

### Catatan Penting

```
FREE TIER AVAILABLE:
✅ MiniMax: ~$5 free credit
✅ Gemini Flash: 1.5M tokens free/month
✅ GPT-3.5: $5 free credit

ARTINYA:
- Untuk personal use (50-100 chats/day)
- Bisa FREE atau sangat CHEAP
- Baru perlu bayar kalau sudah heavy usage
```

---

## C2. BUDGET UNTUK PROVIDER

Provider = Kamu yang bikinin bot untuk client

### Modal Awal (Sekali)

```
GRATIS (Modal Utama = Knowledge & Waktu):

✅ Install OpenClaw: FREE
✅ Setup WhatsApp: FREE
✅ Setup Telegram Bot: FREE
✅ Skills: FREE
✅ Panduan ini: FREE

OPSIONAL (gak harus ada):
- VPS sendiri untuk testing: Rp 100.000/bulan
- Domain untuk portfolio: Rp 100.000/tahun
- Sample bots untuk portfolio: waktu + kreativitas
```

### Effort (Yang Sebenarnya)

```
Investment UTAMA:
⏰ Waktu setup: 2-5 jam per project
⏰ Waktu belajar: 1-2 hari (dari panduan ini)
💡 Effort: Reading + Practice

BUKAN MODAL UANG, TAPi TIME & EFFORT
```

### Suggested Pricing (Per Project)

| Paket | Harga Sekali | Waktu Setup | Include |
|-------|--------------|-------------|---------|
| **Basic** | Rp 200.000 | 1-2 jam | 1 platform (WA atau Telegram) |
| **Standard** | Rp 400.000 | 2-3 jam | 2 platform + basic setup |
| **Premium** | Rp 750.000 | 3-5 jam | Full setup + multiple platforms |

### Suggested Maintenance (Per Bulan)

| Paket | Harga/Bulan | Include |
|-------|-------------|---------|
| **Basic** | Rp 100.000 | Monitoring + updates |
| **Standard** | Rp 150.000 | + Email support |
| **Premium** | Rp 250.000 | + Priority response |

---

## C3. BIAYA AI MODEL (DETAIL)

### Cara Hitung Biaya AI

```
RUMUS:

Total Biaya = (Input Tokens × Input Rate) + (Output Tokens × Output Rate)

CONTOH:
- 100 chat per hari
- 300 tokens per chat (input)
- 150 tokens per chat (output)
- Total per hari: 300 + 150 = 450 tokens/chat
- Total per bulan: 450 × 100 × 30 = 1.350.000 tokens/bulan

DENGAN GPT-4o Mini:
- Input: 1.350.000 × $0.15/1M = $0.2025
- Output: 1.350.000 × $0.60/1M = $0.81
- Total: ~$1.01/bulan = ~Rp 16.000/bulan

DENGAN Claude 3.5 Sonnet:
- Input: 1.350.000 × $3.00/1M = $4.05
- Output: 1.350.000 × $15.00/1M = $20.25
- Total: ~$24.30/bulan = ~Rp 390.000/bulan
```

### Tabel Biaya per Usage Level

```
VOLUME RENDAH (30 chats/hari, ~100 tokens/chat):
─────────────────────────────────────────────────
Model               | $/bulan | Rp/bulan |
MiniMax M2.7       | ~$0.10  | ~Rp 1.600 |
Gemini Flash       | ~$0.05  | ~Rp 800   |
GPT-4o Mini        | ~$0.20  | ~Rp 3.200 |
Claude Haiku        | ~$0.35  | ~Rp 5.600 |

VOLUME SEDANG (100 chats/hari, ~300 tokens/chat):
─────────────────────────────────────────────────
Model               | $/bulan | Rp/bulan |
MiniMax M2.7       | ~$0.90  | ~Rp 14.400 |
Gemini Flash       | ~$0.45  | ~Rp 7.200  |
GPT-4o Mini        | ~$1.00  | ~Rp 16.000 |
Claude Haiku        | ~$1.80  | ~Rp 28.800 |

VOLUME TINGGI (500 chats/hari, ~500 tokens/chat):
─────────────────────────────────────────────────
Model               | $/bulan | Rp/bulan |
MiniMax M2.7       | ~$7.50  | ~Rp 120.000 |
Gemini Flash       | ~$3.75  | ~Rp 60.000  |
GPT-4o Mini        | ~$8.00  | ~Rp 128.000 |
Claude Haiku        | ~$15.00 | ~Rp 240.000 |
GPT-4o             | ~$60.00 | ~Rp 960.000 |
Claude Sonnet       | ~$100.00| ~Rp 1.600.000 |
```

### Free Tier Limits

```
FREE TIER YANG BISA DIGUNAKAN:

1. MiniMax (minimax.io)
   - $5 free credit
   - Token: ~25M input atau ~7M output
   - Cukup untuk: 50-100 chats/day untuk 1-2 bulan
   - Registration: mudah

2. Google AI Studio (aistudio.google.com)
   - 1.5M tokens/month FREE (Gemini 1.5 Flash)
   -足够 untuk: ~15.000 short conversations/month
   - Cukup untuk: LOW volume business bot
   - Registration: butuh Google account

3. OpenAI (openai.com)
   - $5 free credit (for new users)
   - Token: ~10M input atau ~2.5M output
   - Cukup untuk: Testing + low volume
   - Registration: butuh phone verification

STRATEGI FREE:
- Start dengan free tier
- Monitor usage
- Upgrade kalau udah deket limit
```

---

## C4. TABEL RINGKASAN BIAYA

### Untuk Client (Per Bulan)

| Kebutuhan | Opsi Murah | Opsi Standard | Opsi Premium |
|-----------|------------|---------------|--------------|
| **VPS** | Rp 50.000 | Rp 100.000 | Rp 150.000 |
| **AI Model** | FREE | Rp 50.000 | Rp 200.000 |
| **Setup Fee** | Rp 200.000 | Rp 400.000 | Rp 750.000 |
| **Maintenance** | Rp 100.000 | Rp 150.000 | Rp 250.000 |
| **Total First Month** | **~Rp 350.000** | **~Rp 700.000** | **~Rp 1.350.000** |
| **Total Next Month** | **~Rp 150.000** | **~Rp 300.000** | **~Rp 600.000** |

### Untuk Provider (Profit)

```
PER PROJECT:

Basic (Rp 200.000 - 300.000 setup):
- Time: 1-2 jam
- Profit: ~Rp 150.000-250.000
- Effective rate: ~Rp 100.000-150.000/jam

Standard (Rp 400.000 - 600.000 setup):
- Time: 2-3 jam
- Profit: ~Rp 350.000-550.000
- Effective rate: ~Rp 150.000-200.000/jam

Premium (Rp 750.000 - 1.500.000 setup):
- Time: 3-5 jam
- Profit: ~Rp 600.000-1.300.000
- Effective rate: ~Rp 200.000-300.000/jam

MONTHLY RECURRING:
- Basic maintenance: Rp 100.000/bulan
- Standard: Rp 150.000/bulan
- Premium: Rp 250.000/bulan

Example:
- 5 clients × Rp 150.000/bulan = Rp 750.000/bulan recurring
- 10 clients × Rp 150.000/bulan = Rp 1.500.000/bulan recurring
```

---

# BAGIAN D: SETUP DARI 0 - DI LAPTOP

---

## D1. BELI DAN SETUP VPS

### Step 1: Pilih Provider

```
REKOMENDASI: DigitalOcean

Alasan:
- Mudah注册
- Singapore region (dekat Indonesia)
- Dashboard понятный
- Documentation lengkap
- Price transparent

Alternatif: Vultr, Linode, Hetzner
```

### Step 2: Create Account

```
1. Buka https://www.digitalocean.com
2. Klik "Sign Up"
3. Masukkan:
   - Email
   - Password
   - Verifikasi email
4. Login
```

### Step 3: Add Payment

```
1. Buka https://cloud.digitalocean.com/billing
2. Klik "Add credit card" atau "Add payment method"
3. Masukkan data kartu kredit
4.一些小优惠: bisa juga pake PayPal

NOTE:
- Accepts Visa, Mastercard
- Some countries accept prepaid cards
- $5 minimum untuk verify
```

### Step 4: Create Droplet

```
1. Klik hijau "Create" → "Droplets"

2. Configure:

   📍 Choose Region:
   → Singapore (paling dekat & latency rendah)

   🖥️ Choose an Image:
   → Ubuntu 22.04 LTS (x64) [ RECOMMENDED ]
   → atau Ubuntu 24.04 LTS (newer)

   📦 Choose Size:
   → $6/mo - 1 vCPU, 1GB, 25GB SSD [CUKUP UNTUK MULAI]
   → $12/mo - 1 vCPU, 2GB, 50GB SSD [JIKA LEBIH]

   🔐 Choose Authentication:
   → Password [EASIER untuk pemula]
   → SSH Key [MORE SECURE, optional]

   ☐ Additional Options:
   → ☑️ Monitoring (FREE, useful)
   → ☐ VPC Network (default, leave as is)

   🔤 Finalize:
   → Hostname: openclaw-server
   → Quantity: 1

3. Klik "Create Droplet"
4. Tunggu 1-2 menit
5. ✅ Berhasil! Dapat IP address di email & dashboard
```

### Step 5: Simpan Credentials

```
SETELAH DROPLET JADI:

Lo dapat di email:
━━━━━━━━━━━━━━━━━━
IP Address: 143.198.xx.xx
Username: root
Password: xxxxxxxx

SIMPAN INFO INI:
- Write it down
- Save somewhere safe
- Lo butuh ini untuk connect via SSH
━━━━━━━━━━━━━━━━━━
```

---

## D2. CONNECT VPS DARI WINDOWS

### Cara 1: Windows Terminal (Recommended - Windows 10/11)

```
1. Buka Windows Terminal
   - Windows 11: Klik kanan Start → "Terminal"
   - Windows 10: Search "Windows Terminal"

2. Connect dengan command:
   ssh root@143.198.xx.xx
   
   (ganti 143.198.xx.xx dengan IP lo)

3. Tekan Enter
4. Muncul prompt:
   "Are you sure you want to continue connecting?"
   → Ketik: yes
   → Enter

5. Password prompt:
   → Paste password dari email (klik kanan untuk paste)
   → Enter
   
   NOTE: Password gak keliatan (normal di Linux)
   
6. Jika berhasil:
   
   root@openclaw-server:~#
   
   🎉 Berhasil connect!
```

### Cara 2: PuTTY (Untuk Windows Lama / lebih visual)

```
1. Download PuTTY:
   - Buka https://www.putty.org
   - Download putty.exe

2. Buka PuTTY

3. Configure:
   - Host Name (or IP address): 143.198.xx.xx
   - Port: 22
   - Connection type: SSH

4. Klik "Open"

5. Login prompt:
   - Login as: root
   - Password: (paste dari email)

6. Jika berhasil:
   
   root@openclaw-server:~#
   
   🎉 Berhasil connect!
```

### Troubleshooting Koneksi

```
MASALAH: "Connection refused"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Cause: SSH service belum jalan
Solve:
  service ssh status
  service ssh start

MASALAH: "Connection timed out"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Cause: Salah IP atau firewall block
Solve:
  - Cek IP address di DigitalOcean dashboard
  - Tambah Firewall rule: allow port 22

MASALAH: "Permission denied"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Cause: Password salah
Solve:
  - Reset password di DigitalOcean console
  - Atau generate new password

MASALAH: Paste gak работает di Terminal
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Cause: Windows Terminal default Ctrl+V
Solve:
  - Klik kanan di window → Paste
  - Atau Ctrl+Shift+V
```

---

## D3. CONNECT VPS DARI MAC/LINUX

### Dari Mac

```
1. Buka Terminal
   - Cmd + Space → ketik "Terminal"
   - Enter

2. Connect:
   ssh root@143.198.xx.xx
   
   (ganti dengan IP lo)

3. Tekan Enter
4. First time: muncul fingerprint confirmation
   → Ketik: yes
   → Enter

5. Masukkan password:
   → Paste (Cmd+V)
   → Enter

6. Jika berhasil:
   
   root@openclaw-server:~#
   
   🎉
```

### Dari Linux

```
1. Buka Terminal
   - Ctrl+Alt+T (umumnya)
   - Atau search "Terminal"

2. Connect:
   ssh root@143.198.xx.xx

3. Enter password

4. Done!
```

---

## D4. INSTALL OPENCLAW

### Prasyarat

```
SEBELUM INSTALL, PASTIKAN:

1. Sudah connect ke VPS via SSH
2. Tampil prompt seperti ini:
   root@openclaw-server:~#

3. Jika belum, kembali ke section D2/D3
```

### Step 1: Update Server

```
JALANKAN:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
apt update && apt upgrade -y
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Ini 1-5 menit, tergantung koneksi.

Output yang bener:
- Reading package lists... Done
- Building dependency tree... Done
- 0 upgraded, 0 newly installed

Lanjut ke step 2
```

### Step 2: Install Node.js

```
OPENCLAW BUTUH NODE.JS 18+.

JALANKAN:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
apt-get install -y nodejs
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

VERIFIKASI:
node --version
npm --version

Output yang bener:
- v18.x.x atau lebih tinggi
- 9.x.x atau lebih tinggi
```

### Step 3: Install OpenClaw

```
JALANKAN:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
npm install -g openclaw
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Ini 2-5 menit.

SUCCESS OUTPUT:
- + openclaw@x.x.x
- added xxx packages
```

### Step 4: Verifikasi Install

```
JALANKAN:
openclaw --version

Output: x.x.x (version number)
```

### Step 5: Initialize OpenClaw

```
JALANKAN:
openclaw init

OUTPUT:
? Choose a mode for this gateway (Use arrow keys)
❯ configure  (recommended)
  install-only
  skip
```

PILIH: configure (arrow down → Enter)

```
SETELAH INIT:

? Setup account? (Y/n)
→ Y

? Gateway auth token:
→ (will be generated automatically - SIMPAN!)
```

### Step 6: Start OpenClaw

```
JALANKAN:
openclaw start

OUTPUT:
Gateway starting on http://localhost:18789
```

### Step 7: Akses Dashboard

```
DARI BROWSER DI LAPTOP:

1. Buka: http://143.198.xx.xx:18789
   
   (ganti 143.198.xx.xx dengan IP VPS lo)

2. Akan diminta login:
   - Username: (kosongin atau "admin")
   - Password: (auth token dari step 5)

3. 🎉 DASHBOARD TERBUKA!
```

---

## D5. SETUP AUTO-START (PM2)

Tanpa PM2, bot MATI kalau server reboot. Dengan PM2, bot AUTO START.

### Install PM2

```
JALANKAN:
npm install -g pm2
```

### Start OpenClaw dengan PM2

```
JALANKAN:
pm2 start openclaw --name openclaw

OUTPUT:
[PM2] Spawning PM2 daemon
[PM2] Starting openclaw in fork_mode
[PM2] Done.
```

### Verify PM2 Status

```
JALANKAN:
pm2 list

OUTPUT:
┌─────┬──────────┬─────────────┬──────────┬──────────┐
│ id  │ name     │ mode        │ status   │ restart  │
├─────┼──────────┼─────────────┼──────────┼──────────┤
│ 0   │ openclaw │ fork        │ online   │ 0        │
└─────┴──────────┴─────────────┴──────────┴──────────┘

STATUS = online = ✅ Berhasil
```

### Setup Auto-Start saat Server Reboot

```
JALANKAN:
pm2 startup

OUTPUT:
[PM2] Generating system init script
[PM2] Detecting available init system

CARA SETUP (ikuti output dari pm2 startup):

Systemd:
  systemctl enable pm2-init.sh

ATAU BIASA NYA:
pm2 save

Ini SAVE current state.
Sekarang kalo server reboot, PM2 auto-start.
```

### Important PM2 Commands

```
LIHAT LOGS:
pm2 logs openclaw --lines 50

RESTART BOT:
pm2 restart openclaw

STOP BOT:
pm2 stop openclaw

MONITOR REAL-TIME:
pm2 monit

LIHAT STATUS:
pm2 list
```

---

## D6. VERIFIKASI BOT

### Checklist Pengecekan

```
SETIAP SETELAH SETUP, PASTIKAN:

□ PM2 Status = online
□ OpenClaw Dashboard accessible
□ VPS Resources (htop) = normal
□ Internet connectivity = OK
```

### Test Commands

```
TEST PM2:
pm2 list
→ Status "online" ✅

TEST DASHBOARD:
curl http://localhost:18789
→ HTML response ✅

TEST EXTERNAL ACCESS:
Buka browser: http://143.198.xx.xx:18789
→ Dashboard muncul ✅

TEST RESOURCES:
htop
→ CPU < 50%, RAM < 80% ✅
```

---

# BAGIAN E: SETUP DARI 0 - DI HP

---

## E1. CONNECT VPS DARI ANDROID

### Menggunakan Termius (Recommended)

```
STEP 1: Download
1. Buka Google Play Store
2. Search "Termius"
3. Download & Install (FREE with ads, or Premium)

STEP 2: Buat New Host
1. Buka Termius
2. Klik "+" (New Host)
3. Isi form:

   ┌─────────────────────────────────┐
   │ LABEL: OpenClaw Server          │
   │ HOSTNAME: 143.198.xx.xx          │
   │ USERNAME: root                  │
   │ PASSWORD: xxxxxxxx              │
   │ PORT: 22                        │
   └─────────────────────────────────┘

4. Klik "Save"

STEP 3: Connect
1. Klik host yang baru dibuat
2. Accept fingerprint (first time only)
3. Masukkan password lagi (jika diminta)
4. ✅ Connected!

STEP 4: Verify
Lihat prompt:
root@openclaw-server:~#
```

### Menggunakan JuiceSSH (Alternative - FREE)

```
STEP 1: Download
1. Google Play Store
2. Search "JuiceSSH"
3. Install

STEP 2: Create Connection
1. Connections → + (NEW)
2. Type: SSH
3. Identity:
   - Nickname: OpenClaw
   - Username: root
   - Password: (password VPS)
4. Connect:
   - Address: 143.198.xx.xx
   - Port: 22

5. Save → Connect
```

### Menggunakan Rotati (SSH + SFTP)

```
STEP 1: Download
1. Google Play Store
2. Search "Rotati"
3. Install

STEP 2: Setup
1. NEW Connection
2. Isi hostname, username, password
3. Connect

KELEBIHAN:
- Built-in SFTP (transfer files)
- Bookmark sites
- Multiple sessions
```

---

## E2. CONNECT VPS DARI iPHONE

### Menggunakan Termius (Recommended)

```
STEP 1: Download
1. App Store
2. Search "Termius"
3. Download & Install

STEP 2: Setup
1. Buka Termius
2. + → New Host
3. Isi:
   - Host: 143.198.xx.xx
   - Username: root
   - Password: xxxxxxxx
   - Port: 22

4. Save

STEP 3: Connect
1. Tap host
2. ✅ Terminal terbuka
```

### Menggunakan ShellFire (Free)

```
STEP 1: Download
1. App Store
2. Search "ShellFire"
3. Install

STEP 2: Connect
1. NEW → SSH
2. Isi credentials
3. Connect
```

### Menggunakan Blink Shell (Premium Feel)

```
STEP 1: Download
1. App Store
2. Search "Blink Shell"
3. Install ($15 one-time)

STEP 2: Connect
1. + New Host
2. Fill in details
3. Connect

KELEBIHAN:
- Professional grade
- Mosh support (better for mobile)
- Very responsive
```

---

## E3. MANAGE BOT DARI HP

### Yang Bisa Dilakukan dari HP

```
✅ Monitor bot status (pm2 list)
✅ Lihat logs (pm2 logs)
✅ Restart bot (pm2 restart)
✅ Edit config files (nano/vi)
✅ Install updates
✅ View resource usage (htop)
✅ Monitor AI usage

❌ Setup awal (lebih enak di laptop)
❌ Complex config editing
❌ Multi-file operations
```

### Essential Commands for Mobile

```
STATUS CHECK:
pm2 list

LOGS:
pm2 logs openclaw --lines 30

RESTART:
pm2 restart openclaw

STOP:
pm2 stop openclaw

RESOURCES:
htop
```

### Mobile Workflow

```
BIASA WORKFLOW DARI HP:

1. Buka Termius
2. Connect ke VPS
3. pm2 list → Cek status
4. pm2 logs openclaw --lines 20 → Cek error
5. Jika ada issue → pm2 restart openclaw
6. Cek lagi → pm2 list

FOR EMERGENCIES:
- Kalo bot down & lo lagi di luar
- Buka app → SSH → pm2 restart
- Done! Bot up lagi
```

---

# BAGIAN F: CHANNEL SETUP

---

## F1. SETUP WHATSAPP

### Prerequisites

```
SEBELUM SETUP WHATSAPP:

⚠️ PASTIKAN PAKAI NOMOR TERPISAH
- Nomors utama lo = JANGAN dipake
- Gw recommend: eSIM kedua / virtual number
- Sekali dipairing, nomor itu "terkubur" di WhatsApp Web

⚠️ BACKUP NOMOR
- Nomor yang dipake = hilang dari WhatsApp normal
- Jadi pastikan NOMOR KEDUA
```

### Step 1: Generate WhatsApp Session

```
DI DASHBOARD OPENCLAW:

1. Buka: http://143.198.xx.xx:18789
2. Login
3. Navigate ke: Settings → Channels → WhatsApp
4. Klik "Enable" atau "Scan QR"

OUTPUT:
- QR Code muncul di screen
```

### Step 2: Scan QR Code

```
DI HP:

1. Buka WhatsApp di HP yang mau dipake
2. iPhone: Settings → Linked Devices → Link a Device
   Android: ⋮ → Linked Devices → Link a Device
3. Scan QR Code dari screen laptop
4. Wait...
5. ✅ "Device Linked"
```

### Step 3: Verify Connection

```
DI DASHBOARD:

1. Liat status: "Connected" atau "Active"
2. Test dengan kirim pesan ke nomor bot
3. Bot harusnya reply

DI HP BOT:

1. Buka chat dengan bot (nomor bot sendiri)
2. Kirim pesan: "Hello"
3. Harusnya dapat response
4. ✅ WhatsApp connected!
```

### Important Notes

```
⚠️ LIMITASI WHATSAPP:

1. 1 Nomor = 1 WhatsApp (gak bisa multiple device berbeda)
2. Nomor yang dipairing = gak bisa dipake di HP biasa
3. Session expiry = perlu re-scan berkala
4. Official WhatsApp Business API = expensive
5. Unofficial gateway (ini) = risk banned (low risk tapi ada)

⚠️ BEST PRACTICES:

1. Use номер kedua / eSIM
2. Jangan spam (lewat batas = banned)
3. Jangan auto-reply terlalu cepat (spam detection)
4. Setup proper greeting
5. Monitor connected status
```

### Troubleshooting WhatsApp

```
MASALAH: QR Code gak muncul
━━━━━━━━━━━━━━━━━━━━━━━━━━
Solve:
- Refresh page
- Clear cache
- Cek console logs

MASALAH: Scan berhasil tapi gak connect
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Solve:
- Matikan mobile data HP, coba WiFi-only
- Restart OpenClaw: pm2 restart openclaw
- Re-scan QR

MASALAH: "Phone Disconnected"
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Solve:
- HP kehilangan koneksi internet
- WhatsApp di HP crash → restart HP
- Session expired → re-scan QR

MASALAH: Bot gak reply
━━━━━━━━━━━━━━━━━━━━━
Solve:
- Cek AI model config
- Cek logs: pm2 logs openclaw
- Test AI separately
```

---

## F2. SETUP TELEGRAM BOT

### Step 1: Buat Bot di Telegram

```
DI HP ATAU LAPTOP:

1. Buka Telegram
2. Search: @BotFather
3. Klik START

4. Kirim command: /newbot

5. BotFather asks:
   "Alright, a new bot. How are we going to call it? Please choose a name for your bot."
   
   → Ketik nama bot, contoh: "AI Fajar Bot"

6. BotFather asks:
   "Good. Now let's give it a username. Username must end in `bot`. Like MyFirstBot, cat_bot, Tetris_bot or PrimeBot."
   
   → Ketik username harus AKHIRAN _bot, contoh: fajar_ai_bot

7. SUCCESS! BotFather kasih TOKEN:
   
   ┌─────────────────────────────────────┐
   │ Done! Congratulations on your new  │
   │ bot. You will find it at:          │
   │ t.me/fajar_ai_bot                  │
   │                                     │
   │ Use this token to access the HTTP  │
   │ API:                                │
   │ 123456789:ABCdefGHIjklMNOpqrsTUV    │
   │                                     │
   │ KEEP YOUR TOKEN SECURE!             │
   └─────────────────────────────────────┘

⚠️ SIMPAN TOKEN INI!
```

### Step 2: Configure Token di OpenClaw

```
DI DASHBOARD OPENCLAW:

1. Buka: http://143.198.xx.xx:18789
2. Settings → Channels → Telegram
3. Masukkan TOKEN dari BotFather
4. Klik "Enable"

JUGA DI CONFIG (jika perlu):

Token: 123456789:ABCdefGHIjklMNOpqrsTUV
```

### Step 3: Get Your Chat ID

```
SETELAH ENABLE:

1. Buka Telegram
2. Chat ke bot yang baru dibuat
   - Search nama bot
   - Klik: t.me/fajar_ai_bot
3. Kirim: /start
4. Buka browser, visit:
   
   https://api.telegram.org/botYOUR_TOKEN/getUpdates
   
   Contoh:
   https://api.telegram.org/bot123456789:ABCdefGHIjklMNOpqrsTUV/getUpdates

5. Liat JSON response:
   {
     "ok": true,
     "result": [{
       "message": {
         "chat": {
           "id": 123456789,
           ...
         }
       }
     }]
   }

6. ANGKA DI "id": 123456789 = LO CHAT ID
7. SIMPAN CHAT ID INI
```

### Step 4: Verify Telegram Connection

```
DI TELEGRAM:

1. Kirim pesan ke bot: "Hello"
2. Should get response from AI

DI DASHBOARD:

1. Settings → Channels → Telegram
2. Status: Connected
3. Liat incoming message logs
```

### Multiple Telegram Bots

```
UNTUK MULTIPLE CLIENTS:

Masing-masing client = bot terpisah

BOT FATHER WORKFLOW:
1. /newbot → Client A Bot
2. /newbot → Client B Bot
3. Dst...

TOKEN MANAGEMENT:
- Simpan token masing-masing client
- Masukkan di OpenClaw config

CONFIGURASI:
{
  "channels": {
    "telegram": {
      "enabled": true,
      "bots": {
        "client_a": {
          "token": "TOKEN_CLIENT_A",
          "authorizedChats": ["CHAT_ID_A"]
        },
        "client_b": {
          "token": "TOKEN_CLIENT_B",
          "authorizedChats": ["CHAT_ID_B"]
        }
      }
    }
  }
}
```

---

## F3. SETUP MULTIPLE BOT

### Untuk Multiple Clients

```
ARSITEKTUR:

1 VPS = bisa handle multiple bots

CARA 1: Multiple Telegram Bots
├── Bot A (Client A) → Token A
├── Bot B (Client B) → Token B
└── Bot C (Client C) → Token C

CARA 2: Multiple WhatsApp
├── Number A (Client A)
├── Number B (Client B)
└── Number C (Client C) ← Butuh multiple SIM/eSIM

CARA 3: Hybrid
├── WhatsApp (Main client)
└── Telegram (Other clients)
```

### Resource Planning

```
1 BOT (1 client):
- RAM: ~200-300MB
- CPU: low
- Concurrent: 1-5 chats

10 BOTS (10 clients):
- RAM: ~500-800MB
- CPU: low-medium
- Concurrent: 10-50 chats

50 BOTS (50 clients):
- RAM: ~1.5-2GB
- CPU: medium
- VPS spec harus naik

UPGRADE PATH:
- 1-10 clients: $6-12/mo VPS
- 10-30 clients: $20/mo VPS
- 30-100 clients: $40/mo VPS
```

---

# BAGIAN G: AI MODEL SETUP

---

## G1. PILIH AI MODEL

### Decision Matrix

```
PILIH BERDASARKAN:

1. BUDGET
   │
   ├── FREE / $0-5/bulan → Gemini Flash, MiniMax, GPT-3.5
   ├── $5-20/bulan → GPT-4o Mini, Claude Haiku
   ├── $20-50/bulan → GPT-4o, Claude Sonnet
   └── $50+/bulan → Premium models

2. USE CASE
   │
   ├── Personal assistant → GPT-4o Mini, Claude Haiku
   ├── Business CS Bot → GPT-4o Mini (value)
   ├── Coding heavy → Claude Sonnet, GPT-4o
   ├── Long context (docs) → Gemini 1.5 Pro, Claude
   └── Fast responses → GPT-4o Mini, Claude Haiku

3. VOLUME
   │
   ├── Low (<100 chats/day) → Free tier OK
   ├── Medium (100-500) → $10-30/bulan
   └── High (500+) → $30+/bulan
```

### Rekomendasi Berdasarkan Situasi

| Situasi | Rekomendasi | Alasan |
|---------|-------------|---------|
| Baru mulai | MiniMax / Gemini Flash | Free tier, sufficient |
| Personal use | GPT-4o Mini | Best balance |
| Small business | GPT-4o Mini | Value for money |
| High quality needed | Claude Sonnet / GPT-4o | Premium |
| Long documents | Gemini 1.5 Pro | 1M context |
| Coding heavy | Claude Sonnet | Best coder |

---

## G2. PERBANDINGAN AI MODEL

### Tabel Perbandingan Detail

```
MODEL              | PROVIDER | INPUT$/M | OUTPUT$/M | CONTEXT | SPEED | BEST FOR
────────────────────────────────────────────────────────────────────────────
MiniMax M2.7      | MiniMax  | $0.20    | $0.70     | 32K    | ⚡⚡⚡⚡ | Budget
Gemini Flash       | Google   | $0.075   | $0.40     | 1M ⚡⚡⚡⚡ | Long context  
GPT-3.5 Turbo     | OpenAI   | $0.50    | $2.00     | 16K    | ⚡⚡⚡⚡⚡ | Fast cheap
GPT-4o Mini       | OpenAI   | $0.15    | $0.60     | 128K   | ⚡⚡⚡⚡ | ⭐ Best value
Claude 3.5 Haiku  | Anthro   | $0.25    | $1.25     | 200K   | ⚡⚡⚡ | Fast coding
Gemini 1.5 Pro    | Google   | $1.25    | $5.00     | 1M ⚡⚡⚡ | Huge context
GPT-4o            | OpenAI   | $2.50    | $10.00    | 128K   | ⚡⚡⚡ | Premium
Claude 3.5 Sonnet | Anthro   | $3.00    | $15.00    | 200K   | ⚡⚡ | Top tier
```

### Speed vs Quality Tradeoff

```
SPEED ←————————————————————————→ QUALITY
   │                              │
   │ GPT-3.5    GPT-4o Mini       │
   │ Gemini     Claude Haiku      │ Claude Sonnet
   │ Flash                          │ GPT-4o
   │                              │
   └──────────────────────────────┘
   Fast & Cheap              Slow & Premium
```

---

## G3. SETUP API KEY

### MiniMax (yang lo pake sekarang)

```
1. Buka https://www.minimax.io
2. Sign Up / Login
3. Dashboard → API Keys
4. Create New Key
5. Copy & Save ( jangan share!)

CONFIG DI OPENCLAW:
{
  "auth": {
    "profiles": {
      "minimax:global": {
        "provider": "minimax",
        "apiKey": "YOUR_API_KEY"
      }
    }
  }
}
```

### OpenAI (GPT-4o Mini)

```
1. Buka https://platform.openai.com
2. Sign Up / Login
3. Dashboard → API Keys
4. Create New Secret Key
5. Copy & Save

FREE CREDIT:
- New users: $5 free
- Usage: https://platform.openai.com/usage

CONFIG DI OPENCLAW:
{
  "auth": {
    "profiles": {
      "openai:global": {
        "provider": "openai",
        "apiKey": "sk-..."
      }
    }
  }
}
```

### Google AI (Gemini)

```
1. Buka https://aistudio.google.com
2. Sign in dengan Google account
3. Dashboard → Get API Key
4. Create (atau Use existing)
5. Copy & Save

FREE TIER:
- Gemini 1.5 Flash: 1.5M tokens/month FREE
- Gemini 1.5 Pro: Limited free tier

CONFIG DI OPENCLAW:
{
  "auth": {
    "profiles": {
      "google:global": {
        "provider": "google",
        "apiKey": "YOUR_API_KEY"
      }
    }
  }
}
```

### Anthropic (Claude)

```
1. Buka https://www.anthropic.com
2. Sign Up / Login
3. Console → API Keys
4. Create Key
5. Copy & Save

FREE CREDIT:
- New users: $5 free (varies)

CONFIG DI OPENCLAW:
{
  "auth": {
    "profiles": {
      "anthropic:global": {
        "provider": "anthropic",
        "apiKey": "sk-ant-..."
      }
    }
  }
}
```

---

## G4. KONFIGURASI MODEL DI OPENCLAW

### Basic Model Selection

```
DI DASHBOARD:

1. Settings → AI Models
2. Primary Model → Pilih dari dropdown:
   - minimax/MiniMax-M2.7
   - openai/gpt-4o-mini
   - google/gemini-1.5-flash
   - anthropic/claude-3-5-haiku-20240307

3. Save
```

### Via Config File

```
JALANKAN:
openclaw config edit

ATAUlangsung edit file:
nano ~/.openclaw/openclaw.json

CONFIGURE:
{
  "models": {
    "providers": {
      "minimax": {
        "apiKey": "YOUR_KEY",
        "models": [{
          "id": "MiniMax-M2.7"
        }]
      }
    }
  },
  "agents": {
    "defaults": {
      "model": {
        "primary": "minimax/MiniMax-M2.7"
      }
    }
  }
}
```

### Model Fallback (Jika Primary Gagal)

```
CONFIGURE FALLBACK:
{
  "agents": {
    "defaults": {
      "model": {
        "primary": "openai/gpt-4o-mini",
        "fallbacks": [
          "minimax/MiniMax-M2.7",
          "google/gemini-1.5-flash"
        ]
      }
    }
  }
}

ARTINYA:
1. Coba GPT-4o Mini dulu
2. Kalo gagal → coba MiniMax
3. Kalo gagal lagi → coba Gemini
4. Kalo semua gagal → error
```

---

# BAGIAN H: KONFIGURASI BOT

---

## H1. SETUP AI ASSISTANT PERSONAL

### Overview

```
AI ASSISTANT PERSONAL:

Untuk: Kamu sendiri
Goal: Helper yang kerja 24/7
Channel: WhatsApp atau Telegram
```

### Step 1: Basic Configuration

```
DI DASHBOARD:

1. Settings → General
2. Set bot name: "My AI Assistant"
3. Set greeting message
4. Set timezone: Asia/Jakarta
```

### Step 2: AI Personality

```
CONFIGURE:

{
  "ai": {
    "model": "minimax/MiniMax-M2.7",
    "personality": {
      "name": "Aira",
      "role": "Personal AI Assistant",
      "tone": "Friendly, casual, helpful",
      "language": "Bahasa Indonesia & English",
      "traits": [
        "Direct and to the point",
        "Proactive",
        "Helpful without being annoying"
      ]
    }
  }
}
```

### Step 3: System Instructions

```
CUSTOM INSTRUCTIONS:

Lo bisa override behavior dengan kasih specific instructions.

Contoh:

"You are Aira, a personal assistant for [Nama Lo]. 
You help with:
- Research and information gathering
- Drafting emails and messages
- Summarizing long documents
- Coding help
- General questions

Always:
- Be concise and direct
- Answer in the same language as the user
- If unsure, say you're unsure

Never:
- Make up information
- Share private data
- Be condescending"
```

### Step 4: Enable Features

```
FEATURES UNTUK PERSONAL ASSISTANT:

✅ Web Search - untuk research
✅ Calculator - untuk math
✅ Weather - cek cuaca
✅ Calendar - (jika connected)

INSTALL SKILLS:
openclaw skills install weather
openclaw skills install calculator
```

### Test Personal Assistant

```
TESTS TO RUN:

1. Simple greeting:
   "Hello, who are you?"
   → Should respond with personality

2. Information:
   "What's the weather in Jakarta?"
   → Should give weather

3. Task:
   "Help me write an email to my client"
   → Should help draft

4. Complex:
   "Research the latest AI trends"
   → Should search and summarize
```

---

## H2. SETUP BUSINESS BOT (CS BOT)

### Overview

```
BUSINESS BOT:

Untuk: Customer service bisnis
Goal: Handle inquiries 24/7
Channel: WhatsApp / Telegram / both
```

### Step 1: Business Profile

```
CONFIGURASI:

{
  "business": {
    "name": "Nama Bisnis Lo",
    "industry": "E-commerce / Restaurant / Service",
    "description": "Brief description",
    
    "contact": {
      "whatsapp": "+62812345678",
      "telegram": "@username",
      "email": "cs@bisnis.com",
      "address": "Jl. Alamat Bisnis"
    },
    
    "hours": "09.00 - 21.00",
    "timezone": "Asia/Jakarta"
  }
}
```

### Step 2: Knowledge Base

```
KNOWLEDGE BASE =

Semua info tentang bisnis lo yang harus AI tau.

{
  "knowledge": {
    "products": [
      {
        "name": "Produk A",
        "price": "Rp 100.000",
        "description": "Deskripsi produk",
        "stock": "Ready" / "Pre-order" / "Out of stock"
      }
    ],
    
    "services": [
      {
        "name": "Layanan A",
        "description": "Apa yang dilakukan",
        "price": "Rp 50.000",
        "duration": "1-2 jam"
      }
    ],
    
    "faq": [
      {
        "question": "Jam berapa buka?",
        "answer": "09.00 - 21.00"
      },
      {
        "question": "Bagaimana cara pesan?",
        "answer": "Chat ke nomor ini dengan format: Nama, Alamat, Pesanan"
      }
    ],
    
    "policies": {
      "shipping": "2-5 hari kerja",
      "return": "Bisa return dalam 3 hari dengan video unboxing",
      "payment": "Transfer BCA atau COD"
    }
  }
}
```

### Step 3: CS Personality

```
CONFIGURE:

{
  "ai": {
    "model": "openai/gpt-4o-mini",
    "personality": {
      "role": "Customer Service",
      "name": "CS Bot",
      "tone": "Friendly, professional, helpful",
      "language": "Bahasa Indonesia",
      
      "rules": [
        "Always be polite",
        "Confirm order details before closing",
        "Escalate complaints to human",
        "Never make up product info",
        "Always mention price clearly"
      ]
    }
  }
}
```

### Step 4: Automation Rules

```
AUTO-REPLY RULES:

1. GREETING (when customer says hi)
   → "Halo! Terima kasih sudah menghubungi [Nama Bisnis]. 
      Saya CS Bot. Ada yang bisa saya bantu?"

2. PRODUCT INQUIRY (when asking about product)
   → AI check knowledge base → give product info

3. ORDER PROCESS
   → Collect: Nama, Alamat, Pesanan
   → Confirm details
   → Give total price
   → Give ETA

4. COMPLAINT
   → Listen
   → Apologize
   → Escalate to human: "Mohon tunggu, saya将进一步连接 dengan tim kami."

5. CLOSING
   → "Terima kasih! Jika ada pertanyaan lain, jangan ragu untuk menghubungi kami lagi."
```

### Example: E-commerce Fashion Bot

```javascript
{
  "business": {
    "name": "Fashion House Indonesia",
    "industry": "Fashion E-commerce"
  },
  
  "knowledge": {
    "products": [
      {
        "name": "Dress Floral Midi",
        "price": "Rp 350.000",
        "sizes": ["S", "M", "L"],
        "colors": ["Blue", "Pink", "White"],
        "stock": "Ready"
      },
      {
        "name": "High Waist Jeans",
        "price": "Rp 450.000",
        "sizes": ["26", "28", "30", "32"],
        "colors": ["Blue", "Black"],
        "stock": "Ready"
      }
    ],
    
    "shipping": [
      {"name": "JNE", "eta": "2-4 hari"},
      {"name": "J&T", "eta": "2-5 hari"},
      {"name": "SiCepat", "eta": "1-3 hari"}
    ],
    
    "payment": ["BCA", "Mandiri", "COD"],
    
    "faq": [
      {"q": "Berapa lama pengiriman?", "a": "2-5 hari kerja tergantung ekspedisi"},
      {"q": "Bisa retur?", "a": "Bisa dalam 3 hari dengan video unboxing"},
      {"q": "Jam berapa buka?", "a": "08.00 - 22.00"}
    ]
  },
  
  "ai": {
    "personality": {
      "tone": "Friendly, helpful, salesperson vibes",
      "style": "Sapa dengan salam, tanya kebutuhan, recommend produk"
    }
  }
}
```

---

## H3. SETUP AUTOMATION (CRON / SCHEDULED TASKS)

### Apa Itu Automation

```
CRON = Task yang jalan OTOMATIS di waktu tertentu

CONTOH:
- Setiap jam 9 pagi → kirim report
- Setiap Senin jam 8 → posting promo
- Setiap hari jam 6 sore → reminder ke customer
- Setiap 5 menit → check price

BEDA NYA:
- User-triggered: User chat → AI respon
- Cron: Waktu tertentu → AI aksi otomatis
```

### Setup Cron di OpenClaw

```
VIA DASHBOARD:

1. Settings → Automation → Cron
2. Add New Cron Job
3. Configure

VIA CONFIG:

{
  "cron": {
    "jobs": [
      {
        "name": "Morning Report",
        "schedule": {
          "kind": "cron",
          "expr": "0 9 * * *"  // Every day at 9 AM
        },
        "payload": {
          "kind": "agentTurn",
          "message": "Kirim morning report ke semua client"
        }
      }
    ]
  }
}
```

### Cron Expression Guide

```
CRON FORMAT: minute hour day month weekday

CONTOH:

0 9 * * *       → Every day at 9:00 AM
0 18 * * *      → Every day at 6:00 PM
30 9 * * 1      → Every Monday at 9:30 AM
0 */2 * * *     → Every 2 hours
0 9,18 * * *    → Every day at 9 AM and 6 PM
*/5 * * * *     → Every 5 minutes

SPECIAL:
@hourly        → Every hour
@daily         → Every day at midnight
@weekly        → Every week at midnight
```

### Example Automations

```
1. MORNING GREETING (every day 8 AM)
   ┌─────────────────────────────────────┐
   │ Job: Morning Greeting               │
   │ Schedule: 0 8 * * *                 │
   │ Action: Send good morning message   │
   │ To: All customers                   │
   └─────────────────────────────────────┘

2. PRICE ALERT (every 15 minutes)
   ┌─────────────────────────────────────┐
   │ Job: Bitcoin Price Check             │
   │ Schedule: */15 * * * *               │
   │ Action: Check BTC price              │
   │ If > $100k → Alert user             │
   └─────────────────────────────────────┘

3. WEEKLY PROMO (every Monday 10 AM)
   ┌─────────────────────────────────────┐
   │ Job: Weekly Promo                    │
   │ Schedule: 0 10 * * 1                 │
   │ Action: Send promo to all customers  │
   └─────────────────────────────────────┘

4. DAILY REPORT (every day 7 PM)
   ┌─────────────────────────────────────┐
   │ Job: Daily Summary                   │
   │ Schedule: 0 19 * * *                 │
   │ Action: Generate & send daily report │
   └─────────────────────────────────────┘

5. FOLLOW-UP (1 hour after order)
   ┌─────────────────────────────────────┐
   │ Job: Order Follow-up                 │
   │ Trigger: After order confirmation    │
   │ Wait: 1 hour                         │
   │ Action: "Apakah pesanan sudah diterima?" │
   └─────────────────────────────────────┘
```

---

## H4. SETUP AI AGENTIC (AUTONOMOUS ACTIONS)

### Apa Itu AI Agentic

```
AI AGENTIC = AI yang BISA AMBIL ACTION SENDIRI

BEDA:

AI Biasa:
User: "ChatGPT, buatin email"
AI: *kasih draft email*
User: *copy paste manual ke email client*

AI Agentic:
User: "ChatGPT, handle email dari client"
AI: *baca inbox* → *generate response* → *send email* → *confirm*

USER CUMA PERNYATAIN GOAL, AI YANG EKSEKUSI
```

### Kemampuan AI Agentic (2026 Reality)

```
YANG SUDAH BISA:
✅ Auto-reply email + send
✅ Browse web + extract info
✅ Post to social media
✅ Monitor price + alert
✅ Schedule appointments
✅ Update spreadsheets
✅ Generate reports + send
✅ Basic data analysis
✅ File management

YANG BELUM BISA (atau masih limited):
❌ Full autonomous (still need rules)
❌ Self-initiated goals (need trigger)
❌ True "thinking" (pattern matching)
❌ Handle highly nuanced situations
❌ Make big decisions independently
```

### Setup AI Agentic di OpenClaw

```
PREREQUISITES:

1. AI Model with function calling:
   - GPT-4o, GPT-4o Mini ✅
   - Claude 3.5 Sonnet ✅
   - Gemini 1.5 Pro ✅

2. Tools configured:
   - Web browsing
   - Email (if needed)
   - File system
   - API integrations
```

### Example: Research + Report Agent

```
GOAL: "Setiap pagi, research 5 berita crypto terbaru, 
      generate summary, dan kirim ke email saya"

AI AGENTIC FLOW:
1. Browse crypto news sites
2. Extract 5 latest news
3. Generate summary for each
4. Compile into report
5. Send to email

CONFIG:
{
  "agentic": {
    "enabled": true,
    "model": "openai/gpt-4o",
    
    "tasks": {
      "crypto_news": {
        "trigger": "cron",
        "schedule": "0 7 * * *",
        
        "workflow": [
          {"action": "browse", "url": "https://coindesk.com"},
          {"action": "browse", "url": "https://cointelegraph.com"},
          {"action": "extract", "data": "headlines"},
          {"action": "summarize", "length": "short"},
          {"action": "send", "to": "email@client.com"}
        ]
      }
    }
  }
}
```

### Example: Auto-Order Follow-up

```
GOAL: "Kalo ada order baru, auto-confirm dan follow up 1 jam kemudian"

WORKFLOW:
1. Order received (webhook atau manual trigger)
2. AI generate confirmation message
3. Send via WhatsApp/Telegram to customer
4. Wait 1 hour
5. AI send follow-up: "Apakah barang sudah diterima?"

CONFIG:
{
  "automation": {
    "order_confirm": {
      "trigger": "webhook:new_order",
      
      "steps": [
        {"action": "generate_confirm", "template": "Terima kasih..."},
        {"action": "send_to_customer"},
        {"action": "schedule_followup", "delay": "1h"},
        {"action": "send_followup", "template": "Hallo..."}
      ]
    }
  }
}
```

---

# BAGIAN I: CONTOH REAL

---

## I1. CONTOH: E-COMMERCE FASHION

### Profile Bisnis

```
BUSINESS: Toko online fashion
PRODUCTS: Baju, celana, aksesoris
CHANNEL: WhatsApp + Telegram
VOLUME: 50-100 chats/day
TEAM: 1 owner + 2 staff
```

### Bot Configuration

```javascript
{
  "business": {
    "name": "Fashion House ID",
    "industry": "Fashion E-commerce",
    
    "contact": {
      "whatsapp": "+62812345678",
      "telegram": "@fashionhouseid",
      "instagram": "@fashionhouseid"
    },
    
    "hours": "09.00 - 21.00",
    "address": "Jl. Sudirman No. 123, Jakarta"
  },
  
  "knowledge": {
    "products": [
      {
        "category": "Dress",
        "items": [
          {"name": "Dress Floral Midi", "price": "Rp 350.000", "sizes": ["S","M","L"]},
          {"name": "Dress Casual Short", "price": "Rp 250.000", "sizes": ["S","M","L","XL"]}
        ]
      },
      {
        "category": "Atasan",
        "items": [
          {"name": "Blouse Office", "price": "Rp 280.000", "sizes": ["S","M","L"]},
          {"name": "Crop Top", "price": "Rp 150.000", "sizes": ["All"]}
        ]
      },
      {
        "category": "Celana",
        "items": [
          {"name": "High Waist Jeans", "price": "Rp 450.000", "sizes": ["26-32"]},
          {"name": "Kulot Pants", "price": "Rp 320.000", "sizes": ["S","M","L"]}
        ]
      }
    ],
    
    "shipping": [
      {"name": "JNE", "eta": "2-4 hari", "cost": "Based on weight"},
      {"name": "J&T", "eta": "2-5 hari", "cost": "Based on weight"},
      {"name": "SiCepat", "eta": "1-3 hari", "cost": "Based on weight"}
    ],
    
    "payment": ["BCA", "Mandiri", "BNI", "COD"],
    
    "faq": [
      {"q": "Jam berapa buka?", "a": "09.00 - 21.00 setiap hari"},
      {"q": "Berapa lama pengiriman?", "a": "1-5 hari tergantung ekspedisi"},
      {"q": "Bisa retur?", "a": "Bisa dalam 3 hari dengan video unboxing"},
      {"q": "Ada offline store?", "a": "Ya, Jl. Sudirman No. 123, Jakarta"},
      {"q": "Pakai app?", "a": "Bisa chat WhatsApp atau Telegram ini"}
    ]
  },
  
  "automation": {
    "order_confirm": {
      "trigger": "manual",
      "message": "Terima kasih! Pesanan {{product}} size {{size}} akan kami proses. Total: {{price}}. Mohon transfer ke BCA 123456789 a/n Fashion House. Konfirmasi setelah transfer ya!"
    },
    
    "shipping_notify": {
      "trigger": "after_payment_confirm",
      "message": "Pesanan sudah kami kirim via {{courier}} dengan resi {{tracking}}. ETA: {{eta}}"
    }
  }
}
```

### Bot Conversation Flow

```
CUSTOMER: "Halo, ada dress yang cocok untuk acara kantor?"

BOT: "Halo! Terima kasih sudah menghubungi Fashion House ID! 😊

Untuk acara kantor, kami recommend:
1. Blouse Office - Rp 280.000 (professional & nyaman)
2. Dress Floral Midi - Rp 350.000 (semi-formal tapi stylish)

Boleh tau preferensi lo?
- Warna favorit?
- Budget?
- Untuk acara formal atau casual office?"

CUSTOMER: "Blouse Office dong, warna putih ada?"

BOT: "Ada! ✅ Blouse Office warna White ready stock.

Details:
- Price: Rp 280.000
- Size: S, M, L (lo punya size apa?)
- Material: Katun premium (adem & nyaman buat daily)

Mau proceed atau mau tanya lagi?"

CUSTOMER: "Size M, mau pesan. Alamat Jaksel."

BOT: "Perfect! 📝 Order details:

Blouse Office White - Size M
Price: Rp 280.000

Shipping ke: Jaksel
Opsi ekspedisi:
1. JNE - 2-4 hari
2. J&T - 2-5 hari
3. SiCepat - 1-3 hari

Pilihan ekspedisi?"

CUSTOMER: "SiCepat aja"

BOT: "Siap! Total: Rp 280.000 + Ongkir

Silakan transfer ke:
🏦 BCA 123456789 a/n Fashion House

Kirim bukti transfer ya untuk确认!"

CUSTOMER: [sends transfer proof]

BOT: "Confirmed! ✅ Pesanan akan diproses.

预计 pengiriman 1-3 hari via SiCepat.
Kami akan kabari lagi setelah barang dikirim.

Terima kasih! 🙏"
```

---

## I2. CONTOH: RESTAURANT / WARUNG

### Profile

```
BUSINESS: Warung / Restaurant local
PRODUCTS: Makanan & minuman
CHANNEL: WhatsApp (primary)
VOLUME: 30-50 orders/day
SPECIAL: Delivery via GoFood/GrabFood
```

### Bot Configuration

```javascript
{
  "business": {
    "name": "Warteg Nusantara",
    "industry": "Restaurant",
    
    "location": "Jl. Merdeka No. 123, Jakarta",
    "hours": "10.00 - 22.00",
    "delivery": "GoFood, GrabFood, ShopeeFood"
  },
  
  "knowledge": {
    "menu": {
      "makanan": [
        {"name": "Nasi Goreng Special", "price": "Rp 35.000", "desc": "Nasi + telur + ayam suwir + sayur"},
        {"name": "Mie Goreng Jawa", "price": "Rp 30.000", "desc": "Mie + telur + sayuran"},
        {"name": "Ayam Geprek", "price": "Rp 38.000", "desc": "Ayam crispy + sambal geprek + nasi"},
        {"name": "Ayam Bakar", "price": "Rp 42.000", "desc": "Ayam bakar bumbu kecap + nasi"},
        {"name": "Pecel Lele", "price": "Rp 28.000", "desc": "Lele goreng + sambal + lalapan + nasi"}
      ],
      "minuman": [
        {"name": "Es Teh Manis", "price": "Rp 8.000"},
        {"name": "Teh Anget", "price": "Rp 6.000"},
        {"name": "Es Jeruk", "price": "Rp 10.000"},
        {"name": "Es Degan", "price": "Rp 12.000"},
        {"name": "Jus Alpukat", "price": "Rp 18.000"}
      ],
      "paket": [
        {"name": "Paket Hemat", "price": "Rp 40.000", "include": "Nasi Goreng + Es Teh"},
        {"name": "Paket Kenyang", "price": "Rp 55.000", "include": "Ayam Geprek + Nasi + Es Jeruk"}
      ]
    },
    
    "delivery": {
      "gofood": "Available - cek di app",
      "grabfood": "Available - cek di app", 
      "shopeefood": "Available - cek di app",
      "self_delivery": "Available dalam radius 5km, Rp 10.000"
    },
    
    "faq": [
      {"q": "Jam berapa buka?", "a": "10.00 - 22.00"},
      {"q": "Ada delivery?", "a": "Ya! Via GoFood, GrabFood, ShopeeFood. Atau delivery sendiri untuk radius 5km (Rp 10.000)"},
      {"q": "Bisa reservation?", "a": "Bisa! Untuk group 10+ orang, hubungi kami 1 hari sebelumnya."}
    ]
  }
}
```

### Bot Conversation Flow

```
CUSTOMER: "Mau pesan delivery"

BOT: "Halo! Selamat datang di Warteg Nusantara 🍛

Mau pesan apa hari ini?
Berikut menu best seller kami:
1. 🥇 Nasi Goreng Special - Rp 35.000
2. 🥈 Ayam Geprek - Rp 38.000
3. 🥉 Mie Goreng Jawa - Rp 30.000

Atau mau liat menu lengkap?"

CUSTOMER: "Nasi Goreng Special + Ayam Geprek + 2 Es Teh"

BOT: "Perfect! 📝 Order:

1. Nasi Goreng Special - Rp 35.000
2. Ayam Geprek - Rp 38.000
3. Es Teh Manis x2 - Rp 16.000

Subtotal: Rp 89.000

Untuk delivery, options:
1. Via GoFood/GrabFood/ShopeeFood (order di app aja ya)
2. Delivery langsung (radius 5km, Rp 10.000)

Pilih option?"

CUSTOMER: "Delivery langsung aja"

BOT: "Siap! 📍

Mohon info:
- Nama pemesan:
- Alamat lengkap:
- No HP:

(Delivery langsung untuk Jaksel ya)"

CUSTOMER: "Nama: Budi, Alamat: Jl. Melati No. 5 Jaksel, HP: 0812345678"

BOT: "Confirmed! ✅

📦 Order Summary:
- Nasi Goreng Special - Rp 35.000
- Ayam Geprek - Rp 38.000
- Es Teh Manis x2 - Rp 16.000
- Delivery fee - Rp 10.000
─────────────────────
TOTAL: Rp 99.000

📍 Delivery ke: Jl. Melati No. 5 Jaksel
👤 Nama: Budi
📱 HP: 0812345678

Estimated arrival: 45-60 menit

Silakan transfer ke:
🏦 BCA 987654321 a/n Warteg Nusantara

Konfirmasi setelah transfer ya! 🙏"
```

---

## I3. CONTOH: FREELANCE SERVICE

### Profile

```
BUSINESS: Freelance AI Consultant
SERVICES: Setup AI Bot, Automation, Consulting
CHANNEL: Telegram (more professional)
CLIENTS: SME, business owners
SPECIAL: Remote work, global clients
```

### Bot Configuration

```javascript
{
  "business": {
    "name": "AI Solutions by Fajar",
    "industry": "AI Consulting & Development",
    
    "contact": {
      "telegram": "@fajar_ai",
      "email": "fajar@aisolutions.id",
      "web": "www.aisolutions.id"
    },
    
    "hours": "09.00 - 18.00 (Mon-Fri)",
    "timezone": "Asia/Jakarta"
  },
  
  "knowledge": {
    "services": [
      {
        "name": "AI Bot Setup",
        "price": "Rp 300.000 - 1.500.000",
        "description": "Setup AI assistant atau business bot dengan WhatsApp/Telegram",
        "timeline": "1-3 hari",
        "includes": ["VPS setup", "Channel integration", "AI model config", "Basic training"]
      },
      {
        "name": "Business Automation", 
        "price": "Rp 500.000 - 2.000.000",
        "description": "Automation workflows, cron jobs, auto-responders",
        "timeline": "3-7 hari",
        "includes": ["Workflow analysis", "Automation setup", "Testing", "Documentation"]
      },
      {
        "name": "AI Consulting",
        "price": "Rp 150.000/jam",
        "description": "Konsultasi AI untuk bisnis, strategy, implementation",
        "format": "Online meeting via Google Meet/Zoom"
      },
      {
        "name": "Monthly Maintenance",
        "price": "Rp 100.000 - 250.000/bulan",
        "description": "Monitoring, updates, troubleshooting",
        "includes": ["24/7 monitoring", "Weekly reports", "Priority support"]
      }
    ],
    
    "process": [
      "1. Initial consultation (free 15 min)",
      "2. Project scoping & quotation",
      "3. Down payment (50%)",
      "4. Development & testing",
      "5. Demo & revisions",
      "6. Final payment (50%)",
      "7. Deployment & handover"
    ],
    
    "portfolio": [
      "E-commerce bot untuk Fashion House ID (50+ orders/day)",
      "CS Automation untuk Crypto signal provider",
      "Personal AI Assistant untuk 10+ professionals"
    ],
    
    "faq": [
      {"q": "Berapa lama setup?", "a": "Basic: 1-2 hari, Standard: 3-5 hari, Premium: 1-2 minggu"},
      {"q": "Ada garansi?", "a": "Ya, 30 hari garansi untuk bug fixes setelah deployment"},
      {"q": "Bisa custom?", "a": "Tentu! Setiap bisnis beda, kita custom sesuai kebutuhan"},
      {"q": "Training disediakan?", "a": "Ya, included free training & documentation"}
    ]
  }
}
```

### Bot Conversation Flow

```
CLIENT: "Halo, mau tanya soal AI bot untuk bisnis saya"

BOT: "Halo! 👋 Terima kasih sudah menghubungi.

Saya Fajar, konsultan AI yang bantu bisnis² di Indonesia pake AI automation.

Boleh tau:
1. Bisnis apa yang lo jalankan?
2. Challenge apa yang mau lo solve dengan AI?
3. Udah pernah pake AI sebelumnya?

Ini biar saya bisa kasih rekomendasi yang pas untuk bisnis lo."

CLIENT: "Saya punya toko online fashion, mau AI buat CS. Jadi kalau customer nanya2 soal produk, shipping, dll bisa auto reply."

BOT: "Oke cool! 🎯

CS Bot itu perfect buat online shop seperti lo.

Benefit CS Bot untuk Toko Online:
✅ Auto-reply 24/7 (lo tidur bot tetap jawab)
✅ Instant response (gak perlu nunggu balasan)
✅ Handle pertanyaan umum (harga, stock, shipping)
✅ Bisa handle multiple customers sekaligus
✅ Konsisten serviceeven lo lagi sibuk

Estimasi Harga untuk CS Bot:

BASIC (Rp 300.000):
- 1 channel (WA atau Telegram)
- Basic FAQ
- Responsi umum

STANDARD (Rp 500.000):
- 2 channels
- Knowledge base produk
- Order follow-up
- Basic automation

PREMIUM (Rp 750.000):
- Full setup
- Multiple platforms
- Advanced automation
- Priority support

Lo mau yang mana atau mau kita diskusiin lebih lanjut?"

CLIENT: "Standard dong. Include apa aja?"

BOT: "Perfect! Ini yang lo dapat di paket Standard: 📋

✅ VPS Setup (server 24/7)
✅ WhatsApp + Telegram integration
✅ Knowledge base (produk, harga, FAQ lo)
✅ CS personality configuration
✅ Auto-reply untuk pertanyaan umum
✅ Order confirmation automation
✅ Basic analytics dashboard
✅ Free training 30 menit
✅ 30 hari garansi

Timeline: 3-5 hari kerja

Proses:
1. Kita diskusiin detail kebutuhan
2. Saya setup & test
3. Demo ke lo
4. Revisi jika perlu
5. Deploy & handover

Pertanyaan sebelum proceed?"

CLIENT: "Gimana caranya bayar?"

BOT: "Gampang! 💳

Payment Methods:
- BCA: 123456789 a/n Fajar Alamsyah
- GoPay / OVO: 0812345678
- Wise / PayPal: (for international clients)

Terms:
- 50% upfront (untuk mulai project)
- 50%剩下 saat handover

Contoh:
Total: Rp 500.000
- Down payment: Rp 250.000 (now)
- Pelunasan: Rp 250.000 (saat bot deployed)

Kalo agree, kita mulai dengan kickoff meeting untuk ngumpulin info bisnis lo. Ready?"
```

---

## I4. CONTOH: CRYPTO TRADING BOT

### Profile

```
BUSINESS: Crypto signal provider
SERVICES: Trading signals, portfolio tracking
CHANNEL: Telegram (multiple groups)
VOLUME: 1000+ members
SPECIAL: Real-time alerts, auto-trading option
```

### Bot Configuration

```javascript
{
  "business": {
    "name": "CryptoSignals Pro",
    "industry": "Crypto Trading Signals",
    
    "channels": {
      "free_channel": "@cryptosignalsfree",
      "premium_channel": "@cryptosignalspro",
      "announcements": "@cryptosignalsann"
    },
    
    "contact": "@cryptosignals_support"
  },
  
  "knowledge": {
    "tier": {
      "free": {
        "features": [
          "Daily market analysis",
          "Basic signals (BTC, ETH)",
          "Community access"
        ],
        "price": "FREE"
      },
      "premium": {
        "price": "Rp 150.000/bulan",
        "features": [
          "All free features",
          "Real-time signals (24/7)",
          "Altcoin gems",
          "Entry/exit points",
          "Portfolio management",
          "Priority support"
        ]
      }
    },
    
    "signal_format": {
      "example": "🟢 BTC/USDT\nEntry: $67,500\nTarget 1: $68,500\nTarget 2: $70,000\nStop Loss: $66,500\nRisk: MEDIUM\nTimeframe: 4H"
    },
    
    "trading_pairs": ["BTC/USDT", "ETH/USDT", "BNB/USDT", "SOL/USDT", "Various altcoins"]
  },
  
  "automation": {
    "daily_analysis": {
      "cron": "0 8 * * *",
      "action": "Generate & post daily market analysis"
    },
    
    "weekly_report": {
      "cron": "0 9 * * 0",
      "action": "Post weekly performance report"
    },
    
    "price_alert": {
      "trigger": "price_movement",
      "condition": "BTC moves > 5% in 1h",
      "action": "Send urgent alert to all channels"
    }
  }
}
```

### Bot Features

```
CRYPTO BOT FEATURES:

1. 📊 DAILY ANALYSIS (Automated)
   - Market overview
   - Key levels
   - Trend analysis
   - Risk assessment

2. 📈 SIGNAL DELIVERY
   - Entry/exit points
   - Stop loss
   - Risk/reward ratio
   - Position sizing guide

3. ⏰ REAL-TIME ALERTS
   - Price movement alerts
   - Breakout alerts
   - Whale activity detection

4. 📉 PORTFOLIO TRACKING
   - Track user holdings
   - P&L calculation
   - Performance metrics

5. 🎓 EDUCATIONAL CONTENT
   - Trading tips
   - Risk management
   - Technical analysis basics

6. 🤖 AUTO-TRADING (Premium)
   - Connect to exchange
   - Execute trades automatically
   - Dollar-cost averaging
```

---

## I5. CONTOH: PERSONAL ASSISTANT

### Profile

```
USER: Professional / Entrepreneur
PURPOSE: Personal productivity
CHANNEL: WhatsApp (24/7 available)
USAGE: 20-50 interactions/day
```

### Bot Configuration

```javascript
{
  "personal": {
    "owner": "Fajar Alamsyah",
    "role": "Personal AI Assistant",
    
    "channels": {
      "primary": "WhatsApp",
      "backup": "Telegram"
    },
    
    "timezone": "Asia/Jakarta",
    "work_hours": "Flexible (owner lifestyle)"
  },
  
  "ai": {
    "personality": {
      "name": "Aira",
      "tone": "Casual, direct, efficient",
      "style": "Seperti ngobrol sama teman yang emang pinter",
      
      "traits": [
        "Proactive - kasitau hal penting tanpa ditanya",
        "Direct - to the point, no fluff",
        "Resourceful - cari solusi dulu sebelum nanya",
        "Helpful but not annoying"
      ],
      
      "language": "Bahasa Indonesia & English (bilingual)"
    },
    
    "capabilities": {
      "research": {
        "enabled": true,
        "description": "Cari info, summarize articles, comparison shopping"
      },
      
      "writing": {
        "enabled": true,
        "description": "Draft emails, messages, proposals, documents"
      },
      
      "scheduling": {
        "enabled": true,
        "description": "Manage calendar, set reminders, schedule meetings"
      },
      
      "coding": {
        "enabled": true,
        "description": "Help with scripts, automation, technical tasks"
      },
      
      "research": {
        "enabled": true,
        "description": "Market research, competitor analysis, trends"
      },
      
      "personal": {
        "enabled": true,
        "description": "Travel planning, gift ideas, restaurant recommendations"
      }
    }
  },
  
  "automation": {
    "morning_brief": {
      "cron": "0 7 * * *",
      "action": "Morning summary: weather, schedule, important alerts"
    },
    
    "evening_summary": {
      "cron": "0 21 * * *",
      "action": "End of day summary: pending tasks, tomorrow's schedule"
    },
    
    "reminder_check": {
      "cron": "0 */4 * * *",
      "action": "Check pending reminders, send if due"
    }
  }
}
```

### Daily Interaction Examples

```
MORNING (7 AM - Auto):

📱 AI: "Good morning Fajar! ☀️

Weather: ☁️ Jakarta, 28°C, humidity 75%
Chance of rain in the afternoon

📅 Today's Schedule:
- 9:00 AM: Meeting with client A
- 2:00 PM: Call with team
- 5:00 PM: Gym

⚡ Quick Hits:
- Crypto: BTC up 2.3% overnight
- News: [Headline summary]

Ada yang perlu saya prepare sebelum meeting 9 AM?"

────────────────────────────────────────────

USER: "Research competitors untuk project baru"

AI: "Siap, gue research dulu. Sabar bentar... 🔍

[5 minutes later]

Ketemu! Ini competitors untuk [project type]:

TOP 3:
1. Competitor A
   - Website: www.competitorA.com
   - Price: Rp X
   - Strengths: [list]
   - Weaknesses: [list]

2. Competitor B
   - Website: www.competitorB.com
   - Price: Rp Y
   - Strengths: [list]
   - Weaknesses: [list]

3. Competitor C
   - Website: www.competitorC.com
   - Price: Rp Z
   - Strengths: [list]
   - Weaknesses: [list]

💡 KEY INSIGHTS:
- Market lagi [trend]
- Gap yang bisa dimasuki: [opportunity]

Mau gue dalamin aspek tertentu?"

────────────────────────────────────────────

USER: "Bantu draft email ke client soal progress project"

AI: "Gas! 📧

Kirim ke siapa & subject apa?"

USER: "Ke Pak Budi, subject: Update Progress Project X"

AI: "Siap. Ini draftnya:

---

Subject: Update Progress - Project X

Pak Budi,

Berikut update progress Project X per hari ini:

✅ COMPLETED:
- Milestone 1
- Milestone 2

🔄 IN PROGRESS:
- Milestone 3 (80% done, ETA: 2 hari)

⏳ UPCOMING:
- Milestone 4
- Milestone 5

Jika ada вопросы atau perubahan, lets discuss.

Best regards,
Fajar

---

Mau gue adjust tone-nya (lebih formal/casual) atau tambah/kurang detail?"

────────────────────────────────────────────

USER: "Thanks, looks good. Send it."

AI: "Sent! ✅ 

Cc juga ke siapa? Atau langsung ke Pak Budi aja?"

USER: "Ke Budi aja"

AI: "Done! ✉️ Sent to Pak Budi. 

Ada lagi yang perlu gue handle?"
```

---

# BAGIAN J: SERVICE & PRICING

---

## J1. PAKET SERVICE UNTUK CLIENT

### Overview

```
SERVICE YANG LO TAWARKAN SEBAGAI PROVIDER:

1. SETUP FEE (sekali bayar)
   → Buat install & configure bot

2. MONTHLY MAINTENANCE (per bulan)
   → Buat monitoring & updates

3. ADDITIONAL SERVICES (opsional)
   → Custom features, extra channels, dll
```

### Paket Setup

| Paket | Harga | Waktu | Channels | AI Model | Knowledge Base |
|-------|-------|-------|----------|----------|---------------|
| **Basic** | Rp 200.000 | 1-2 jam | 1 | Basic | Basic FAQ |
| **Standard** | Rp 400.000 | 2-3 jam | 2 | Good | Products + FAQ |
| **Premium** | Rp 750.000 | 3-5 jam | All | Premium | Full + Custom |

### Paket Maintenance

| Paket | Harga/Bulan | Monitoring | Updates | Support |
|-------|-------------|------------|---------|---------|
| **Basic** | Rp 100.000 | ✅ | ✅ | Chat only |
| **Standard** | Rp 150.000 | ✅ | ✅ | + Email |
| **Premium** | Rp 250.000 | ✅ | ✅ | + Priority |

### Paket Add-ons

| Add-on | Harga | Description |
|--------|-------|-------------|
| Extra Channel | Rp 100.000 | Add WhatsApp/Telegram/Discord |
| Extra Knowledge | Rp 50.000 | Tambah 50 produk/items |
| Custom Feature | Rp 150.000+ | Based on complexity |
| Training Session | Rp 50.000/jam | Training untuk client team |

---

## J2. CONTOH QUOTATION LENGKAP

### Quotation: Personal AI Assistant

```
╔══════════════════════════════════════════════════════╗
║                   QUOTATION                           ║
║               Personal AI Assistant                    ║
╠══════════════════════════════════════════════════════╣
║                                                              ║
║  From: Fajar Alamsyah                                      ║
║  To: [Client Name]                                          ║
║  Date: April 5, 2026                                        ║
║                                                              ║
╠════════════════════════════════════════════════════════════╣
║  SERVICES                                                   ║
╠════════════════════════════════════════════════════════════╣
║                                                              ║
║  1. SETUP FEE (One-time)                                    ║
║  ─────────────────────────────────────────────────────────   ║
║  • VPS Configuration (24/7 server)            Rp 100.000    ║
║  • OpenClaw Installation & Setup             Rp 100.000    ║
║  • WhatsApp Integration                       Rp  50.000    ║
║  • Telegram Integration                       Rp  50.000    ║
║  • AI Model Configuration (MiniMax)           Rp  50.000    ║
║  • Personality & Instructions Setup          Rp  75.000    ║
║  • Testing & Deployment                       Rp  75.000    ║
║                                                   ─────────  ║
║  SUBTOTAL SETUP                               Rp 500.000    ║
║                                                              ║
║  2. MONTHLY MAINTENANCE                                        ║
║  ─────────────────────────────────────────────────────────   ║
║  • Server Monitoring & Updates               Rp  50.000    ║
║  • AI Model API cost (estimate)             Rp  25.000    ║
║  • Bug fixes & Support                       Rp  50.000    ║
║                                                   ─────────  ║
║  SUBTOTAL MONTHLY                             Rp 125.000    ║
║                                                              ║
╠════════════════════════════════════════════════════════════╣
║  PAYMENT TERMS:                                              ║
║  • 50% upfront (to start project)                            ║
║  • 50% upon completion                                        ║
║  • Monthly: Paid in advance                                  ║
╠════════════════════════════════════════════════════════════╣
║  TIMELINE:                                                   ║
║  • Setup: 2-3 working days                                    ║
║  • Deployment: Day 4                                         ║
╠════════════════════════════════════════════════════════════╣
║                                                              ║
║  TOTAL FIRST MONTH: Rp 625.000                               ║
║  TOTAL NEXT MONTHS: Rp 125.000                               ║
║                                                              ║
╚════════════════════════════════════════════════════════════╝
```

### Quotation: Business CS Bot

```
╔══════════════════════════════════════════════════════════════╗
║                   QUOTATION                                   ║
║               Business CS Bot (Standard)                      ║
╠══════════════════════════════════════════════════════════════╣
║                                                              ║
║  From: Fajar Alamsyah                                        ║
║  To: [Business Name]                                         ║
║  Date: April 5, 2026                                         ║
║                                                              ║
╠════════════════════════════════════════════════════════════╣
║  SERVICES                                                    ║
╠════════════════════════════════════════════════════════════╣
║                                                              ║
║  1. SETUP FEE (One-time)                                      ║
║  ─────────────────────────────────────────────────────────   ║
║  • VPS Configuration (24/7 server)            Rp 100.000    ║
║  • OpenClaw Installation                      Rp  75.000    ║
║  • WhatsApp Integration                       Rp  75.000    ║
║  • Telegram Integration                       Rp  75.000    ║
║  • AI Model Configuration (GPT-4o Mini)       Rp  75.000    ║
║  • Business Knowledge Base Setup              Rp 150.000    ║
║  • CS Personality Configuration                Rp 100.000    ║
║  • Automation Rules Setup                      Rp 100.000    ║
║  • Testing & QA                                Rp  75.000    ║
║  • Training & Documentation                    Rp  75.000    ║
║                                                    ─────────  ║
║  SUBTOTAL SETUP                               Rp 900.000    ║
║                                                              ║
║  NOTE: VPS cost (Rp 100.000/bulan) excluded -               ║
║        client beli terpisah atau gunakan ours @cost         ║
║                                                              ║
║  2. MONTHLY MAINTENANCE                                       ║
║  ─────────────────────────────────────────────────────────   ║
║  • Server Monitoring & Updates                 Rp  50.000    ║
║  • AI Model API (estimate, based on volume)     Rp  75.000    ║
║  • Knowledge Base Updates (monthly)            Rp  25.000    ║
║  • Priority Support                            Rp  50.000    ║
║                                                    ─────────  ║
║  SUBTOTAL MONTHLY                             Rp 200.000    ║
║                                                              ║
╠════════════════════════════════════════════════════════════╣
║  WHAT'S INCLUDED:                                            ║
║  ✅ 24/7 AI Customer Service                                  ║
║  ✅ Auto-reply untuk FAQ                                      ║
║  ✅ Product inquiry handling                                  ║
║  ✅ Order confirmation automation                             ║
║  ✅ Multi-channel (WhatsApp + Telegram)                      ║
║  ✅ Monthly performance report                               ║
║  ✅ Unlimited conversations                                   ║
║  ✅ 30-day warranty on bugs                                   ║
╠════════════════════════════════════════════════════════════╣
║  PAYMENT TERMS:                                              ║
║  • 50% upfront to start                                       ║
║  • 50% upon completion                                        ║
║  • Monthly: Paid in advance                                   ║
╠════════════════════════════════════════════════════════════╣
║  TIMELINE:                                                   ║
║  • Kickoff & data collection: Day 1                          ║
║  • Development: Day 2-4                                       ║
║  • Testing & revisions: Day 5                                ║
║  • Deployment: Day 6                                          ║
╠════════════════════════════════════════════════════════════╣
║                                                              ║
║  TOTAL FIRST MONTH: Rp 1.000.000                             ║
║  TOTAL NEXT MONTHS: Rp 200.000                               ║
║                                                              ║
╚════════════════════════════════════════════════════════════╝
```

---

## J3. CARA GET CLIENTS

### Strategy 1: Personal Network

```
DIMULAI DARI LINGKARAN TERDEKAT:

1. Family & Friends
   - Tanya siapa yang punya bisnis
   - Offer trial / discounted price
   - Minta referral

2. Social Media Personal
   - Post tentang services lo
   - Share results & testimonials
   - Engage dengan interested people

3. WhatsApp Status
   - Update regularly tentang AI services
   - Share demo videos
   - Post testimonials
```

### Strategy 2: Content Marketing

```
BUAT CONTENT YANG BERMANFAAT:

Platforms:
- LinkedIn: Professional content
- Instagram: Demo videos, infographics
- Twitter/X: Quick tips, insights
- TikTok: Viral potential (AI demos)

Content Types:
- Tutorial: "How to setup AI CS Bot"
- Case study: "Hasil bot untuk client X"
- Tips: "5 ways AI bisa hemat biaya bisnis"
- Demo: Video bot working real-time
- Behind scenes: Process & setup
```

### Strategy 3: Community Involvement

```
JOIN COMMUNITIES:

1. Business Communities
   - Entrepreneur groups
   - SME associations
   - Industry-specific groups

2. Crypto/Tech Communities
   - Discord servers
   - Telegram groups
   - Reddit

3. Freelancer Communities
   - Freelancer Indonesia
   - Digital nomad groups

APPROACH:
- Be helpful, not salesy
- Share knowledge
- Answer questions
- Build reputation
- Then offer services
```

### Strategy 4: Cold Outreach

```
JANGKAU TARGET YANG TEPAT:

1. Identify Potential Clients
   - Online shop tanpa CS automation
   - Business yang reply manual 24/7
   - Companies dengan high volume inquiries

2. Research
   - Cek social media
   - Liat review & complaints (market gap)
   - Understand business model

3. Personalized Outreach
   - Reference something specific
   - Offer value first
   - Propose meeting/call

EXAMPLE MESSAGE:

"Halo [Name],

Saya lihat [Business] lagi grow pesat - selamat! 🎉

Saya заметил bahwa response time ke customer masih manual. 

Saya bantu bisnis similar dengan AI CS Bot yang bisa:
✅ Auto-reply 24/7
✅ Handle pertanyaan umum
✅ Proses order otomatis

Boleh saya kirim demo ke [Business]? free, no obligation.

Best,
[Fajar]"
```

### Strategy 5: Referral Program

```
INCENTIVIZE REFERRALS:

Existing Client:
- Discount bulan depan untuk setiap referral
- Example: "Temen lo jadi client = lo dapat 1 bulan free"

Partner/Affiliate:
- Commission per referral (10-20%)
- Example: 20% dari first month payment
```

---

## J4. PRICING STRATEGY

### Stage 1: Building Portfolio (Month 1-3)

```
TARGET: Get first 5 clients & build testimonials

PRICING:
- Basic: Rp 200.000 (low barrier)
- Standard: Rp 300.000 (discounted from 400k)
- Premium: Rp 500.000 (discounted from 750k)

WHY LOW:
- Need testimonials
- Need portfolio
- Learning curve (lo juga masih belajar)
- Accept smaller profit for experience

GOALS:
✅ 5 happy clients
✅ 5 testimonials
✅ Case studies
✅ Referrals
```

### Stage 2: Established (Month 4-6)

```
TARGET: Increase prices, maintain quality

PRICING:
- Basic: Rp 300.000
- Standard: Rp 500.000
- Premium: Rp 750.000

WHY INCREASE:
- Sudah punya portfolio
- Process udah streamlined
- Lebih cepat selesai
- Quality proven

GOALS:
✅ 10-15 active clients
✅ Recurring revenue
✅ Efficient processes
```

### Stage 3: Premium Provider (Month 7+)

```
TARGET: Position as premium, command higher prices

PRICING:
- Basic: Rp 400.000
- Standard: Rp 750.000
- Premium: Rp 1.500.000+

ADD SERVICES:
- Custom development
- Enterprise solutions
- Ongoing consulting

WHY HIGHER:
- Reputation
- Limited slots ( scarcity)
- Higher quality (time invested)
- Premium positioning

GOALS:
✅ 20+ clients
✅ Waitlist
✅ Premium brand
✅ Higher margins
```

---

# BAGIAN K: TROUBLESHOOTING & SECURITY

---

## K1. TROUBLESHOOTING

### Common Issues & Solutions

| Problem | Likely Cause | Solution |
|---------|-------------|----------|
| Bot offline | PM2 stopped | `pm2 restart openclaw` |
| Bot slow | High load / bad model | Check `htop`, switch model |
| WhatsApp disconnected | Session expired | Re-scan QR code |
| WhatsApp can't connect | Network/firewall | Check VPS firewall, restart |
| Telegram no response | Wrong token | Verify token in config |
| AI responses wrong | Wrong model/config | Check model settings |
| No internet on VPS | Network issue | `ping google.com` |
| VPS unreachable | Server down / firewall | Check DigitalOcean console |
| High memory usage | Too many processes | `pm2 list`, restart if needed |
| High CPU | AI model processing | Normal if short spike |

### Diagnostic Commands

```
CHECK BOT STATUS:
pm2 list
pm2 logs openclaw --lines 50

CHECK RESOURCES:
htop
# CPU > 80% = high load
# RAM > 90% = not enough memory

CHECK NETWORK:
ping google.com
curl -I http://localhost:18789

CHECK LOGS:
pm2 logs openclaw --err --lines 100

RESTART EVERYTHING:
pm2 restart openclaw
```

---

## K2. SECURITY

### VPS Security Checklist

```
SEKURITI VPS:

1. UPDATE REGULER
   apt update && apt upgrade -y

2. GANTI PORT SSH (optional tapi recommended)
   - Default port 22 → ganti ke 2222
   - Edit: /etc/ssh/sshd_config
   - Port 2222
   - service ssh restart

3. INSTALL FAIL2BAN
   apt install -y fail2ban
   - Prevents brute force attacks
   - Auto-blocks suspicious IPs

4. FIREWALL (UFW)
   ufw allow 22      # SSH
   ufw allow 80      # HTTP
   ufw allow 443     # HTTPS
   ufw allow 18789   # OpenClaw port
   ufw enable

5. ROOT LOGIN DISABLE (recommended for production)
   - Buat user baru
   - Sudo access
   - Disable direct root login
```

### Hardening Script

```bash
#!/bin/bash
# security-hardening.sh

echo "Starting security hardening..."

# Update
apt update && apt upgrade -y

# Install fail2ban
apt install -y fail2ban

# Setup basic firewall
ufw default deny incoming
ufw default allow outgoing
ufw allow 22
ufw allow 80
ufw allow 443
ufw allow 18789
ufw --force enable

# Secure SSH
sed -i 's/#Port 22/Port 2222/' /etc/ssh/sshd_config
sed -i 's/#PermitRootLogin yes/PermitRootLogin no/' /etc/ssh/sshd_config
systemctl restart sshd

echo "Security hardening complete!"
```

---

## K3. API KEY SECURITY

```
DO's:
✅ Store API keys in environment variables
✅ Use separate keys per service
✅ Rotate keys periodically (every 3-6 months)
✅ Use read-only permissions when possible
✅ Monitor usage for anomalies

DON'Ts:
❌ Commit API keys to git
❌ Share keys in plain text
❌ Use same key for everything
❌ Give full access when not needed
❌ Store in code (use config file)
```

### Proper API Key Storage

```bash
# Use environment variables
export OPENAI_API_KEY="sk-xxxx"
export MINIMAX_API_KEY="xxxx"

# Or use .env file
nano ~/.env
# Add keys there
# Then in code: process.env.OPENAI_API_KEY

# NEVER do this:
# echo "apiKey: sk-xxxx" >> ~/.openclaw/config.json
```

---

## K4. COMMANDS REFERENCE

### Essential Commands

```bash
# ===================
# SSH & CONNECTIVITY
# ===================
ssh root@IP_VPS              # Connect to VPS
exit                         # Disconnect

# ===================
# SYSTEM UPDATES
# ===================
apt update && apt upgrade -y # Update packages

# ===================
# OPENCLAW
# ===================
openclaw --version           # Check version
openclaw start              # Start bot
openclaw stop               # Stop bot
openclaw restart            # Restart bot
openclaw status             # Check status
openclaw logs               # View logs
openclaw config edit        # Edit config

# ===================
# PM2 PROCESS MANAGER
# ===================
pm2 list                     # List all processes
pm2 status                   # Quick status
pm2 logs openclaw            # View bot logs
pm2 logs openclaw --err      # Error logs only
pm2 logs --lines 100         # Last 100 lines
pm2 restart openclaw         # Restart bot
pm2 stop openclaw            # Stop bot
pm2 monit                    # Real-time monitor
pm2 startup                 # Setup auto-start
pm2 save                     # Save current state

# ===================
# SYSTEM MONITORING
# ===================
htop                        # Interactive process view
top                         # Simple process view
df -h                       # Disk usage
free -m                     # Memory usage
uptime                      # Server uptime

# ===================
# NETWORK
# ===================
ping google.com             # Test connectivity
curl http://localhost:18789  # Test local
netstat -tlnp               # Listening ports

# ===================
# FILE EDITING
# ===================
nano file.txt               # Edit with nano
cat file.txt                # View file
ls -la                      # List files
```

---

# BAGIAN L: QUICK START SUMMARY

---

## TL;DR - Step by Step

```
MINIMAL SETUP (30 MENIT):

1. Beli VPS (DigitalOcean $6)           → 10 menit
2. Connect via SSH                       → 5 menit
3. Install OpenClaw                      → 5 menit
4. Setup PM2 auto-start                  → 2 menit
5. Setup Telegram Bot                    → 5 menit
6. Configure AI Model                    → 3 menit
7. Test & Verify                         → 5 menit

TOTAL: ~30-45 menit
COST: Rp 60.000 (VPS bulan pertama)
```

---

## Checklist

```
PRE-SETUP:
□ VPS sudah aktif (DigitalOcean/Vultr/etc)
□ SSH credentials received
□ AI Model API key ready (MiniMax/GPT-4o Mini)

SETUP STEPS:
□ Connect to VPS via SSH
□ apt update && upgrade
□ Install Node.js 18+
□ npm install -g openclaw
□ openclaw init
□ openclaw start
□ Install PM2: npm install -g pm2
□ pm2 start openclaw --name openclaw
□ pm2 startup && pm2 save
□ Setup Telegram Bot (get token from BotFather)
□ Configure AI Model in OpenClaw
□ Verify bot responds

POST-SETUP:
□ Test from another Telegram account
□ Setup auto-restart (PM2 already done)
□ Document credentials somewhere safe
□ Monitor first 24 hours
```

---

# PENUTUP

## Yang Sudah Kamu Pelajari

```
SETELAH BACA PANDUAN INI:

✅ Paham perbedaan AI → AI Agentic → AGI → ASI
✅ Tahu tools yang dibutuhkan
✅ Bisa setup VPS dari 0
✅ Bisa connect dari laptop atau HP
✅ Bisa install & configure OpenClaw
✅ Bisa setup WhatsApp & Telegram
✅ Bisa configure AI model
✅ Bisa setup Personal AI Assistant
✅ Bisa setup Business CS Bot
✅ Bisa setup Automation/Cron
✅ Paham pricing untuk client
✅ Tahu cara get clients
✅ Tau security basics
✅ Bisa troubleshoot common issues
```

## Langkah Selanjutnya

```
UNTUK START:

1. 🚀 Setup VPS pertama lo (DigitalOcean $6)
2. 📱 Install OpenClaw
3. 💬 Setup Telegram Bot
4. 🤖 Configure AI Model
5. 🧪 Test dengan chat ke bot
6. 📢 Share ke teman/pasang harga
7. 🔄 Improve based on feedback

INGAT:
- Starting is the hardest part
- Each bot you build = experience
- First client may take time
- Keep learning & improving
```

---

## Resource Links

```
TOOLS:
- OpenClaw: https://openclaw.ai
- DigitalOcean: https://digitalocean.com
- Vultr: https://vultr.com
- Node.js: https://nodejs.org

AI MODELS:
- MiniMax: https://minimax.io
- OpenAI: https://platform.openai.com
- Google AI: https://aistudio.google.com
- Anthropic: https://www.anthropic.com

COMMUNITY:
- OpenClaw Discord
- AI Indonesia Telegram Group
- Crypto/Tech Communities

DOCUMENTATION:
- OpenClaw Docs: docs.openclaw.ai
- This Guide: [repository URL]
```

---

## Contact & Support

```
QUESTIONS?

- Via GitHub Issues (if using repo)
- Via DM on Telegram

FOUND ERRORS?

- Submit correction
- PR welcome

WANT TO CONTRIBUTE?

- PRs welcome
- Share your learnings
- Help others in community
```

---

**Versi final: April 2026**
**Last updated: April 5, 2026**
**By: Aira ⚡**

---

© 2026 AI POWER AUTOMATION SERVICE GUIDE
Build with ❤️ for aspiring AI Service Providers in Indonesia

