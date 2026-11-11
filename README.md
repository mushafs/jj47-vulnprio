# jj47-vulnprio

COMP-474 (Vulnerability Assessment & Reverse Engineering), PAF-IAST, Fall 2026. Team JJ47.
AI-Driven Vulnerability Prioritization: Wazuh manager + Logstash + Elasticsearch + Kibana, with an LLM-assisted prioritization and remediation engine.

## Team and module ownership
| Member | Role | Owns |
|---|---|---|
| Mushaf Saleem | Project lead, integration, QA and metrics | repo, integration, `eval/`, report |
| Noor Eman Fatimah | SIEM platform engineer | M-SIEM |
| Hasnain Shah Saad | Vulnerability analyst | M-VUL, M-DSH |
| Abdullah Tipu | AI / LLM engineer | M-AI |
| Shaheer Ahmad | Log-source and network security engineer | M-LOG, M-NET |
| Izhar Ul Haq | Remediation engineer | M-REM, M-PAT |

## Repository layout
```
siem/      Wazuh manager config, agent.conf, custom rules and decoders
logstash/  pipelines, enrichment dictionaries
elastic/   ILM, templates, transforms, Kibana exports (.ndjson)
engine/    scoring, enrichment, LLM client, prompts, routing
netdev/    scan scripts, ingest, config checks
patch/     orchestrator, playbooks, Active Response scripts
eval/      dataset, rubric, evaluation scripts, results
docs/      report, diagrams, test records, screenshots
```

## Versions (fill in as installed)
| Component | Version | Host |
|---|---|---|
| Wazuh manager | TBD | siem-01 |
| Wazuh agent (Linux) | TBD (must match manager) | Ubuntu agent |
| Wazuh agent (Windows) | TBD (must match manager) | Windows agent |
| Elasticsearch | TBD | es-01 |
| Kibana | TBD (same as Elasticsearch) | es-01 |
| Logstash | TBD (same minor as Elasticsearch) | siem-01 |

## Credentials policy
- No passwords, API keys, certificates or private keys are ever committed. `.gitignore` blocks the common ones.
- Logstash credentials live only in the Logstash keystore.
- Logstash uses a least-privilege Elasticsearch user, never `elastic`.

## Rules of engagement
Scan, attack and patch only our own isolated lab. No live exploitation. No real organisational data.

## Working rules
- Every member commits under their own name. Work goes through pull requests with one reviewer.
- Screenshots go in `docs/screenshots/` using the naming pattern in `docs/README.md`.
- AI-assistant use is disclosed in the report appendix.
