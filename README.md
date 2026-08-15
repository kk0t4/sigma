# Japan Threat Detections

Detection rules created from publicly reported malware and cyber threat activity, primarily focusing on threats targeting Japan.

This repository is intended both as a personal Detection Engineering practice project and as a collection of detection rules that may be useful to defenders and security researchers.

## Scope

The repository focuses on translating publicly available threat intelligence into practical detection logic.

Current rule formats include:

- **Sigma** — Behavior-based detection rules for endpoint and log telemetry
- **YARA** — File and malware detection rules based on static characteristics

Additional detection formats may be added in the future when appropriate.

## Repository Structure

```text
.
├── sigma/
│   └── ...
├── yara/
│   └── ...
└── README.md
```

## Detection Approach

Rules are created based on publicly available information such as:

- Threat research reports
- Malware analysis reports
- Incident reports
- Security researcher publications
- Public sandbox analysis results

Where possible, rules focus on behavioral or relatively stable characteristics rather than short-lived indicators such as individual IP addresses or file hashes.

Not every reported threat will have both Sigma and YARA rules. Rules are created only when useful and reasonably reliable detection opportunities can be identified.

## Rule Status

Most rules in this repository should be considered **experimental** unless otherwise stated.

They are created primarily for research and Detection Engineering practice and may require additional validation, tuning, and false-positive analysis before use in production environments.

## References

Each rule includes references to the public sources used to derive the detection logic whenever possible.

These references are intended to make it easier to:

- Understand the original threat activity
- Review the reasoning behind the detection
- Validate or improve the rule
- Perform additional investigation or threat hunting

## Disclaimer

The rules provided in this repository are offered for research and defensive security purposes.

No guarantee is made regarding detection accuracy, completeness, or suitability for any particular environment.

Before deploying any rule in a production environment, review and test it against your own telemetry and operational requirements.

## Feedback

Feedback, corrections, and suggestions are welcome.

If you find a false positive, missed detection opportunity, or other issue with a rule, please feel free to open an issue or submit a pull request.