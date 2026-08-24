
# 🌐 Tarliam Global Website

A real-world business website developed and deployed for **Tarliam Global**.

This project gave me practical experience working with website development, domain configuration, hosting, DNS, HTTPS/SSL, deployment, and basic web security considerations.

---

## 🎯 Project Overview

The goal of this project was to create a professional online presence for Tarliam Global and make the company's services and information accessible through a dedicated website.

The project involved more than simply creating web pages. I also worked with the infrastructure required to make the website publicly accessible, including domain configuration, hosting, DNS records, SSL/HTTPS, and search engine indexing.

---

## 🚀 Project Goals

* Create a professional business website
* Deploy the website publicly
* Connect a custom domain
* Configure DNS records
* Enable HTTPS/SSL
* Make the website accessible across devices
* Configure business email services
* Submit the website to search engines
* Learn about the infrastructure behind a production website

---

## 🛠️ Technologies & Services

| Technology / Service    | Purpose                                 |
| ----------------------- | --------------------------------------- |
| HTML / CSS / JavaScript | Website development                     |
| Netlify                 | Website hosting and deployment          |
| Custom `.ae` Domain     | Public website address                  |
| DNS                     | Domain and infrastructure configuration |
| HTTPS / SSL             | Secure communication                    |
| Zoho Mail               | Business email                          |
| Google Search Console   | Search indexing and monitoring          |

---

## 🌐 Infrastructure

### Domain

The website uses a custom `.ae` domain.

### Hosting

The website is deployed using Netlify.

### DNS

DNS records were configured to connect the custom domain with the hosting infrastructure.

### HTTPS

HTTPS/SSL was configured to encrypt communication between visitors and the website.

### Email

Business email infrastructure was configured separately using Zoho Mail.

---

## 🔐 Cybersecurity Learning

Although this was primarily a business website project, it helped me understand several cybersecurity concepts in a practical environment.

### 1. DNS

Learned how domains are connected to infrastructure using DNS records.

Concepts explored:

* DNS records
* CNAME
* A records
* Domain verification
* DNS propagation

### 2. HTTP & HTTPS

Learned the difference between HTTP and HTTPS and why TLS/SSL is important for protecting communication between users and websites.

### 3. Network Exposure

Used Nmap to inspect the publicly accessible domain and understand what services were exposed.

Example:

```bash
nmap -sV <authorized-domain>
```

The scan helped me understand:

* Open ports
* Running services
* Service detection
* HTTP/HTTPS exposure

### 4. Web Security

This project introduced me to basic web security considerations including:

* HTTPS
* Secure configuration
* Domain security
* Exposure of public services
* Security headers
* Input validation
* Protecting sensitive information

---

## 🔎 Security Testing

Security testing was performed only against infrastructure that I was authorized to test.

The purpose was to understand how a publicly accessible website appears from a security perspective.

Areas explored:

```text
Domain
   ↓
DNS
   ↓
Hosting
   ↓
Open Services
   ↓
HTTP/HTTPS
   ↓
Web Application
```

---

## 📚 What I Learned

This project helped me understand that cybersecurity isn't limited to tools such as Nmap or Metasploit.

A real website involves multiple layers:

```text
Domain
   ↓
DNS
   ↓
Hosting
   ↓
Web Server
   ↓
HTTPS/TLS
   ↓
Web Application
   ↓
User
```

Understanding how these components interact is important when learning both offensive and defensive security.

---

## 💡 Challenges

During development and deployment, I encountered issues involving:

* DNS configuration
* Domain verification
* CNAME configuration
* MX records
* SSL/HTTPS configuration
* Search engine verification
* Website deployment

Troubleshooting these issues helped me understand how production websites are actually deployed and maintained.

---

## 📸 Screenshots

Screenshots of the website and relevant configuration will be added here.

```text
screenshots/
├── homepage.png
├── services.png
├── mobile-view.png
└── deployment.png
```

---

## 📈 Future Improvements

* Perform a structured web security assessment
* Learn and implement security headers
* Review TLS configuration
* Perform vulnerability scanning in an authorized environment
* Improve website security monitoring
* Document security findings and remediation
* Learn more about web application security

---

## 🧠 Key Takeaways

> Building a website taught me how the different layers of the web connect together.

The project gave me practical exposure to:

**Web Development → DNS → Hosting → HTTPS → Networking → Security**

This became one of my first projects where I could connect my development experience with my growing cybersecurity knowledge.

---

## ⚠️ Disclaimer

Any security testing associated with this project is performed only against systems and infrastructure that I own or have explicit authorization to test.
