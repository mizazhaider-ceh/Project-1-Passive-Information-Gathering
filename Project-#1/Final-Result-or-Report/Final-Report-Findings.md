# Final Report: mudassaracademy.com Investigation / Passive Information Gathering

**Author:** Muhammad Izaz Haider  
**Date:** 2025-02-01  

## Table of Contents

- [Final Report: mudassaracademy.com Investigation / Passive Information Gathering](#final-report-mudassaracademycom-investigation--passive-information-gathering)
  - [Table of Contents](#table-of-contents)
  - [Importance of This Project](#importance-of-this-project)
  - [1. Host Information](#1-host-information)
  - [2. DNS Reconnaissance](#2-dns-reconnaissance)
  - [3. Robots.txt Analysis](#3-robotstxt-analysis)
  - [4. Sitemap.xml Analysis](#4-sitemapxml-analysis)
  - [5. Dig Analysis](#5-dig-analysis)
  - [6. NSLookup Analysis](#6-nslookup-analysis)
  - [7. WhatWeb Analysis](#7-whatweb-analysis)
  - [8. WHOIS Lookup](#8-whois-lookup)
  - [9. Wappalyzer Technology Fingerprinting](#9-wappalyzer-technology-fingerprinting)
  - [10. Web Application Firewall Detection](#10-web-application-firewall-detection)
  - [11. Subdomain Enumeration](#11-subdomain-enumeration)
  - [12. Email Security \& Data Breach Check](#12-email-security--data-breach-check)
  - [13. Contact Information](#13-contact-information)
  - [14. Conclusion](#14-conclusion)

## Importance of This Project

This investigation is crucial for understanding the security posture of the website **mudassaracademy.com**, which is actively engaged in online services. The findings from this report provide valuable insights into the domain's security, technological stack, and associated services, highlighting potential vulnerabilities and areas for improvement. This project helps in:

- Identifying and addressing any security weaknesses.
- Ensuring that the domain is properly configured and secured against common attack vectors.
- Assisting in compliance with web security best practices.
- Providing a foundation for further security enhancements, including domain protection and WAF optimization.

## 1. Host Information

- **Domain:** mudassaracademy.com
- **IP Address:** 209.145.50.90
- **Mail Server:** mudassaracademy.com (handled by itself)

## 2. DNS Reconnaissance

**Command Used:** `dnsrecon -d mudassaracademy.com`

**Results:**

- **SOA:** us1.pakihosting.com (209.145.50.90)
- **NS:** us1.pakihosting.com (209.145.50.90), us2.pakihosting.com (209.145.50.90)
- **MX:** mudassaracademy.com (209.145.50.90)
- **A Record:** 209.145.50.90
- **TXT Records:**
  - `v=spf1 ip4:209.145.50.90 +a +mx +ip4:209.145.62.123 ~all`
  - `_dmarc.mudassaracademy.com v=DMARC1; p=reject; sp=none; rf=afrf; pct=100; ri=86400;`
- **DNSSEC:** Not Configured
- **SRV Records:** None Found

## 3. Robots.txt Analysis

**URL:** `robots.txt`

**Findings:**

- `User-agent: *`
- `Crawl-delay: 15000`
- **Disallowed Paths:**
  - `/wp-admin/`
  - `/wp-admin/admin-ajax.php`
  - `/wp-cron.php`

## 4. Sitemap.xml Analysis

**URL:** `Sitemap`

**Sub-Sitemaps:**

- **Post Sitemap:** post-sitemap.xml (Last Modified: 2024-08-25)
- **Page Sitemap:** page-sitemap.xml (Last Modified: 2024-08-08)
- **Testimonials Sitemap:** testimonials-sitemap.xml (Last Modified: 2024-04-18)
- **Courses Sitemap:** courses-sitemap.xml (Last Modified: 2024-08-09)
- **Category Sitemap:** category-sitemap.xml (Last Modified: 2024-08-25)
- **Local Sitemap:** local-sitemap.xml (Last Modified: 2025-01-17)

## 5. Dig Analysis

**Command Used:** `dig mudassaracademy.com`

**Findings:**

- **Query Time:** 20 msec
- **Server:** 10.0.2.3#53
- **Response:**
  - `mudassaracademy.com. 12442 IN A 209.145.50.90`

## 6. NSLookup Analysis

**Command Used:** `nslookup mudassaracademy.com`

**Results:**

- **Server:** 10.0.2.3
- **Address:** 10.0.2.3#53
- **Non-authoritative Answer:**
  - `mudassaracademy.com -> 209.145.50.90`

## 7. WhatWeb Analysis

**Command Used:** `whatweb mudassaracademy.com`

**Results:**

- **HTTP Status:** 403 Forbidden
- **Country:** United States (US)
- **IP Address:** 209.145.50.90
- **Title:** 403 Forbidden
- **Technologies:** HTML5

## 8. WHOIS Lookup

**Command Used:** `whois mudassaracademy.com`

**Results:**

- **Domain ID:** 2388306600_DOMAIN_COM-VRSN
- **Registrar:** NameCheap, Inc.
- **Registrar WHOIS Server:** whois.namecheap.com
- **Registrar URL:** NameCheap
- **Updated Date:** 2024-08-15
- **Creation Date:** 2019-05-07
- **Registry Expiry Date:** 2025-05-07
- **Registrar Abuse Contact:** abuse@namecheap.com
- **Registrar Abuse Phone:** +1.6613102107
- **Domain Status:** OK
- **Name Servers:**
  - US1.PAKIHOSTING.COM
  - US2.PAKIHOSTING.COM
- **DNSSEC:** Unsigned
- **ICANN WHOIS Complaint Form:** ICANN WICF
- **Last WHOIS Database Update:** 2025-02-01

## 9. Wappalyzer Technology Fingerprinting

- **CMS:** WordPress 6.7.1
- **JavaScript Frameworks:** GSAP 3.11.2
- **Font Scripts:** Google Font API, Font Awesome, Twitter Emoji (Twemoji)
- **Miscellaneous:** RSS, Open Graph, Prism, Popper, HTTP/3
- **Programming Languages:** PHP
- **Marketing Automation:** MailChimp, MailChimp for WordPress 4.9.11
- **Databases:** MySQL
- **Maps:** Google Maps
- **Page Builder:** Elementor 3.21.0
- **SEO:** RankMath SEO
- **JavaScript Libraries:** core-js 3.32.0, Underscore.js 1.13.7, Swiper, jQuery UI 1.12.1, jQuery Migrate 3.4.1, jQuery 3.7.1
- **UI Frameworks:** Bootstrap 4.1.1
- **Email Services:** MailChimp
- **WordPress Plugins:** RankMath SEO, WPForms 1.8.7.2, Redux Framework 4.4.0.1, Elementor 3.21.0, Contact Form 7 5.9.3, MailChimp for WordPress 4.9.11

## 10. Web Application Firewall Detection

**Command Used:** `wafw00f https://mudassaracademy.com`

- **Findings:**
  - The site appears to be behind a **WAF or security solution**.
  - **Server Header Behavior:**
    - Normal response header: `imunify360-webshield/1.21`
    - Attack response header: `""`
  - **Number of Requests:** 6
  - **Error:** Read timeout on HTTPS requests.

## 11. Subdomain Enumeration

**Tools Used:** Sublist3r & Google Dorks

- **Findings:** No subdomains were found.
- **Google & VirusTotal blocking enumeration requests.**

## 12. Email Security & Data Breach Check 🔐📧  

**Tool Used:** *Have I Been Pwned*  

- **Results:** ⚠️ **1 breach found** for the associated email.  
- **Details:** The email was found in a known data breach, which may expose credentials or sensitive information.  

## 13. Contact Information

- **Address:** Bharth Sialkot City, Punjab, Pakistan
- **Phone Numbers:**
  - +92 3140370037
  - +92 3107335707
- **Email:** mudassaracademy786@gmail.com
- **Social Media:**
  - **LinkedIn:** [Mudassar Academy](https://pk.linkedin.com/in/mudassaracademy786)
  - **Facebook:** [Mudassar Academy](https://web.facebook.com/mudassaracademy/)
  - **Instagram:** [Mudassar Academy](https://www.instagram.com/mudassaracademy786/)

## 14. Conclusion

This investigation uncovered a wealth of useful information about the domain **mudassaracademy.com**. The analysis successfully met the five objectives outlined at the start of the project:

- **Purpose of Passive Information Gathering:**
  1. **Identifying IP addresses and DNS details**: The IP address (209.145.50.90) and DNS details were successfully retrieved, showing the domain's hosting configuration and associated name servers.
  2. **Gathering domain ownership and domain-related information**: WHOIS data was gathered, providing details about the domain's registration, ownership, and the registrar.
  3. **Identifying email addresses and social media profiles linked to the target**: The investigation successfully found email addresses associated with the domain and various linked social media profiles (LinkedIn, Facebook, Instagram).
  4. **Discovering the web technologies used on the target site**: The Wappalyzer and WhatWeb analysis revealed a detailed list of technologies, including the use of WordPress, various JavaScript frameworks, and specific plugins.
  5. **Identifying subdomains**: While no subdomains were identified due to restrictions on enumeration, the effort to find subdomains was thorough and complete.

The findings provide an in-depth overview of the domain's security posture, technologies, and associated services, which are vital for assessing vulnerabilities and further strengthening the site.



**Prepared by:** Muhammad Izaz Haider   
**Date:** 2025-02-01
