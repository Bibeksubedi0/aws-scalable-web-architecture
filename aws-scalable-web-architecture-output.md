# 📁 PROJECT EXPORT FOR LLMs

## 📊 Project Information

- **Project Name**: `aws-scalable-web-architecture`
- **Generated On**: 2026-04-01 05:33:50 (Asia/Katmandu / GMT+06:45)
- **Total Files Processed**: 11
- **Export Tool**: Easy Whole Project to Single Text File for LLMs v1.1.0
- **Tool Author**: Jota / José Guilherme Pandolfi

### ⚙️ Export Configuration

| Setting | Value |
|---------|-------|
| Language | `en` |
| Max File Size | `1 MB` |
| Include Hidden Files | `false` |
| Output Format | `both` |

## 🌳 Project Structure

```
├── 📁 Docs/
│   ├── 📄 architecture.md (685 B)
│   ├── 📄 commands.md (344 B)
│   └── 📄 steps.md (858 B)
├── 📁 Screenshots/
│   ├── 📄 ALB-working.png (199.75 KB)
│   ├── 📄 ec2-running.png (192.44 KB)
│   ├── 📄 ec2-website.png (3.79 MB)
│   └── 📄 target-group-healthy.png (139.19 KB)
├── 📁 scripts/
│   └── 📄 setup_nginx.sh (111 B)
├── 📁 website/
│   ├── 📄 error.html (870 B)
│   └── 📄 index.html (123.38 KB)
└── 📄 README.md (1.43 KB)
```

## 📑 Table of Contents

**Project Files:**

- [📄 Docs/architecture.md](#📄-docs-architecture-md)
- [📄 Docs/commands.md](#📄-docs-commands-md)
- [📄 Docs/steps.md](#📄-docs-steps-md)
- [📄 scripts/setup_nginx.sh](#📄-scripts-setup-nginx-sh)
- [📄 website/error.html](#📄-website-error-html)
- [📄 website/index.html](#📄-website-index-html)
- [📄 README.md](#📄-readme-md)

---

## 📈 Project Statistics

| Metric | Count |
|--------|-------|
| Total Files | 11 |
| Total Directories | 4 |
| Text Files | 7 |
| Binary Files | 4 |
| Total Size | 4.44 MB |

### 📄 File Types Distribution

| Extension | Count |
|-----------|-------|
| `.md` | 4 |
| `.png` | 4 |
| `.html` | 2 |
| `.sh` | 1 |

## 💻 File Code Contents

### <a id="📄-docs-architecture-md"></a>📄 `Docs/architecture.md`

**File Info:**
- **Size**: 685 B
- **Extension**: `.md`
- **Language**: `text`
- **Location**: `Docs/architecture.md`
- **Relative Path**: `Docs`
- **Created**: 2026-03-30 14:09:41 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-30 15:18:09 (Asia/Katmandu / GMT+06:45)
- **MD5**: `3a41f9ae52c94e5458a57a500e51f2b5`
- **SHA256**: `0b22f08c12bb97d0dfd823830bbc8af9ea481fb999b079bf99e16d43ddbac7c8`
- **Encoding**: ASCII

**File code content:**

````markdown
# Architecture Explanation

## Flow of Traffic

1. User sends request from browser
2. Request goes to Application Load Balancer
3. ALB distributes traffic to EC2 instances
4. EC2 instances serve the website using Nginx
5. Static content can also be served via S3

## Components

### S3
Used for static website hosting and storing assets.

### EC2
Hosts the web server and serves application content.

### ALB
Distributes incoming traffic across multiple EC2 instances.

### Auto Scaling
Automatically increases or decreases instances based on demand.

## High Availability
- Multiple subnets across different Availability Zones
- Load balancing ensures uptime
````

---

### <a id="📄-docs-commands-md"></a>📄 `Docs/commands.md`

**File Info:**
- **Size**: 344 B
- **Extension**: `.md`
- **Language**: `text`
- **Location**: `Docs/commands.md`
- **Relative Path**: `Docs`
- **Created**: 2026-03-30 14:10:19 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-31 05:06:50 (Asia/Katmandu / GMT+06:45)
- **MD5**: `c6a3a84bd8fc2515f8d0cb059aa111fd`
- **SHA256**: `d5ef7a01153a10fa613b630132db277ee89d2f7c24d5c33fe2afc050083b361f`
- **Encoding**: ASCII

**File code content:**

````markdown
# Commands Used

## SSH into EC2
ssh -i key.pem ubuntu@<public-ip>

## Install Nginx
sudo apt update
sudo apt install nginx -y

## Start Nginx
sudo systemctl start nginx
sudo systemctl enable nginx

## Check Status
sudo systemctl status nginx

## Git Commands
git init
git add .
git commit -m "Initial commit"
git push



````

---

### <a id="📄-docs-steps-md"></a>📄 `Docs/steps.md`

**File Info:**
- **Size**: 858 B
- **Extension**: `.md`
- **Language**: `text`
- **Location**: `Docs/steps.md`
- **Relative Path**: `Docs`
- **Created**: 2026-03-30 14:09:00 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-31 05:06:50 (Asia/Katmandu / GMT+06:45)
- **MD5**: `75877c6e7aaea3900ca75f90189f0e5a`
- **SHA256**: `3cb20490c1a1150c77944484768a22d57ca22808a7372b1856a5e28f082678ab`
- **Encoding**: ASCII

**File code content:**

````markdown
# Step-by-Step Implementation

## Step 1: VPC Setup
- Created a custom VPC
- Configured public subnets
- Attached Internet Gateway
- Configured route tables

## Step 2: S3 Static Website
- Created S3 bucket
- Enabled static website hosting
- Uploaded index.html and error.html
- Configured bucket policy for public access

## Step 3: EC2 Setup
- Launched Ubuntu EC2 instance
- Configured security group (HTTP + SSH)
- Installed Nginx
- Deployed website files

## Step 4: Target Group
- Created target group with HTTP protocol
- Registered EC2 instance
- Configured health checks

## Step 5: Application Load Balancer
- Created ALB with two public subnets
- Configured listener (HTTP)
- Attached target group

## Step 6: Auto Scaling
- Created launch template
- Configured Auto Scaling group
- Attached target group to ASG


````

---

## 🚫 Binary/Excluded Files

The following files were not included in the text content:

- `Screenshots/ALB-working.png`
- `Screenshots/ec2-running.png`
- `Screenshots/ec2-website.png`
- `Screenshots/target-group-healthy.png`

### <a id="📄-scripts-setup-nginx-sh"></a>📄 `scripts/setup_nginx.sh`

**File Info:**
- **Size**: 111 B
- **Extension**: `.sh`
- **Language**: `bash`
- **Location**: `scripts/setup_nginx.sh`
- **Relative Path**: `scripts`
- **Created**: 2026-03-30 14:20:02 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-30 14:20:34 (Asia/Katmandu / GMT+06:45)
- **MD5**: `7b5261d37323d7656b918aa1d7642b43`
- **SHA256**: `5a3d7544eaa70b9d6f983551d561da98a9b897cd511e4151e8256bd9edb53be4`
- **Encoding**: ASCII

**File code content:**

```bash
#!/bin/bash
sudo apt update -y
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

### <a id="📄-website-error-html"></a>📄 `website/error.html`

**File Info:**
- **Size**: 870 B
- **Extension**: `.html`
- **Language**: `html`
- **Location**: `website/error.html`
- **Relative Path**: `website`
- **Created**: 2026-03-30 14:19:11 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-30 05:49:33 (Asia/Katmandu / GMT+06:45)
- **MD5**: `c4d5556336a1abf306fa44357b2639b8`
- **SHA256**: `9ac3d27985afbd7d63f30430720203c9739981d3b26d31db3e35a6ac6a22a835`
- **Encoding**: ASCII

**File code content:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Error - Page Not Found</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            text-align: center;
            padding-top: 100px;
        }
        h1 {
            font-size: 60px;
            color: #ff4d4d;
        }
        p {
            font-size: 20px;
        }
        a {
            text-decoration: none;
            color: white;
            background-color: #0073e6;
            padding: 10px 20px;
            border-radius: 5px;
        }
        a:hover {
            background-color: #005bb5;
        }
    </style>
</head>
<body>

<h1>404</h1>
<p>Oops! The page you are looking for cannot be found.</p>
<a href="index.html">Go Back Home</a>

</body>
</html>
```

---

### <a id="📄-website-index-html"></a>📄 `website/index.html`

**File Info:**
- **Size**: 123.38 KB
- **Extension**: `.html`
- **Language**: `html`
- **Location**: `website/index.html`
- **Relative Path**: `website`
- **Created**: 2026-03-30 14:19:11 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-03-30 14:40:38 (Asia/Katmandu / GMT+06:45)
- **MD5**: `adf7cb79a0389b0904e09da67d5ba5fc`
- **SHA256**: `2eef4aa6f51e3346788d998ac5122a0409e038101bdab5bf3f6a760b89275b9a`
- **Encoding**: UTF-8

**File code content:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> - Discover the Himalayas</title>
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🏔️</text></svg>">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&family=Playfair+Display:wght@700;800;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
    <style>
        /* ============ RESET & BASE ============ */
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1a5632;
            --primary-light: #2d8a4e;
            --secondary: #e8a838;
            --accent: #c0392b;
            --dark: #1a1a2e;
            --darker: #0f0f1a;
            --light: #f8f9fa;
            --gray: #6c757d;
            --white: #ffffff;
            --shadow: 0 10px 40px rgba(0,0,0,0.1);
            --shadow-lg: 0 20px 60px rgba(0,0,0,0.15);
            --transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
            background: var(--white);
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            line-height: 1.2;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        img {
            max-width: 100%;
            display: block;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.8rem;
            color: var(--dark);
            margin-bottom: 15px;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--secondary), var(--accent));
            border-radius: 2px;
        }

        .section-title p {
            color: var(--gray);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 20px auto 0;
        }

        /* ============ PRELOADER ============ */
        #preloader {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--darker);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 99999;
            transition: opacity 0.5s, visibility 0.5s;
        }

        #preloader.hidden {
            opacity: 0;
            visibility: hidden;
        }

        .loader {
            text-align: center;
        }

        .loader-mountain {
            font-size: 4rem;
            animation: bounce 1s infinite;
        }

        .loader p {
            color: var(--white);
            margin-top: 15px;
            font-size: 1.1rem;
            letter-spacing: 3px;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        /* ============ NAVBAR ============ */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            padding: 20px 0;
            transition: var(--transition);
        }

        .navbar.scrolled {
            background: rgba(255, 255, 255, 0.97);
            backdrop-filter: blur(20px);
            padding: 12px 0;
            box-shadow: 0 2px 30px rgba(0,0,0,0.1);
        }

        .navbar .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            font-weight: 800;
            color: var(--white);
            transition: var(--transition);
        }

        .navbar.scrolled .logo {
            color: var(--dark);
        }

        .logo i {
            color: var(--secondary);
            font-size: 1.8rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 35px;
            align-items: center;
        }

        .nav-links a {
            color: rgba(255,255,255,0.9);
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
            transition: var(--transition);
            letter-spacing: 0.5px;
        }

        .navbar.scrolled .nav-links a {
            color: var(--dark);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .nav-btn {
            background: var(--secondary);
            color: var(--white) !important;
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
        }

        .nav-btn:hover {
            background: var(--accent);
            transform: translateY(-2px);
        }

        .nav-btn::after {
            display: none !important;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            z-index: 1001;
        }

        .hamburger span {
            width: 28px;
            height: 3px;
            background: var(--white);
            border-radius: 3px;
            transition: var(--transition);
        }

        .navbar.scrolled .hamburger span {
            background: var(--dark);
        }

        /* ============ HERO SECTION ============ */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }

        .hero-slider {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }

        .hero-slide {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 1.5s ease;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }

        .hero-slide.active {
            opacity: 1;
        }

        .hero-slide:nth-child(1) {
            background-image: url('https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=1920&q=80');
        }

        .hero-slide:nth-child(2) {
            background-image: url('https://images.unsplash.com/photo-1585409677983-0f6c41ca9c3b?w=1920&q=80');
        }

        .hero-slide:nth-child(3) {
            background-image: url('https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=1920&q=80');
        }

        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.3) 50%, rgba(0,0,0,0.6) 100%);
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            text-align: center;
            color: var(--white);
            max-width: 900px;
            padding: 0 20px;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(10px);
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            margin-bottom: 25px;
            border: 1px solid rgba(255,255,255,0.2);
            animation: fadeInDown 1s ease;
        }

        .hero-badge i {
            color: var(--secondary);
        }

        .hero h1 {
            font-size: 4.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            text-shadow: 2px 4px 10px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease 0.2s both;
        }

        .hero h1 span {
            color: var(--secondary);
        }

        .hero-desc {
            font-size: 1.2rem;
            opacity: 0.9;
            max-width: 650px;
            margin: 0 auto 40px;
            animation: fadeInUp 1s ease 0.4s both;
            line-height: 1.8;
        }

        .hero-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 15px 35px;
            border-radius: 50px;
            font-weight: 600;
            font-size: 1rem;
            transition: var(--transition);
            cursor: pointer;
            border: none;
            font-family: 'Poppins', sans-serif;
        }

        .btn-primary {
            background: var(--secondary);
            color: var(--white);
            box-shadow: 0 8px 25px rgba(232,168,56,0.4);
        }

        .btn-primary:hover {
            background: #d4922e;
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(232,168,56,0.5);
        }

        .btn-outline {
            background: transparent;
            color: var(--white);
            border: 2px solid rgba(255,255,255,0.5);
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--dark);
            border-color: var(--white);
            transform: translateY(-3px);
        }

        .hero-stats {
            display: flex;
            justify-content: center;
            gap: 60px;
            margin-top: 60px;
            animation: fadeInUp 1s ease 0.8s both;
        }

        .hero-stat {
            text-align: center;
        }

        .hero-stat h3 {
            font-size: 2.2rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            color: var(--secondary);
        }

        .hero-stat p {
            font-size: 0.85rem;
            opacity: 0.8;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .scroll-indicator {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 2;
            animation: scrollBounce 2s infinite;
        }

        .scroll-indicator a {
            color: var(--white);
            font-size: 1.5rem;
            opacity: 0.7;
            transition: var(--transition);
        }

        .scroll-indicator a:hover {
            opacity: 1;
        }

        @keyframes scrollBounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(10px); }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* ============ QUICK INFO BAR ============ */
        .quick-info {
            background: var(--white);
            padding: 0;
            position: relative;
            z-index: 10;
            margin-top: -60px;
        }

        .quick-info .container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            background: var(--white);
            border-radius: 20px;
            box-shadow: var(--shadow-lg);
            overflow: hidden;
        }

        .info-card {
            padding: 35px 25px;
            text-align: center;
            transition: var(--transition);
            border-right: 1px solid #eee;
            position: relative;
            overflow: hidden;
        }

        .info-card:last-child {
            border-right: none;
        }

        .info-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--secondary);
            transform: scaleX(0);
            transition: var(--transition);
        }

        .info-card:hover::before {
            transform: scaleX(1);
        }

        .info-card:hover {
            background: #fafafa;
        }

        .info-card i {
            font-size: 2.2rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .info-card h4 {
            font-size: 1.1rem;
            margin-bottom: 8px;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
        }

        .info-card p {
            color: var(--gray);
            font-size: 0.9rem;
        }

        /* ============ ABOUT NEPAL SECTION ============ */
        .about {
            padding: 120px 0;
            background: var(--light);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-images {
            position: relative;
        }

        .about-img-main {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow-lg);
            position: relative;
            z-index: 2;
        }

        .about-img-main img {
            width: 100%;
            height: 450px;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .about-img-main:hover img {
            transform: scale(1.05);
        }

        .about-img-float {
            position: absolute;
            bottom: -30px;
            right: -30px;
            width: 200px;
            height: 200px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow-lg);
            border: 5px solid var(--white);
            z-index: 3;
        }

        .about-img-float img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .about-experience {
            position: absolute;
            top: -20px;
            left: -20px;
            background: var(--secondary);
            color: var(--white);
            padding: 20px 25px;
            border-radius: 15px;
            z-index: 3;
            box-shadow: 0 10px 30px rgba(232,168,56,0.3);
        }

        .about-experience h3 {
            font-size: 2rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 800;
        }

        .about-experience p {
            font-size: 0.85rem;
        }

        .about-content h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .about-content h2 span {
            color: var(--primary);
        }

        .about-content > p {
            color: var(--gray);
            margin-bottom: 25px;
            font-size: 1.05rem;
        }

        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 30px;
        }

        .about-feature {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .about-feature i {
            width: 40px;
            height: 40px;
            background: rgba(26,86,50,0.1);
            color: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            font-size: 1rem;
            flex-shrink: 0;
        }

        .about-feature span {
            font-weight: 500;
            font-size: 0.95rem;
        }

        /* ============ DESTINATIONS SECTION ============ */
        .destinations {
            padding: 120px 0;
            background: var(--white);
        }

        .dest-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .dest-card {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
        }

        .dest-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .dest-card-img {
            position: relative;
            height: 280px;
            overflow: hidden;
        }

        .dest-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .dest-card:hover .dest-card-img img {
            transform: scale(1.1);
        }

        .dest-badge {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--secondary);
            color: var(--white);
            padding: 5px 15px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .dest-favorite {
            position: absolute;
            top: 15px;
            right: 15px;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: var(--transition);
        }

        .dest-favorite:hover {
            background: var(--accent);
            color: var(--white);
        }

        .dest-card-body {
            padding: 25px;
        }

        .dest-location {
            display: flex;
            align-items: center;
            gap: 5px;
            color: var(--primary);
            font-size: 0.85rem;
            font-weight: 500;
            margin-bottom: 8px;
        }

        .dest-card-body h3 {
            font-size: 1.4rem;
            margin-bottom: 10px;
        }

        .dest-card-body > p {
            color: var(--gray);
            font-size: 0.9rem;
            margin-bottom: 20px;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .dest-info {
            display: flex;
            justify-content: space-between;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }

        .dest-info-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.85rem;
            color: var(--gray);
        }

        .dest-info-item i {
            color: var(--secondary);
        }

        .dest-difficulty {
            padding: 3px 10px;
            border-radius: 5px;
            font-size: 0.75rem;
            font-weight: 600;
        }

        .diff-easy {
            background: #d4edda;
            color: #155724;
        }

        .diff-moderate {
            background: #fff3cd;
            color: #856404;
        }

        .diff-hard {
            background: #f8d7da;
            color: #721c24;
        }

        .diff-extreme {
            background: #6c1d1d;
            color: #fff;
        }

        /* ============ FEATURED TREK (DETAIL) ============ */
        .featured-trek {
            padding: 120px 0;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            color: var(--white);
            position: relative;
            overflow: hidden;
        }

        .featured-trek::before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(232,168,56,0.1) 0%, transparent 70%);
            border-radius: 50%;
        }

        .featured-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .featured-content .section-title {
            text-align: left;
            margin-bottom: 30px;
        }

        .featured-content .section-title h2 {
            color: var(--white);
            font-size: 2.5rem;
        }

        .featured-content .section-title h2::after {
            left: 0;
            transform: none;
        }

        .featured-desc {
            opacity: 0.9;
            margin-bottom: 30px;
            font-size: 1.05rem;
            line-height: 1.8;
        }

        .featured-details {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 35px;
        }

        .featured-detail {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .featured-detail-icon {
            width: 50px;
            height: 50px;
            background: rgba(232,168,56,0.2);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
        }

        .featured-detail-icon i {
            color: var(--secondary);
            font-size: 1.2rem;
        }

        .featured-detail-text h5 {
            font-family: 'Poppins', sans-serif;
            font-size: 0.8rem;
            opacity: 0.7;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .featured-detail-text p {
            font-weight: 600;
            font-size: 1rem;
        }

        .featured-images {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .featured-img {
            border-radius: 15px;
            overflow: hidden;
            height: 220px;
        }

        .featured-img:first-child {
            grid-row: span 2;
            height: 455px;
        }

        .featured-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .featured-img:hover img {
            transform: scale(1.1);
        }

        /* ============ TREK ROUTES TABLE ============ */
        .trek-routes {
            padding: 120px 0;
            background: var(--light);
        }

        .routes-table-wrapper {
            background: var(--white);
            border-radius: 20px;
            overflow: hidden;
            box-shadow: var(--shadow);
        }

        .routes-table {
            width: 100%;
            border-collapse: collapse;
        }

        .routes-table thead {
            background: var(--primary);
            color: var(--white);
        }

        .routes-table th {
            padding: 18px 20px;
            text-align: left;
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .routes-table td {
            padding: 18px 20px;
            border-bottom: 1px solid #eee;
            font-size: 0.95rem;
        }

        .routes-table tbody tr {
            transition: var(--transition);
        }

        .routes-table tbody tr:hover {
            background: #f8f9fa;
        }

        .routes-table tbody tr:last-child td {
            border-bottom: none;
        }

        .table-trek-name {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .table-trek-thumb {
            width: 50px;
            height: 50px;
            border-radius: 10px;
            overflow: hidden;
            flex-shrink: 0;
        }

        .table-trek-thumb img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .table-rating {
            color: var(--secondary);
        }

        /* ============ SEASONS SECTION ============ */
        .seasons {
            padding: 120px 0;
            background: var(--white);
        }

        .seasons-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
        }

        .season-card {
            background: var(--white);
            border-radius: 20px;
            padding: 35px 25px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }

        .season-card:hover {
            transform: translateY(-8px);
        }

        .season-card.recommended {
            border: 2px solid var(--secondary);
        }

        .season-card.recommended::before {
            content: '★ BEST TIME';
            position: absolute;
            top: 15px;
            right: -30px;
            background: var(--secondary);
            color: var(--white);
            padding: 3px 40px;
            font-size: 0.7rem;
            font-weight: 700;
            transform: rotate(45deg);
            letter-spacing: 1px;
        }

        .season-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .season-card h3 {
            font-size: 1.3rem;
            margin-bottom: 5px;
        }

        .season-card .months {
            color: var(--secondary);
            font-weight: 600;
            font-size: 0.9rem;
            margin-bottom: 15px;
        }

        .season-card p {
            color: var(--gray);
            font-size: 0.9rem;
            line-height: 1.7;
        }

        .season-temps {
            margin-top: 15px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .season-temp {
            font-size: 0.85rem;
        }

        .season-temp .label {
            font-size: 0.75rem;
            color: var(--gray);
            display: block;
        }

        .season-temp .high {
            color: var(--accent);
            font-weight: 600;
        }

        .season-temp .low {
            color: #2196F3;
            font-weight: 600;
        }

        /* ============ PACKING / ESSENTIALS ============ */
        .essentials {
            padding: 120px 0;
            background: var(--light);
        }

        .essentials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .essential-card {
            background: var(--white);
            border-radius: 20px;
            padding: 35px 30px;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .essential-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-lg);
        }

        .essential-card-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .essential-icon {
            width: 55px;
            height: 55px;
            background: linear-gradient(135deg, var(--primary-light), var(--primary));
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.3rem;
            flex-shrink: 0;
        }

        .essential-card h3 {
            font-size: 1.2rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
        }

        .essential-list {
            list-style: none;
        }

        .essential-list li {
            padding: 8px 0;
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.95rem;
            color: #555;
            border-bottom: 1px solid #f0f0f0;
        }

        .essential-list li:last-child {
            border-bottom: none;
        }

        .essential-list li i {
            color: var(--primary);
            font-size: 0.8rem;
        }

        /* ============ TESTIMONIALS ============ */
        .testimonials {
            padding: 120px 0;
            background: var(--white);
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .testimonial-card {
            background: var(--light);
            border-radius: 20px;
            padding: 35px 30px;
            transition: var(--transition);
            position: relative;
        }

        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
        }

        .testimonial-quote {
            font-size: 3rem;
            color: var(--secondary);
            opacity: 0.3;
            line-height: 1;
            margin-bottom: 10px;
        }

        .testimonial-card p {
            color: var(--gray);
            font-size: 0.95rem;
            line-height: 1.8;
            font-style: italic;
            margin-bottom: 20px;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .testimonial-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            border: 3px solid var(--secondary);
        }

        .testimonial-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .testimonial-author h4 {
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
        }

        .testimonial-author span {
            font-size: 0.8rem;
            color: var(--gray);
        }

        .testimonial-stars {
            color: var(--secondary);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        /* ============ NEPAL FACTS ============ */
        .nepal-facts {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: var(--white);
        }

        .facts-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 30px;
        }

        .fact-item {
            text-align: center;
        }

        .fact-item i {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 15px;
        }

        .fact-item h3 {
            font-size: 2.2rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 800;
            margin-bottom: 5px;
        }

        .fact-item p {
            font-size: 0.85rem;
            opacity: 0.8;
            text-transform: uppercase;
            letter-spacing: 1.5px;
        }

        /* ============ GALLERY ============ */
        .gallery {
            padding: 120px 0;
            background: var(--light);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-template-rows: repeat(2, 250px);
            gap: 15px;
        }

        .gallery-item {
            border-radius: 15px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
        }

        .gallery-item:nth-child(1) {
            grid-column: span 2;
            grid-row: span 2;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        .gallery-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 20px;
            background: linear-gradient(transparent, rgba(0,0,0,0.7));
            color: var(--white);
            opacity: 0;
            transition: var(--transition);
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        .gallery-overlay h4 {
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
        }

        .gallery-overlay p {
            font-size: 0.8rem;
            opacity: 0.8;
        }

        /* ============ FAQ ============ */
        .faq {
            padding: 120px 0;
            background: var(--white);
        }

        .faq-grid {
            max-width: 800px;
            margin: 0 auto;
        }

        .faq-item {
            background: var(--light);
            border-radius: 15px;
            margin-bottom: 15px;
            overflow: hidden;
            transition: var(--transition);
        }

        .faq-item.active {
            box-shadow: var(--shadow);
        }

        .faq-question {
            padding: 20px 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
            font-weight: 600;
            font-size: 1.05rem;
            transition: var(--transition);
        }

        .faq-question:hover {
            color: var(--primary);
        }

        .faq-question i {
            transition: var(--transition);
            color: var(--secondary);
        }

        .faq-item.active .faq-question i {
            transform: rotate(180deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease;
        }

        .faq-answer-inner {
            padding: 0 25px 20px;
            color: var(--gray);
            line-height: 1.8;
        }

        /* ============ CTA / BOOKING ============ */
        .cta {
            padding: 120px 0;
            background: url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=1920&q=80') center/cover no-repeat fixed;
            position: relative;
        }

        .cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.65);
        }

        .cta .container {
            position: relative;
            z-index: 2;
        }

        .cta-content {
            text-align: center;
            color: var(--white);
            max-width: 700px;
            margin: 0 auto;
        }

        .cta-content h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .cta-content p {
            font-size: 1.1rem;
            opacity: 0.9;
            margin-bottom: 40px;
            line-height: 1.8;
        }

        /* ============ CONTACT ============ */
        .contact {
            padding: 120px 0;
            background: var(--light);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 50px;
            align-items: start;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .contact-info > p {
            color: var(--gray);
            margin-bottom: 30px;
            line-height: 1.8;
        }

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .contact-detail {
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }

        .contact-detail-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, var(--primary-light), var(--primary));
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--white);
            font-size: 1.1rem;
            flex-shrink: 0;
        }

        .contact-detail h4 {
            font-size: 1rem;
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
            margin-bottom: 3px;
        }

        .contact-detail p {
            color: var(--gray);
            font-size: 0.95rem;
        }

        .contact-social {
            display: flex;
            gap: 12px;
            margin-top: 30px;
        }

        .contact-social a {
            width: 45px;
            height: 45px;
            background: var(--white);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.1rem;
            transition: var(--transition);
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
        }

        .contact-social a:hover {
            background: var(--primary);
            color: var(--white);
            transform: translateY(-3px);
        }

        .contact-form {
            background: var(--white);
            border-radius: 20px;
            padding: 40px;
            box-shadow: var(--shadow);
        }

        .contact-form h3 {
            font-size: 1.5rem;
            margin-bottom: 25px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
            font-size: 0.9rem;
            color: var(--dark);
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            width: 100%;
            padding: 12px 18px;
            border: 2px solid #e9ecef;
            border-radius: 12px;
            font-family: 'Poppins', sans-serif;
            font-size: 0.95rem;
            transition: var(--transition);
            outline: none;
            background: #fafafa;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            border-color: var(--primary);
            background: var(--white);
            box-shadow: 0 0 0 4px rgba(26,86,50,0.1);
        }

        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }

        .form-submit {
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, var(--primary-light), var(--primary));
            color: var(--white);
            border: none;
            border-radius: 12px;
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
        }

        .form-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(26,86,50,0.3);
        }

        /* ============ NEPAL FLAG DECORATION ============ */
        .nepal-divider {
            height: 5px;
            background: linear-gradient(90deg, #dc143c 0%, #dc143c 50%, #003893 50%, #003893 100%);
        }

        /* ============ FOOTER ============ */
        .footer {
            background: var(--darker);
            color: rgba(255,255,255,0.8);
            padding: 80px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: 1.5fr 1fr 1fr 1.2fr;
            gap: 40px;
            margin-bottom: 50px;
        }

        .footer-brand .logo {
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        .footer-brand p {
            font-size: 0.9rem;
            line-height: 1.8;
            opacity: 0.8;
            margin-bottom: 20px;
        }

        .footer h4 {
            color: var(--white);
            font-family: 'Poppins', sans-serif;
            font-size: 1.1rem;
            font-weight: 600;
            margin-bottom: 20px;
            position: relative;
        }

        .footer h4::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 40px;
            height: 2px;
            background: var(--secondary);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: rgba(255,255,255,0.7);
            font-size: 0.9rem;
            transition: var(--transition);
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-links a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }

        .footer-newsletter p {
            font-size: 0.9rem;
            opacity: 0.8;
            margin-bottom: 15px;
        }

        .newsletter-form {
            display: flex;
            gap: 10px;
        }

        .newsletter-form input {
            flex: 1;
            padding: 12px 18px;
            border: none;
            border-radius: 10px;
            background: rgba(255,255,255,0.1);
            color: var(--white);
            font-family: 'Poppins', sans-serif;
            outline: none;
        }

        .newsletter-form input::placeholder {
            color: rgba(255,255,255,0.5);
        }

        .newsletter-form button {
            padding: 12px 20px;
            background: var(--secondary);
            border: none;
            border-radius: 10px;
            color: var(--white);
            cursor: pointer;
            transition: var(--transition);
            font-size: 1rem;
        }

        .newsletter-form button:hover {
            background: #d4922e;
        }

        .footer-bottom {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 0.85rem;
            opacity: 0.7;
        }

        /* ============ BACK TO TOP ============ */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background: var(--secondary);
            color: var(--white);
            border: none;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            box-shadow: 0 5px 20px rgba(232,168,56,0.4);
            z-index: 100;
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }

        /* ============ LIGHTBOX ============ */
        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
        }

        .lightbox.active {
            opacity: 1;
            visibility: visible;
        }

        .lightbox img {
            max-width: 85%;
            max-height: 85%;
            border-radius: 10px;
            object-fit: contain;
        }

        .lightbox-close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: var(--white);
            font-size: 2rem;
            cursor: pointer;
            transition: var(--transition);
        }

        .lightbox-close:hover {
            color: var(--secondary);
        }

        /* ============ ANIMATIONS ============ */
        .animate-on-scroll {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .animate-on-scroll.animated {
            opacity: 1;
            transform: translateY(0);
        }

        /* ============ RESPONSIVE ============ */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 3.2rem;
            }

            .dest-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .seasons-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .facts-grid {
                grid-template-columns: repeat(3, 1fr);
            }

            .footer-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }

            .nav-links {
                position: fixed;
                top: 0;
                right: -100%;
                width: 280px;
                height: 100vh;
                background: var(--white);
                flex-direction: column;
                justify-content: center;
                gap: 25px;
                transition: var(--transition);
                box-shadow: -5px 0 30px rgba(0,0,0,0.1);
            }

            .nav-links.active {
                right: 0;
            }

            .nav-links a {
                color: var(--dark) !important;
                font-size: 1.1rem;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero-desc {
                font-size: 1rem;
            }

            .hero-stats {
                gap: 30px;
            }

            .hero-stat h3 {
                font-size: 1.6rem;
            }

            .quick-info .container {
                grid-template-columns: repeat(2, 1fr);
            }

            .about-grid,
            .featured-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .about-img-float {
                right: 10px;
                bottom: -20px;
            }

            .dest-grid {
                grid-template-columns: 1fr;
            }

            .section-title h2 {
                font-size: 2.2rem;
            }

            .essentials-grid,
            .testimonials-grid {
                grid-template-columns: 1fr;
            }

            .gallery-grid {
                grid-template-columns: repeat(2, 1fr);
                grid-template-rows: auto;
            }

            .gallery-item:nth-child(1) {
                grid-column: span 2;
            }

            .facts-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .routes-table-wrapper {
                overflow-x: auto;
            }

            .routes-table {
                min-width: 700px;
            }

            .form-row {
                grid-template-columns: 1fr;
            }

            .footer-grid {
                grid-template-columns: 1fr;
            }

            .footer-bottom {
                flex-direction: column;
                gap: 10px;
                text-align: center;
            }

            .featured-images {
                grid-template-columns: 1fr;
            }

            .featured-img:first-child {
                grid-row: span 1;
                height: 250px;
            }

            .cta-content h2 {
                font-size: 2.2rem;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 2rem;
            }

            .quick-info .container {
                grid-template-columns: 1fr;
            }

            .seasons-grid {
                grid-template-columns: 1fr;
            }

            .hero-stats {
                flex-direction: column;
                gap: 20px;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .gallery-item:nth-child(1) {
                grid-column: span 1;
            }

            .facts-grid {
                grid-template-columns: 1fr;
            }

            .newsletter-form {
                flex-direction: column;
            }

            .featured-details {
                grid-template-columns: 1fr;
            }

            .about-features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- ============ PRELOADER ============ -->
    <div id="preloader">
        <div class="loader">
            <div class="loader-mountain">🏔️</div>
            <p>NEPAL TREKS</p>
        </div>
    </div>

    <!-- ============ NAVBAR ============ -->
    <nav class="navbar" id="navbar">
        <div class="container">
            <a href="#" class="logo">
                <i class="fas fa-mountain"></i>
                Nepal Treks
            </a>
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#destinations">Destinations</a></li>
                <li><a href="#routes">Routes</a></li>
                <li><a href="#seasons">Seasons</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact" class="nav-btn">Book Now</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
    </nav>

    <!-- ============ HERO SECTION ============ -->
    <section class="hero" id="home">
        <div class="hero-slider">
            <div class="hero-slide active" style="background-image: url('https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=1920&q=80')"></div>
            <div class="hero-slide" style="background-image: url('https://images.unsplash.com/photo-1585409677983-0f6c41ca9c3b?w=1920&q=80')"></div>
            <div class="hero-slide" style="background-image: url('https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=1920&q=80')"></div>
        </div>
        <div class="hero-overlay"></div>
        <div class="hero-content">
            <div class="hero-badge">
                <i class="fas fa-globe-asia"></i>
                The Roof of the World
            </div>
            <h1>Discover <span>Nepal's</span> Majestic Himalayan Trails</h1>
            <p class="hero-desc">
                Embark on an unforgettable journey through ancient trails, towering peaks, and vibrant 
                Sherpa culture. Experience the magic of trekking in the land of Mount Everest.
            </p>
            <div class="hero-buttons">
                <a href="#destinations" class="btn btn-primary">
                    <i class="fas fa-compass"></i> Explore Treks
                </a>
                <a href="#contact" class="btn btn-outline">
                    <i class="fas fa-paper-plane"></i> Plan Your Trip
                </a>
            </div>
            <div class="hero-stats">
                <div class="hero-stat">
                    <h3 id="counter1">0</h3>
                    <p>Trekking Routes</p>
                </div>
                <div class="hero-stat">
                    <h3 id="counter2">0</h3>
                    <p>Peaks Above 8000m</p>
                </div>
                <div class="hero-stat">
                    <h3 id="counter3">0</h3>
                    <p>Happy Trekkers</p>
                </div>
            </div>
        </div>
        <div class="scroll-indicator">
            <a href="#about"><i class="fas fa-chevron-down"></i></a>
        </div>
    </section>

    <!-- ============ QUICK INFO BAR ============ -->
    <section class="quick-info">
        <div class="container">
            <div class="info-card">
                <i class="fas fa-hiking"></i>
                <h4>150+ Trails</h4>
                <p>From easy walks to extreme expeditions</p>
            </div>
            <div class="info-card">
                <i class="fas fa-shield-alt"></i>
                <h4>Safe Trekking</h4>
                <p>Licensed guides & safety equipment</p>
            </div>
            <div class="info-card">
                <i class="fas fa-wallet"></i>
                <h4>Best Prices</h4>
                <p>Affordable packages for every budget</p>
            </div>
            <div class="info-card">
                <i class="fas fa-headset"></i>
                <h4>24/7 Support</h4>
                <p>Round the clock assistance</p>
            </div>
        </div>
    </section>

    <!-- ============ ABOUT NEPAL ============ -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-grid">
                <div class="about-images animate-on-scroll">
                    <div class="about-experience">
                        <h3>15+</h3>
                        <p>Years Experience</p>
                    </div>
                    <div class="about-img-main">
                        <img src="https://images.unsplash.com/photo-1571401835393-8c5f35328320?w=700&q=80" alt="Trekkers in Nepal">
                    </div>
                    <div class="about-img-float">
                        <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?w=300&q=80" alt="Nepal Prayer Flags">
                    </div>
                </div>
                <div class="about-content animate-on-scroll">
                    <h2>Why Trek in <span>Nepal</span>?</h2>
                    <p>
                        Nepal is the ultimate trekking paradise, home to 8 of the world's 14 highest peaks, 
                        including Mount Everest (8,848.86m). The country offers unparalleled diversity — from 
                        subtropical jungles to arctic tundra, all within a few days' walk.
                    </p>
                    <p>
                        Beyond the mountains, you'll encounter ancient monasteries, warm Sherpa hospitality, 
                        exotic wildlife, and breathtaking landscapes that have drawn adventurers for centuries. 
                        Whether you're a beginner or an experienced mountaineer, Nepal has a trail for you.
                    </p>
                    <div class="about-features">
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>8 of 14 Highest Peaks</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>UNESCO Heritage Sites</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>Diverse Flora & Fauna</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>Rich Cultural Heritage</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>Affordable Trekking</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check"></i>
                            <span>Warm Hospitality</span>
                        </div>
                    </div>
                    <a href="#destinations" class="btn btn-primary">
                        <i class="fas fa-mountain"></i> View Destinations
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ DESTINATIONS ============ -->
    <section class="destinations" id="destinations">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Popular Trekking Destinations</h2>
                <p>Explore the most breathtaking trekking routes in Nepal, each offering unique experiences and stunning views</p>
            </div>
            <div class="dest-grid">

                <!-- Card 1 - Everest Base Camp -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1516302752625-fcc3c50ae61f?w=700&q=80" alt="Everest Base Camp Trek">
                        <span class="dest-badge">Most Popular</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Solukhumbu, Nepal
                        </div>
                        <h3>Everest Base Camp Trek</h3>
                        <p>
                            Stand at the foot of the world's highest mountain at 5,364m. Trek through Sherpa villages, 
                            cross suspension bridges, visit Tengboche Monastery, and witness incredible panoramas of 
                            Everest, Lhotse, Nuptse, and Ama Dablam.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 14 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 5,364m
                            </div>
                            <span class="dest-difficulty diff-hard">Challenging</span>
                        </div>
                    </div>
                </div>

                <!-- Card 2 - Annapurna Circuit -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1585409677983-0f6c41ca9c3b?w=700&q=80" alt="Annapurna Circuit">
                        <span class="dest-badge">Classic Route</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Annapurna Region, Nepal
                        </div>
                        <h3>Annapurna Circuit Trek</h3>
                        <p>
                            The classic Annapurna Circuit is one of the world's greatest treks, circling the 
                            Annapurna massif through diverse landscapes from rice paddies to alpine meadows. 
                            Cross the legendary Thorong La Pass at 5,416m.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 18 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 5,416m
                            </div>
                            <span class="dest-difficulty diff-hard">Challenging</span>
                        </div>
                    </div>
                </div>

                <!-- Card 3 - Annapurna Base Camp -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=700&q=80" alt="Annapurna Base Camp">
                        <span class="dest-badge">Scenic</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Kaski, Nepal
                        </div>
                        <h3>Annapurna Base Camp</h3>
                        <p>
                            A stunning trek to the sanctuary of the Annapurna massif at 4,130m. Walk through 
                            lush rhododendron forests, terraced rice fields, and Gurung villages before arriving 
                            at the breathtaking amphitheatre of peaks.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 10 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 4,130m
                            </div>
                            <span class="dest-difficulty diff-moderate">Moderate</span>
                        </div>
                    </div>
                </div>

                <!-- Card 4 - Langtang Valley -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1571401835393-8c5f35328320?w=700&q=80" alt="Langtang Valley">
                        <span class="dest-badge">Hidden Gem</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Rasuwa, Nepal
                        </div>
                        <h3>Langtang Valley Trek</h3>
                        <p>
                            Often called "the valley of glaciers," the Langtang Valley offers an accessible trek 
                            close to Kathmandu. Explore Tamang heritage, ancient monasteries, cheese factories, 
                            and dramatic mountain scenery along the Tibetan border.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 7 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 3,870m
                            </div>
                            <span class="dest-difficulty diff-moderate">Moderate</span>
                        </div>
                    </div>
                </div>

                <!-- Card 5 - Manaslu Circuit -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=700&q=80" alt="Manaslu Circuit">
                        <span class="dest-badge">Off the Beaten Path</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Gorkha, Nepal
                        </div>
                        <h3>Manaslu Circuit Trek</h3>
                        <p>
                            A restricted-area trek around the world's 8th highest peak (8,163m). This remote trail 
                            offers authentic Tibetan-influenced culture, pristine wilderness, and far fewer trekkers 
                            than Everest or Annapurna regions.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 16 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 5,160m
                            </div>
                            <span class="dest-difficulty diff-hard">Challenging</span>
                        </div>
                    </div>
                </div>

                <!-- Card 6 - Poon Hill -->
                <div class="dest-card animate-on-scroll">
                    <div class="dest-card-img">
                        <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?w=700&q=80" alt="Poon Hill Trek">
                        <span class="dest-badge">Beginner Friendly</span>
                        <div class="dest-favorite"><i class="far fa-heart"></i></div>
                    </div>
                    <div class="dest-card-body">
                        <div class="dest-location">
                            <i class="fas fa-map-marker-alt"></i> Myagdi, Nepal
                        </div>
                        <h3>Ghorepani Poon Hill Trek</h3>
                        <p>
                            Perfect for beginners, this short trek offers spectacular sunrise views over Dhaulagiri 
                            and Annapurna ranges from Poon Hill viewpoint at 3,210m. Walk through beautiful 
                            rhododendron forests and traditional Magar villages.
                        </p>
                        <div class="dest-info">
                            <div class="dest-info-item">
                                <i class="fas fa-clock"></i> 5 Days
                            </div>
                            <div class="dest-info-item">
                                <i class="fas fa-arrow-up"></i> 3,210m
                            </div>
                            <span class="dest-difficulty diff-easy">Easy</span>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- ============ FEATURED TREK DETAIL ============ -->
    <section class="featured-trek" id="featured">
        <div class="container">
            <div class="featured-grid">
                <div class="featured-content animate-on-scroll">
                    <div class="section-title">
                        <h2>Everest Base Camp — The Ultimate Trek</h2>
                    </div>
                    <p class="featured-desc">
                        The Everest Base Camp trek is the most iconic trekking experience in the world. Follow in the 
                        footsteps of legendary mountaineers Sir Edmund Hillary and Tenzing Norgay. This 14-day 
                        adventure takes you through the heart of the Khumbu region, offering unmatched Himalayan 
                        panoramas, rich Sherpa culture, and a once-in-a-lifetime experience at the base of Mount Everest.
                    </p>
                    <div class="featured-details">
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-mountain"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Max Altitude</h5>
                                <p>5,364m / 17,598ft</p>
                            </div>
                        </div>
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-calendar-alt"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Duration</h5>
                                <p>12–14 Days</p>
                            </div>
                        </div>
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-route"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Distance</h5>
                                <p>130 km Round Trip</p>
                            </div>
                        </div>
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-fire"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Difficulty</h5>
                                <p>Challenging</p>
                            </div>
                        </div>
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-sun"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Best Season</h5>
                                <p>Oct–Nov, Mar–May</p>
                            </div>
                        </div>
                        <div class="featured-detail">
                            <div class="featured-detail-icon">
                                <i class="fas fa-dollar-sign"></i>
                            </div>
                            <div class="featured-detail-text">
                                <h5>Starting Price</h5>
                                <p>$1,200 / person</p>
                            </div>
                        </div>
                    </div>
                    <a href="#contact" class="btn btn-primary">
                        <i class="fas fa-paper-plane"></i> Book This Trek
                    </a>
                </div>
                <div class="featured-images animate-on-scroll">
                    <div class="featured-img">
                        <img src="https://images.unsplash.com/photo-1516302752625-fcc3c50ae61f?w=700&q=80" alt="Everest">
                    </div>
                    <div class="featured-img">
                        <img src="https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=700&q=80" alt="Everest Region">
                    </div>
                    <div class="featured-img">
                        <img src="https://images.unsplash.com/photo-1571401835393-8c5f35328320?w=700&q=80" alt="Trekkers">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ TREK ROUTES TABLE ============ -->
    <section class="trek-routes" id="routes">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Trek Routes Comparison</h2>
                <p>Compare different trekking routes to find the perfect adventure for your experience level</p>
            </div>
            <div class="routes-table-wrapper animate-on-scroll">
                <table class="routes-table">
                    <thead>
                        <tr>
                            <th>Trek Name</th>
                            <th>Duration</th>
                            <th>Max Altitude</th>
                            <th>Difficulty</th>
                            <th>Best Season</th>
                            <th>Rating</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1516302752625-fcc3c50ae61f?w=100&q=60" alt="EBC">
                                    </div>
                                    <strong>Everest Base Camp</strong>
                                </div>
                            </td>
                            <td>14 Days</td>
                            <td>5,364m</td>
                            <td><span class="dest-difficulty diff-hard">Challenging</span></td>
                            <td>Oct-Nov, Mar-May</td>
                            <td class="table-rating">★★★★★</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1585409677983-0f6c41ca9c3b?w=100&q=60" alt="Annapurna">
                                    </div>
                                    <strong>Annapurna Circuit</strong>
                                </div>
                            </td>
                            <td>18 Days</td>
                            <td>5,416m</td>
                            <td><span class="dest-difficulty diff-hard">Challenging</span></td>
                            <td>Oct-Nov, Mar-Apr</td>
                            <td class="table-rating">★★★★★</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=100&q=60" alt="ABC">
                                    </div>
                                    <strong>Annapurna Base Camp</strong>
                                </div>
                            </td>
                            <td>10 Days</td>
                            <td>4,130m</td>
                            <td><span class="dest-difficulty diff-moderate">Moderate</span></td>
                            <td>Oct-Nov, Mar-May</td>
                            <td class="table-rating">★★★★☆</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1571401835393-8c5f35328320?w=100&q=60" alt="Langtang">
                                    </div>
                                    <strong>Langtang Valley</strong>
                                </div>
                            </td>
                            <td>7 Days</td>
                            <td>3,870m</td>
                            <td><span class="dest-difficulty diff-moderate">Moderate</span></td>
                            <td>Oct-Dec, Mar-May</td>
                            <td class="table-rating">★★★★☆</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=100&q=60" alt="Manaslu">
                                    </div>
                                    <strong>Manaslu Circuit</strong>
                                </div>
                            </td>
                            <td>16 Days</td>
                            <td>5,160m</td>
                            <td><span class="dest-difficulty diff-hard">Challenging</span></td>
                            <td>Sep-Nov, Mar-May</td>
                            <td class="table-rating">★★★★★</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?w=100&q=60" alt="Poon Hill">
                                    </div>
                                    <strong>Poon Hill</strong>
                                </div>
                            </td>
                            <td>5 Days</td>
                            <td>3,210m</td>
                            <td><span class="dest-difficulty diff-easy">Easy</span></td>
                            <td>Oct-May</td>
                            <td class="table-rating">★★★★☆</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=100&q=60" alt="Upper Mustang">
                                    </div>
                                    <strong>Upper Mustang</strong>
                                </div>
                            </td>
                            <td>12 Days</td>
                            <td>3,840m</td>
                            <td><span class="dest-difficulty diff-moderate">Moderate</span></td>
                            <td>Mar-Nov</td>
                            <td class="table-rating">★★★★★</td>
                        </tr>
                        <tr>
                            <td>
                                <div class="table-trek-name">
                                    <div class="table-trek-thumb">
                                        <img src="https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=100&q=60" alt="Three Passes">
                                    </div>
                                    <strong>Three Passes Trek</strong>
                                </div>
                            </td>
                            <td>19 Days</td>
                            <td>5,545m</td>
                            <td><span class="dest-difficulty diff-extreme">Extreme</span></td>
                            <td>Oct-Nov, Apr-May</td>
                            <td class="table-rating">★★★★★</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- ============ SEASONS ============ -->
    <section class="seasons" id="seasons">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Best Time to Trek in Nepal</h2>
                <p>Nepal has four distinct seasons, each offering a different trekking experience</p>
            </div>
            <div class="seasons-grid">
                <div class="season-card recommended animate-on-scroll">
                    <div class="season-icon">🍂</div>
                    <h3>Autumn</h3>
                    <div class="months">October - November</div>
                    <p>
                        The best trekking season with clear skies, stable weather, and spectacular mountain views. 
                        Trails are busy but conditions are ideal. Perfect visibility for photography.
                    </p>
                    <div class="season-temps">
                        <div class="season-temp">
                            <span class="label">Day</span>
                            <span class="high">15-20°C</span>
                        </div>
                        <div class="season-temp">
                            <span class="label">Night</span>
                            <span class="low">-5 to 5°C</span>
                        </div>
                    </div>
                </div>
                <div class="season-card recommended animate-on-scroll">
                    <div class="season-icon">🌸</div>
                    <h3>Spring</h3>
                    <div class="months">March - May</div>
                    <p>
                        Second-best season with blooming rhododendrons and wildflowers. Warmer temperatures 
                        and longer days. Slightly hazier than autumn but incredibly beautiful.
                    </p>
                    <div class="season-temps">
                        <div class="season-temp">
                            <span class="label">Day</span>
                            <span class="high">15-25°C</span>
                        </div>
                        <div class="season-temp">
                            <span class="label">Night</span>
                            <span class="low">0 to 10°C</span>
                        </div>
                    </div>
                </div>
                <div class="season-card animate-on-scroll">
                    <div class="season-icon">❄️</div>
                    <h3>Winter</h3>
                    <div class="months">December - February</div>
                    <p>
                        Cold but clear weather with fewer trekkers. Lower altitude treks are still feasible. 
                        High passes may be closed due to snow. Great for solitude seekers.
                    </p>
                    <div class="season-temps">
                        <div class="season-temp">
                            <span class="label">Day</span>
                            <span class="high">5-15°C</span>
                        </div>
                        <div class="season-temp">
                            <span class="label">Night</span>
                            <span class="low">-15 to -5°C</span>
                        </div>
                    </div>
                </div>
                <div class="season-card animate-on-scroll">
                    <div class="season-icon">🌧️</div>
                    <h3>Monsoon</h3>
                    <div class="months">June - September</div>
                    <p>
                        Heavy rainfall, leeches, and landslide risks. Not recommended for most treks. 
                        Rain shadow areas like Upper Mustang and Dolpo remain accessible.
                    </p>
                    <div class="season-temps">
                        <div class="season-temp">
                            <span class="label">Day</span>
                            <span class="high">20-30°C</span>
                        </div>
                        <div class="season-temp">
                            <span class="label">Night</span>
                            <span class="low">10-20°C</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ PACKING ESSENTIALS ============ -->
    <section class="essentials" id="essentials">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Trekking Essentials</h2>
                <p>Everything you need to pack for a safe and comfortable trek in the Himalayas</p>
            </div>
            <div class="essentials-grid">
                <div class="essential-card animate-on-scroll">
                    <div class="essential-card-header">
                        <div class="essential-icon">
                            <i class="fas fa-tshirt"></i>
                        </div>
                        <h3>Clothing</h3>
                    </div>
                    <ul class="essential-list">
                        <li><i class="fas fa-check-circle"></i> Moisture-wicking base layers</li>
                        <li><i class="fas fa-check-circle"></i> Down jacket (rated -20°C)</li>
                        <li><i class="fas fa-check-circle"></i> Waterproof outer shell</li>
                        <li><i class="fas fa-check-circle"></i> Trekking pants (convertible)</li>
                        <li><i class="fas fa-check-circle"></i> Warm fleece mid-layer</li>
                        <li><i class="fas fa-check-circle"></i> Merino wool socks (4-5 pairs)</li>
                        <li><i class="fas fa-check-circle"></i> Sun hat & warm beanie</li>
                    </ul>
                </div>
                <div class="essential-card animate-on-scroll">
                    <div class="essential-card-header">
                        <div class="essential-icon">
                            <i class="fas fa-backpack"></i>
                        </div>
                        <h3>Gear & Equipment</h3>
                    </div>
                    <ul class="essential-list">
                        <li><i class="fas fa-check-circle"></i> Trekking boots (broken in)</li>
                        <li><i class="fas fa-check-circle"></i> 50-65L backpack</li>
                        <li><i class="fas fa-check-circle"></i> Sleeping bag (-15°C rated)</li>
                        <li><i class="fas fa-check-circle"></i> Trekking poles (collapsible)</li>
                        <li><i class="fas fa-check-circle"></i> Headlamp + spare batteries</li>
                        <li><i class="fas fa-check-circle"></i> Water purification tablets</li>
                        <li><i class="fas fa-check-circle"></i> Dry bags for electronics</li>
                    </ul>
                </div>
                <div class="essential-card animate-on-scroll">
                    <div class="essential-card-header">
                        <div class="essential-icon">
                            <i class="fas fa-first-aid"></i>
                        </div>
                        <h3>Health & Safety</h3>
                    </div>
                    <ul class="essential-list">
                        <li><i class="fas fa-check-circle"></i> First aid kit</li>
                        <li><i class="fas fa-check-circle"></i> Altitude sickness medication</li>
                        <li><i class="fas fa-check-circle"></i> SPF 50+ sunscreen</li>
                        <li><i class="fas fa-check-circle"></i> UV protection sunglasses</li>
                        <li><i class="fas fa-check-circle"></i> Insect repellent</li>
                        <li><i class="fas fa-check-circle"></i> Personal medications</li>
                        <li><i class="fas fa-check-circle"></i> Travel insurance documents</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ NEPAL FACTS ============ -->
    <section class="nepal-facts">
        <div class="container">
            <div class="facts-grid">
                <div class="fact-item animate-on-scroll">
                    <i class="fas fa-mountain"></i>
                    <h3>8,848m</h3>
                    <p>Mt. Everest Height</p>
                </div>
                <div class="fact-item animate-on-scroll">
                    <i class="fas fa-flag"></i>
                    <h3>8</h3>
                    <p>Peaks Above 8000m</p>
                </div>
                <div class="fact-item animate-on-scroll">
                    <i class="fas fa-users"></i>
                    <h3>125+</h3>
                    <p>Ethnic Groups</p>
                </div>
                <div class="fact-item animate-on-scroll">
                    <i class="fas fa-paw"></i>
                    <h3>900+</h3>
                    <p>Bird Species</p>
                </div>
                <div class="fact-item animate-on-scroll">
                    <i class="fas fa-landmark"></i>
                    <h3>10</h3>
                    <p>UNESCO Sites</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ GALLERY ============ -->
    <section class="gallery" id="gallery">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Trek Gallery</h2>
                <p>Stunning captures from the trails across Nepal's magnificent landscapes</p>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item animate-on-scroll" onclick="openLightbox(this)">
                    <img src="https://images.unsplash.com/photo-1544735716-392fe2489ffa?w=800&q=80" alt="Himalayan Panorama">
                    <div class="gallery-overlay">
                        <h4>Himalayan Panorama</h4>
                        <p>Everest Region</p>
                    </div>
                </div>
                <div class="gallery-item animate-on-scroll" onclick="openLightbox(this)">
                    <img src="https://images.unsplash.com/photo-1585409677983-0f6c41ca9c3b?w=600&q=80" alt="Mountain Lake">
                    <div class="gallery-overlay">
                        <h4>Mountain Lake</h4>
                        <p>Annapurna Region</p>
                    </div>
                </div>
                <div class="gallery-item animate-on-scroll" onclick="openLightbox(this)">
                    <img src="https://images.unsplash.com/photo-1605649487212-47bdab064df7?w=600&q=80" alt="Prayer Flags">
                    <div class="gallery-overlay">
                        <h4>Prayer Flags</h4>
                        <p>Mountain Pass</p>
                    </div>
                </div>
                <div class="gallery-item animate-on-scroll" onclick="openLightbox(this)">
                    <img src="https://images.unsplash.com/photo-1486911278844-a81c5267e227?w=600&q=80" alt="Alpine Meadow">
                    <div class="gallery-overlay">
                        <h4>Alpine Meadow</h4>
                        <p>Langtang Valley</p>
                    </div>
                </div>
                <div class="gallery-item animate-on-scroll" onclick="openLightbox(this)">
                    <img src="https://images.unsplash.com/photo-1571401835393-8c5f35328320?w=600&q=80" alt="Trekking Trail">
                    <div class="gallery-overlay">
                        <h4>Trekking Trail</h4>
                        <p>Khumbu Region</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ TESTIMONIALS ============ -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Trekker Experiences</h2>
                <p>What our fellow trekkers say about their Nepal adventure</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-quote">"</div>
                    <div class="testimonial-stars">★★★★★</div>
                    <p>
                        The Everest Base Camp trek was the most transformative experience of my life. Standing 
                        at the base of the world's highest peak brought tears to my eyes. The Sherpa guides 
                        were incredible — their knowledge and warmth made the journey unforgettable.
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">
                            <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&q=60" alt="James">
                        </div>
                        <div>
                            <h4>James Wilson</h4>
                            <span>🇺🇸 United States • EBC Trek</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-quote">"</div>
                    <div class="testimonial-stars">★★★★★</div>
                    <p>
                        The Annapurna Circuit exceeded every expectation. From subtropical forests to high 
                        alpine passes, the diversity was incredible. Crossing Thorong La Pass at dawn was 
                        absolutely magical. Nepal has stolen my heart forever.
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">
                            <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=100&q=60" alt="Sarah">
                        </div>
                        <div>
                            <h4>Sarah Mitchell</h4>
                            <span>🇬🇧 United Kingdom • Annapurna Circuit</span>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card animate-on-scroll">
                    <div class="testimonial-quote">"</div>
                    <div class="testimonial-stars">★★★★★</div>
                    <p>
                        As a first-time trekker, Poon Hill was perfect. The sunrise view with Dhaulagiri 
                        and Annapurna glowing in golden light is something I'll never forget. The teahouses 
                        were cozy and the dal bhat gave me power! Highly recommend Nepal.
                    </p>
                    <div class="testimonial-author">
                        <div class="testimonial-avatar">
                            <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=100&q=60" alt="Kenji">
                        </div>
                        <div>
                            <h4>Kenji Tanaka</h4>
                            <span>🇯🇵 Japan • Poon Hill Trek</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ FAQ ============ -->
    <section class="faq" id="faq">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Frequently Asked Questions</h2>
                <p>Everything you need to know before trekking in Nepal</p>
            </div>
            <div class="faq-grid">
                <div class="faq-item active animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        Do I need a permit to trek in Nepal?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer" style="max-height: 200px;">
                        <div class="faq-answer-inner">
                            Yes, most treks in Nepal require permits. The two main permits are the TIMS (Trekkers' 
                            Information Management System) card and the relevant conservation area or national park 
                            entry permit (e.g., Sagarmatha National Park for Everest, ACAP for Annapurna). Some 
                            restricted areas like Upper Mustang and Manaslu require special permits through a 
                            registered trekking agency.
                        </div>
                    </div>
                </div>
                <div class="faq-item animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        How fit do I need to be for trekking?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="faq-answer-inner">
                            It depends on the trek. Easy treks like Poon Hill require basic fitness — regular walking 
                            and light exercise. For moderate treks like ABC, you should be comfortable walking 5-7 
                            hours daily with elevation gain. Challenging treks like EBC or Annapurna Circuit require 
                            good cardiovascular fitness and ideally 2-3 months of preparation including hiking with a 
                            loaded backpack, cardio, and strength training.
                        </div>
                    </div>
                </div>
                <div class="faq-item animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        What about altitude sickness?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="faq-answer-inner">
                            Altitude sickness (AMS) is a real concern above 2,500m. Symptoms include headache, 
                            nausea, dizziness, and fatigue. The key is proper acclimatization — don't ascend more 
                            than 300-500m per day above 3,000m, take rest days, stay hydrated, and avoid alcohol. 
                            Medication like Diamox can help. If symptoms worsen, descend immediately. All reputable 
                            guides are trained to recognize and handle altitude sickness.
                        </div>
                    </div>
                </div>
                <div class="faq-item animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        Can I trek independently or do I need a guide?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="faq-answer-inner">
                            As of recent regulations, solo trekking is restricted in many areas, and hiring a 
                            licensed guide or porter is highly recommended (and sometimes mandatory). A guide 
                            provides safety, local knowledge, cultural insights, and navigation expertise. 
                            Popular routes like Annapurna and Everest regions have good teahouse infrastructure, 
                            but a guide enhances the experience significantly.
                        </div>
                    </div>
                </div>
                <div class="faq-item animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        What food is available on the trail?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="faq-answer-inner">
                            Teahouses along popular routes serve a variety of food. Dal Bhat (lentil soup with rice) 
                            is the staple — it's nutritious, unlimited refills, and affordable. You'll also find 
                            pasta, noodle soups, momos (dumplings), pancakes, eggs, and basic Western dishes. 
                            At higher altitudes, options become limited and prices increase. Vegetarian food is 
                            widely available. Always carry some snacks like energy bars, nuts, and chocolate.
                        </div>
                    </div>
                </div>
                <div class="faq-item animate-on-scroll">
                    <div class="faq-question" onclick="toggleFaq(this)">
                        How much does a trek in Nepal cost?
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="faq-answer">
                        <div class="faq-answer-inner">
                            Costs vary widely. Budget trekkers spend $25-40/day on teahouse accommodation and meals. 
                            Permits cost $20-50. Flights to Lukla (for Everest) cost $180-350. A guided package trek 
                            typically costs $1,000-2,500 for 2 weeks including guide, porter, accommodation, meals, 
                            and permits. Add international flights, travel insurance ($100-200), gear, and tips. 
                            Total budget: $1,500-4,000 for a two-week trip including everything.
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ CTA SECTION ============ -->
    <section class="cta">
        <div class="container">
            <div class="cta-content animate-on-scroll">
                <h2>Ready for Your Himalayan Adventure?</h2>
                <p>
                    Life is short and the world is wide. Take the first step towards an 
                    unforgettable journey through Nepal's majestic mountains. Your adventure awaits!
                </p>
                <div class="hero-buttons">
                    <a href="#contact" class="btn btn-primary">
                        <i class="fas fa-paper-plane"></i> Start Planning
                    </a>
                    <a href="#destinations" class="btn btn-outline">
                        <i class="fas fa-map"></i> View All Treks
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ CONTACT ============ -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title animate-on-scroll">
                <h2>Plan Your Trek</h2>
                <p>Get in touch with us to customize your perfect Himalayan trekking adventure</p>
            </div>
            <div class="contact-grid">
                <div class="contact-info animate-on-scroll">
                    <h3>Let's Start Your Journey</h3>
                    <p>
                        Whether you're a first-time trekker or a seasoned mountaineer, our team of experienced 
                        guides and travel experts will help you plan the perfect Nepal trekking adventure. 
                        Reach out to us today!
                    </p>
                    <div class="contact-details">
                        <div class="contact-detail">
                            <div class="contact-detail-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4>Our Office</h4>
                                <p>, Kathmandu, Nepal 44600</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-detail-icon">
                                <i class="fas fa-phone-alt"></i>
                            </div>
                            <div>
                                <h4>Phone</h4>
                                <p>+977 0000000000 / +977 0000000000</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-detail-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <p>Bibek@nepaltreks.com</p>
                            </div>
                        </div>
                        <div class="contact-detail">
                            <div class="contact-detail-icon">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h4>Office Hours</h4>
                                <p>Sun-Fri: 9:00 AM - 6:00 PM (NPT)</p>
                            </div>
                        </div>
                    </div>
                    <div class="contact-social">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-whatsapp"></i></a>
                    </div>
                </div>
                <div class="contact-form animate-on-scroll">
                    <h3>Send Us a Message</h3>
                    <form id="contactForm" onsubmit="handleSubmit(event)">
                        <div class="form-row">
                            <div class="form-group">
                                <label for="firstName">First Name *</label>
                                <input type="text" id="firstName" placeholder="Your first name" required>
                            </div>
                            <div class="form-group">
                                <label for="lastName">Last Name *</label>
                                <input type="text" id="lastName" placeholder="Your last name" required>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="email">Email *</label>
                                <input type="email" id="email" placeholder="your@email.com" required>
                            </div>
                            <div class="form-group">
                                <label for="phone">Phone</label>
                                <input type="tel" id="phone" placeholder="+1 234 567 8900">
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label for="trek">Preferred Trek *</label>
                                <select id="trek" required>
                                    <option value="">Select a trek</option>
                                    <option value="ebc">Everest Base Camp</option>
                                    <option value="ac">Annapurna Circuit</option>
                                    <option value="abc">Annapurna Base Camp</option>
                                    <option value="lv">Langtang Valley</option>
                                    <option value="mc">Manaslu Circuit</option>
                                    <option value="ph">Poon Hill</option>
                                    <option value="um">Upper Mustang</option>
                                    <option value="custom">Custom Trek</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="date">Preferred Date</label>
                                <input type="date" id="date">
                            </div>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" placeholder="Tell us about your trekking experience, group size, special requirements..."></textarea>
                        </div>
                        <button type="submit" class="form-submit">
                            <i class="fas fa-paper-plane"></i> Send Inquiry
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- ============ NEPAL FLAG DIVIDER ============ -->
    <div class="nepal-divider"></div>

    <!-- ============ FOOTER ============ -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-brand">
                    <a href="#" class="logo">
                        <i class="fas fa-mountain"></i>
                        Nepal Treks
                    </a>
                    <p>
                        Your trusted partner for Himalayan trekking adventures since 2009. We are a licensed 
                        and registered trekking agency based in Kathmandu, Nepal, committed to providing safe, 
                        sustainable, and unforgettable trekking experiences.
                    </p>
                    <div class="contact-social">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div>
                    <h4>Quick Links</h4>
                    <ul class="footer-links">
                        <li><a href="#home"><i class="fas fa-chevron-right"></i> Home</a></li>
                        <li><a href="#about"><i class="fas fa-chevron-right"></i> About Nepal</a></li>
                        <li><a href="#destinations"><i class="fas fa-chevron-right"></i> Destinations</a></li>
                        <li><a href="#routes"><i class="fas fa-chevron-right"></i> Trek Routes</a></li>
                        <li><a href="#seasons"><i class="fas fa-chevron-right"></i> Best Seasons</a></li>
                        <li><a href="#gallery"><i class="fas fa-chevron-right"></i> Gallery</a></li>
                        <li><a href="#contact"><i class="fas fa-chevron-right"></i> Contact Us</a></li>
                    </ul>
                </div>
                <div>
                    <h4>Popular Treks</h4>
                    <ul class="footer-links">
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Everest Base Camp</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Annapurna Circuit</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Annapurna Base Camp</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Langtang Valley</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Manaslu Circuit</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Upper Mustang</a></li>
                        <li><a href="#"><i class="fas fa-chevron-right"></i> Poon Hill</a></li>
                    </ul>
                </div>
                <div class="footer-newsletter">
                    <h4>Newsletter</h4>
                    <p>
                        Subscribe to get the latest trekking news, seasonal offers, and travel tips 
                        delivered to your inbox.
                    </p>
                    <form class="newsletter-form" onsubmit="event.preventDefault(); alert('Thank you for subscribing!');">
                        <input type="email" placeholder="Your email address" required>
                        <button type="submit"><i class="fas fa-paper-plane"></i></button>
                    </form>
                    <div style="margin-top: 25px;">
                        <h4>Certifications</h4>
                        <p style="font-size: 0.85rem; opacity: 0.7;">
                            🏅 Nepal Tourism Board Licensed<br>
                            🏅 TAAN Member<br>
                            🏅 NMA Affiliated
                        </p>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Nepal Treks. All rights reserved. Made with ❤️ in Kathmandu</p>
                <p>
                    <a href="#" style="color: var(--secondary);">Privacy Policy</a> | 
                    <a href="#" style="color: var(--secondary);">Terms of Service</a>
                </p>
            </div>
        </div>
    </footer>

    <!-- ============ BACK TO TOP ============ -->
    <button class="back-to-top" id="backToTop" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
        <i class="fas fa-arrow-up"></i>
    </button>

    <!-- ============ LIGHTBOX ============ -->
    <div class="lightbox" id="lightbox" onclick="closeLightbox()">
        <span class="lightbox-close">&times;</span>
        <img src="" alt="Gallery Image" id="lightboxImg">
    </div>

    <!-- ============ JAVASCRIPT ============ -->
    <script>
        // ===== PRELOADER =====
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('preloader').classList.add('hidden');
            }, 1500);
        });

        // ===== NAVBAR SCROLL EFFECT =====
        const navbar = document.getElementById('navbar');
        const backToTop = document.getElementById('backToTop');

        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                navbar.classList.add('scrolled');
                backToTop.classList.add('visible');
            } else {
                navbar.classList.remove('scrolled');
                backToTop.classList.remove('visible');
            }
        });

        // ===== HAMBURGER MENU =====
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Close mobile menu on link click
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });

        // ===== HERO SLIDER =====
        const slides = document.querySelectorAll('.hero-slide');
        let currentSlide = 0;

        function nextSlide() {
            slides[currentSlide].classList.remove('active');
            currentSlide = (currentSlide + 1) % slides.length;
            slides[currentSlide].classList.add('active');
        }

        setInterval(nextSlide, 5000);

        // ===== COUNTER ANIMATION =====
        function animateCounter(elementId, target, suffix = '') {
            const element = document.getElementById(elementId);
            const duration = 2000;
            const step = target / (duration / 16);
            let current = 0;

            function update() {
                current += step;
                if (current >= target) {
                    element.textContent = target + suffix;
                    return;
                }
                element.textContent = Math.floor(current) + suffix;
                requestAnimationFrame(update);
            }
            update();
        }

        // Start counters when hero is in view
        let countersStarted = false;
        const heroObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && !countersStarted) {
                    countersStarted = true;
                    setTimeout(() => {
                        animateCounter('counter1', 150, '+');
                        animateCounter('counter2', 8);
                        animateCounter('counter3', 50, 'K+');
                    }, 1000);
                }
            });
        }, { threshold: 0.5 });

        heroObserver.observe(document.querySelector('.hero'));

        // ===== SCROLL ANIMATIONS =====
        const scrollObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, { 
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        });

        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            scrollObserver.observe(el);
        });

        // ===== FAQ ACCORDION =====
        function toggleFaq(element) {
            const faqItem = element.parentElement;
            const answer = faqItem.querySelector('.faq-answer');
            const isActive = faqItem.classList.contains('active');

            // Close all
            document.querySelectorAll('.faq-item').forEach(item => {
                item.classList.remove('active');
                item.querySelector('.faq-answer').style.maxHeight = '0';
            });

            // Open clicked if it wasn't active
            if (!isActive) {
                faqItem.classList.add('active');
                answer.style.maxHeight = answer.scrollHeight + 'px';
            }
        }

        // ===== FAVORITE HEART TOGGLE =====
        document.querySelectorAll('.dest-favorite').forEach(btn => {
            btn.addEventListener('click', (e) => {
                e.preventDefault();
                const icon = btn.querySelector('i');
                icon.classList.toggle('far');
                icon.classList.toggle('fas');
                if (icon.classList.contains('fas')) {
                    icon.style.color = '#e74c3c';
                    btn.style.background = '#fff';
                } else {
                    icon.style.color = '';
                }
            });
        });

        // ===== LIGHTBOX =====
        function openLightbox(element) {
            const img = element.querySelector('img');
            const lightbox = document.getElementById('lightbox');
            const lightboxImg = document.getElementById('lightboxImg');
            lightboxImg.src = img.src;
            lightbox.classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeLightbox() {
            document.getElementById('lightbox').classList.remove('active');
            document.body.style.overflow = '';
        }

        // Close lightbox with Escape key
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Escape') closeLightbox();
        });

        // ===== FORM SUBMISSION =====
        function handleSubmit(event) {
            event.preventDefault();
            
            const formData = {
                firstName: document.getElementById('firstName').value,
                lastName: document.getElementById('lastName').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                trek: document.getElementById('trek').value,
                date: document.getElementById('date').value,
                message: document.getElementById('message').value
            };

            // Show success message
            const btn = document.querySelector('.form-submit');
            const originalText = btn.innerHTML;
            btn.innerHTML = '<i class="fas fa-check"></i> Message Sent Successfully!';
            btn.style.background = '#27ae60';
            
            setTimeout(() => {
                btn.innerHTML = originalText;
                btn.style.background = '';
                document.getElementById('contactForm').reset();
            }, 3000);

            console.log('Form submitted:', formData);
        }

        // ===== SMOOTH SCROLL FOR ANCHOR LINKS =====
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    const offset = 80;
                    const position = target.getBoundingClientRect().top + window.pageYOffset - offset;
                    window.scrollTo({ top: position, behavior: 'smooth' });
                }
            });
        });

        // ===== ACTIVE NAV LINK HIGHLIGHT =====
        const sections = document.querySelectorAll('section[id]');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 150;
                if (window.scrollY >= sectionTop) {
                    current = section.getAttribute('id');
                }
            });

            document.querySelectorAll('.nav-links a').forEach(link => {
                link.style.color = '';
                if (link.getAttribute('href') === '#' + current) {
                    if (navbar.classList.contains('scrolled')) {
                        link.style.color = 'var(--secondary)';
                    }
                }
            });
        });

        // ===== PARALLAX EFFECT ON HERO =====
        window.addEventListener('scroll', () => {
            const scrolled = window.scrollY;
            const hero = document.querySelector('.hero-content');
            if (hero && scrolled < window.innerHeight) {
                hero.style.transform = `translateY(${scrolled * 0.3}px)`;
                hero.style.opacity = 1 - (scrolled / window.innerHeight);
            }
        });
    </script>
</body>
</html>
```

---

### <a id="📄-readme-md"></a>📄 `README.md`

**File Info:**
- **Size**: 1.43 KB
- **Extension**: `.md`
- **Language**: `text`
- **Location**: `README.md`
- **Relative Path**: `root`
- **Created**: 2026-03-30 14:15:48 (Asia/Katmandu / GMT+06:45)
- **Modified**: 2026-04-01 05:33:49 (Asia/Katmandu / GMT+06:45)
- **MD5**: `cfb89d1ffdfa9453ada4c3bb39d0f82a`
- **SHA256**: `f9045cda2bd224ae3b1e39ff70e303a5cc40d463d4f8308a94c04480ddca8799`
- **Encoding**: ASCII

**File code content:**

````markdown
# AWS Scalable Web Architecture

## Project Overview
This project demonstrates a scalable and highly available web application architecture on AWS using core cloud services.

The architecture includes static website hosting using S3, compute using EC2, traffic distribution using Application Load Balancer, and automatic scaling using Auto Scaling Group.

## Services Used
- Amazon S3 (Static Website Hosting)
- Amazon EC2 (Ubuntu + Nginx)
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- VPC (Public Subnets, Route Tables, Internet Gateway)
- Security Groups

## Key Features
- High Availability using Multi-AZ deployment
- Load Balancing using ALB
- Auto Scaling for handling traffic spikes
- Static website hosting using S3
- Secure access using Security Groups

## Implementation Details
Detailed steps are documented in:
- docs/steps.md
- docs/commands.md
- docs/architecture.md

## Challenges Faced
- EC2 Connect failed due to incorrect SSH rules
- ALB required at least 2 public subnets
- S3 static website returned Access Denied errors
## Solutions
- Updated security groups to allow SSH properly
- Created second public subnet in a different Availability Zone
- Fixed S3 bucket policy and routing configuration

## Key Learnings
- Difference between public and private subnets
- How Load Balancer distributes traffic
- Importance of security groups
- How Auto Scaling works
- S3 static hosting behavior

````

---

