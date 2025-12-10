# My On-Prem DevOps Stack

A self-hosted DevOps environment using Docker Compose, featuring GitLab for repositories, Jenkins for CI/CD, Grafana with Loki and Prometheus for monitoring, and a simple webpage dashboard. Perfect for personal or small-team deployments before pushing to production.

## Features
- **GitLab CE**: Version control and project management.
- **Jenkins**: Automated builds, tests, and deployments.
- **Grafana + Loki + Prometheus**: Logging, metrics, and dashboards.
- **Webpage Dashboard**: Simple HTML page with links to all services.
- **Security Scanning**: Integrated Trivy for vulnerability checks.

## Prerequisites
- Linux server with Docker and Docker Compose installed.
- At least 8-16 GB RAM and 100 GB storage.
- Nginx Proxy Manager (or similar) on a separate machine for routing.

## Setup Instructions
1. Clone this repo: `[git clone https://github.com/yourusername/your-repo-name.git](https://github.com/SpindlyFox20703/DevOps)`
2. Create required files:
   - `.env` with your passwords and URLs (see `.env.example`).
   - `prometheus.yml` and `loki-config.yml` (provided in the repo).
   - `webpage/index.html` (or use the template for dynamic generation).
3. Run `docker-compose up -d`.
4. Configure your Nginx Proxy Manager to route subdomains to the services.
5. Access via your DNS (e.g., `https://gitlab.yourdomain.com`).

## Usage
- Log in to services with the passwords from `.env`.
- Set up Jenkins pipelines, Grafana datasources, and Trivy scans as needed.
- Monitor with `docker-compose logs` or Grafana dashboards.

## Contributing
Feel free to fork and improve! Open issues for bugs or suggestions.

## License
This project is open-source under the MIT License.

## Credits and Acknowledgments

This setup was inspired and guided by assistance from Grok, an AI built by xAI. Special thanks to the open-source communities behind Docker, GitLab, Jenkins, Grafana, Loki, Prometheus, and Trivy for making self-hosted DevOps accessible.
