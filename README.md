# Sentinel Privacy Shield

Privacy-by-design toolkit for PII detection, redaction, and reporting.

## Features

- **PII Detection**: Identify personally identifiable information (names, emails, phones, SSN, etc.)
- **Automatic Redaction**: Mask or remove PII from text/documents
- **Reporting**: Generate compliance reports (GDPR, HIPAA)
- **Multi-Format**: Support for text, JSON, CSV, and documents
- **Rust Core**: High-performance PII detection via Rust backend
- **Dashboard**: React-based UI for interactive analysis

## Architecture

```
sentinel-privacy-shield/
├── core/           # Python detection logic
├── core-rust/      # Rust performance-critical code
├── dashboard-react/ # Web UI
├── notebooks/      # Jupyter analysis notebooks
└── docs/           # Documentation
```

## Installation

```bash
# Python package
pip install sentinel-privacy-shield

# From source
git clone https://github.com/Brainfeed-1996/sentinel-privacy-shield.git
cd sentinel-privacy-shield
pip install -e .
```

## Usage

```python
from sentinel_privacy_shield import detect_pii, redact_pii

# Detect PII
results = detect_pii("Contact: john.doe@email.com, phone: +33 6 12 34 56 78")
print(results)

# Redact PII
redacted = redact_pii("Contact: john.doe@email.com")
```

## CLI

```bash
sentinel-privacy-shield --input document.txt --output redacted.txt --report
```

## Notebooks

- `notebooks/01_pii_detection_redaction_pipeline.ipynb` — PII detection + redaction + evaluation

## Compliance

Supports detection for:
- GDPR (EU)
- HIPAA (US Healthcare)
- CCPA (California)

## License

MIT
