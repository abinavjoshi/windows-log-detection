# windows-log-detection
Beginner SOC Analyst Project using Sigma rules for threat detection


This repository contains a beginner-level SOC (Security Operations Center) analyst project focused on detecting and analyzing failed logon attempts using Windows Security Event Logs.

## Objective

The goal of this project is to simulate a real-world SOC workflow by detecting suspicious authentication events and documenting the response process. I created this project to help beginners understand the basics of log analysis, Sigma rule usage, and detection reporting.

## Tools Used

- Sigma: Generic signature format for SIEM systems.
- Chainsaw: Fast Windows event log parser that uses Sigma rules for detection.
- EVTX Logs: Windows Event Log format used as the raw log input.
- GitHub: For version control and project portfolio hosting.

## Project Structure

windows-log-detection/
│
├── logs/
│   └── FailedLogon.evtx                # Sample Windows Event Log file
│
├── detections/
│   └── failed_logon.json              # Detection output from Chainsaw
│
├── analysis/
│   ├── detection-notes.md             # SOC-style report describing the alert
│   └── soc-response-checklist.md      # Checklist of steps taken during investigation
│
├── mappings/
│   └── mapping.yml                    # Chainsaw mapping file (optional, if customized)
│
├── sigma_rules/
│   └── failed_logon.yml               # Custom Sigma detection rule
│
└── README.md                          # This file

## Steps Performed

1. Collected a sample `.evtx` Windows Security log file containing failed logon events.
2. Wrote a Sigma rule to detect failed logon attempts by analyzing `Event ID 4625`.
3. Ran Chainsaw with the Sigma rule and the `.evtx` file to detect suspicious logon attempts.
4. Captured and saved the JSON detection output from Chainsaw in the `detections/` folder.
5. Wrote an analyst-style detection report and saved it in `analysis/detection-notes.md`.
6. Created a SOC response checklist to document steps and best practices in `soc-response-checklist.md`.
7. Pushed the project to GitHub to serve as part of my cybersecurity learning portfolio.

## Key Learning Outcomes

- Understanding how to use Sigma rules for log-based threat detection.
- Learning to parse and analyze Windows Security Event Logs.
- Documenting detections and responses in a structured SOC report format.
- Using Git for version control and GitHub for project hosting.

## Notes

This project was built as part of a beginner-friendly SOC analyst learning path and is intended for educational purposes only. All log data used is simulated or publicly available test data.
