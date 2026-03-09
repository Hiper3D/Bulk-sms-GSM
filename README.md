# 📱 SMS Segment Optimizer: Telecom Routing & Cost Calculator

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Telecom](https://img.shields.io/badge/Telecom-CPaaS-0052CC?style=for-the-badge)

## 📌 Executive Overview
The **SMS (Short Message Service - a text messaging service component of telephone, internet, and mobile device systems) Segment Optimizer** is a purpose-built, lightweight application engineered to analyze telecom text payloads in real-time. 

Architected specifically to solve a persistent routing and billing challenge within the CPaaS (Communications Platform as a Service - a cloud-based platform that enables developers to add real-time communications features to their own applications) industry, this tool demonstrates a deep understanding of telecommunications infrastructure. It was developed as a practical proof-of-concept for Bhash Software Labs to optimize enterprise messaging costs by preventing accidental character encoding shifts that drastically reduce per-segment payload capacities.

## 🏗️ Core Architecture & Logic Implementation



### 1. Dynamic Encoding Detection
* **Real-Time Parsing:** The underlying logic actively scans input strings to instantly detect the required character encoding standard. It differentiates between purely standard GSM (Global System for Mobile Communications - a standard developed to describe the protocols for second-generation digital cellular networks) character sets and payloads requiring UCS-2 (2-byte Universal Character Set - a character encoding standard that uses exactly 16 bits to represent each character) encoding (triggered by emojis or regional language scripts).

### 2. Algorithmic Segmentation Math
* **Cost Calculation:** The tool accurately calculates the exact number of message segments required for network transmission based on strict telecom carrier rules:
  * **GSM-7 Standard:** Allocates 160 characters for a standalone segment, dynamically adjusting to 153 characters per segment for concatenated, multi-part payloads.
  * **Unicode Standard:** Restricts capacity to 70 characters for a standalone segment, shifting to 67 characters per segment for concatenated messages.

### 3. Enterprise Use Case: Billing Optimization
* **Financial Impact:** In high-volume transactional or marketing deployments, a single stray Unicode character (e.g., a localized smart quote `”` instead of a standard straight quote `"`) forces the entire payload into the 70-character UCS-2 format. This silently splits a standard 160-character payload into three separate billable segments, tripling the routing cost. This optimizer proactively identifies and mitigates these costly encoding errors prior to dispatch.

## ⚙️ Deployment & Initialization
Because this is a decoupled, client-side utility, provisioning a complex runtime environment is not required.

### Prerequisites
* A modern web browser to execute the localized HTML (HyperText Markup Language - the standard code used to structure a web page) and JS (JavaScript - a programming language that lets you implement complex features on web pages) execution context.
* Alternatively, load the source files into your preferred IDE (Integrated Development Environment - a software application that provides comprehensive facilities to computer programmers for software development) for further modification and testing.
