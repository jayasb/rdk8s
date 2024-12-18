# Rancher Desktop - Kubernetes

Infrastructure as Code (IaC) and GitOps implementation for Kubernetes.

## Repository Structure
```bash
├── apps/                     # Application configurations
│   ├── dashy/               # Dashy dashboard
│   └── petclinic/           # Spring PetClinic
└── infrastructure/          # Shared infrastructure
    ├── cert-manager/        # SSL/TLS certificates
    ├── config/              # Common configurations
    ├── ingress/            # Ingress configurations
    ├── monitoring/         # Prometheus & Grafana
    └── postgres/           # Database configurations