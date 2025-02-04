
# Commands and Tools Used 🛠️

## 1️⃣ `whatis whatis`

**Purpose:** Displays a brief description of the `whatis` command.

## 2️⃣ `whatis host`

**Purpose:** Provides a short description of the `host` command, which is used for DNS lookups.

## 3️⃣ `whatweb mudassaracademy.com`

**Purpose:** Analyzes the website to detect CMS, technologies, and frameworks used.

## 4️⃣ `whois -I mudassaracademy.com`

**Purpose:** Retrieves domain registration details, owner information, and expiration details.

## 5️⃣ `url/robots.txt`

**Purpose:** Checks the robots.txt file for restricted website paths and indexing rules.

## 6️⃣ `url/sitemap.xml`

**Purpose:** Extracts the sitemap to find listed URLs and potential entry points.

## 7️⃣ `whatweb mudassaracademy.com`

**Purpose:** Scans the website again for additional insights about its technologies.

## 8️⃣ `httrack -d`

**Purpose:** Downloads a copy of the website for offline analysis.

## 9️⃣ `whois -I mudassaracademy.com`

**Purpose:** Retrieves domain details again for verification.

## 🔟 `dnsrecon -d mudassaracademy.com`

**Purpose:** Conducts DNS reconnaissance to find subdomains, records, and configurations.

## 1️⃣1️⃣ `nslookup mudassaracademy.com`

**Purpose:** Queries the DNS records to fetch details like IP address and mail server.

## 1️⃣2️⃣ `dig mudassaracademy.com`

**Purpose:** Retrieves DNS information, including A, MX, TXT, and CNAME records.

## 1️⃣3️⃣ `wafw00f mudassaracademy.com`

**Purpose:** Detects the presence of a Web Application Firewall (WAF) and its type.

## 1️⃣4️⃣ `sublist3r mudassaracademy.com`

**Purpose:** Enumerates subdomains of the target domain using multiple sources.

## 1️⃣5️⃣ Dorks Used 🔍

Google Dorking was performed to extract hidden or sensitive data:

- `inurl:admin/forum` → Finds admin-related forums.
- `site:*.mudassaracademy.com>subdomains` → Lists subdomains.
- `site:*.mudassaracademy.com inurl:admin` → Searches for admin pages.
- `site:*.mudassaracademy.com intitle:admin` → Finds admin-related pages.
- `site:mudassaracademy.com filetype:pdf` → Finds PDF files.
- `site:*.mudassaracademy.com filetype:pdf` → Finds PDFs across subdomains.
- `site:mudassaracademy.com employees` → Looks for employee-related pages.
- `site:mudassaracademy.com instructors` → Searches for instructor details.
- `intitle:index of` → Finds directories that might expose files.

## 1️⃣6️⃣ `theHarvester -d mudassaracademy.com`

**Purpose:** Collects email addresses, subdomains, and employee details using OSINT techniques.
