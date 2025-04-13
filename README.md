# Simple Anonymizer

## Overview

The **Simple Anonymizer** is a lightweight, browser-based tool for anonymizing sensitive information in text. It uses built-in patterns to detect and redact common types of Personally Identifiable Information (PII) and allows users to define custom redaction patterns using regular expressions.

## Features

- Anonymize text directly in your browser.
- Built-in patterns for detecting sensitive data like emails, phone numbers, and more.
- Define custom redaction patterns using JavaScript regular expressions.
- No data is sent anywhere — everything runs locally in your browser.

## How It Works

1. Paste the text you want to anonymize into the "Paste Text Here" input area.
2. Optionally, define custom redaction patterns using JavaScript regular expressions in the "Custom Redaction Patterns" input area.
3. Click the "Anonymize Text" button to process the text.
4. View the anonymized text in the output area.

## Built-in Redaction Rules

The following built-in rules are applied automatically:

- **Email**: Matches email addresses.
- **Phone Number**: Matches various phone number formats, including optional country codes.
- **SSN**: Matches US Social Security Numbers in the format `XXX-XX-XXXX`.
- **Credit Card Like**: Matches sequences of 13-19 digits, optionally separated by spaces or dashes.
- **IBAN Like**: Matches basic IBAN-like patterns.
- **IPv4 Address**: Matches IPv4 addresses.
- **Long Number Sequence**: Matches numeric sequences of 9 or more digits.

## Custom Redaction Patterns

Custom patterns can be defined using JavaScript regular expressions. Each pattern should be written on a new line. You can include flags (e.g., `/pattern/gi`), and if no flags are provided, the global flag (`g`) will be assumed.

### Example Custom Patterns

- `/\bProject[\s_]?Confidential\b/gi` - Matches "Project Confidential" with optional spaces or underscores.
- `/ACME-\d{4}/g` - Matches "ACME-" followed by 4 digits.

## How to Use Locally

To use the tool locally:

1. Download the `index.html` file from this repository.
2. Open the file in any modern web browser.
3. Follow the steps in the "How It Works" section to anonymize your text.

Since the tool runs entirely in your browser, no data is sent to any server, ensuring your privacy.

## Disclaimer

This tool is designed for basic anonymization tasks and may not cover all edge cases or specific requirements. Use it with caution and verify the results before sharing anonymized data.