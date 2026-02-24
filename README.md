# SMS Segment Optimizer 📱💬

## Overview
The **SMS Segment Optimizer** is a lightweight, purpose-built tool designed to analyze SMS text inputs in real-time. It detects the underlying character encoding (GSM-7 vs. Unicode/UCS-2), calculates the exact number of message segments required for transmission, and estimates the resulting SMS costs. 

This project was specifically developed to address a common telecom and CPaaS challenge: optimizing SMS routing costs by preventing accidental Unicode character inclusion, which drastically reduces the character limit per message segment.

## Motivation
This tool was built as a practical demonstration of problem-solving for a job application with **Bhash Software Labs**. It showcases an understanding of telecommunications infrastructure, message encoding standards, and cost-efficiency in bulk SMS routing.

## Key Features
* **Encoding Detection:** Automatically detects whether a message consists purely of the standard GSM-7 character set or if it contains Unicode (UCS-2) characters (like emojis or regional language scripts).
* **Accurate Segmentation:** Calculates message segments based on standard telecom rules:
  * **GSM-7:** 160 characters for a single segment, 153 characters per segment for multi-part messages.
  * **Unicode:** 70 characters for a single segment, 67 characters per segment for multi-part messages.
* **Cost Estimation:** Provides an immediate calculation of the total message cost based on the number of generated segments.
* **Real-time Feedback:** Instantly updates segment counts and encoding types as the user types.

## Use Case
In bulk SMS marketing or transactional messaging, a single accidental Unicode character (like a smart quote `”` instead of a straight quote `"`) can force an entire 160-character GSM message into a 70-character Unicode format. This splits the message into multiple segments, doubling or tripling the billing cost from the telecom operator. This tool helps identify and prevent those costly mistakes.

## Getting Started

### Prerequisites
* A modern web browser (if running locally as an HTML/JS file) or your preferred IDE.
