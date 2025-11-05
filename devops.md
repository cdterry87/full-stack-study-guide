# DevOps

## 🧩 Beginner Level

- **Question:** What is DevOps?  
  **Answer:** A culture and set of practices combining software development and IT operations to shorten the development lifecycle and deliver software faster and more reliably.

- **Question:** What are the key goals of DevOps?  
  **Answer:** Continuous integration, continuous delivery, faster deployment, improved collaboration, automation, and infrastructure as code.

- **Question:** What is CI/CD?  
  **Answer:** Continuous Integration (CI) automatically builds and tests code; Continuous Deployment (CD) automatically releases it to production.

- **Question:** What is the difference between Continuous Delivery and Continuous Deployment?  
  **Answer:** Continuous Delivery requires manual approval for production releases; Continuous Deployment pushes changes automatically.

- **Question:** What is version control and why is it important in DevOps?  
  **Answer:** It tracks code changes, enables collaboration, rollback, and is central to CI/CD pipelines.

- **Question:** What are some popular CI/CD tools?  
  **Answer:** GitHub Actions, GitLab CI, Jenkins, CircleCI, Bitbucket Pipelines, Travis CI.

- **Question:** What is containerization?  
  **Answer:** Packaging software with its dependencies in isolated environments (containers) for consistent deployment.

- **Question:** What’s the difference between a container and a virtual machine?  
  **Answer:** Containers share the host OS kernel and are lightweight; VMs run their own OS and are heavier.

- **Question:** What is Docker used for?  
  **Answer:** To build, run, and manage containers for consistent environments across development and production.

- **Question:** What is orchestration in DevOps?  
  **Answer:** Managing containerized applications across multiple hosts using tools like Kubernetes or Docker Swarm.

---

## ⚙️ Intermediate Level

- **Question:** What is Infrastructure as Code (IaC)?  
  **Answer:** Managing and provisioning infrastructure through code (e.g., Terraform, Ansible) instead of manual setup.

- **Question:** Why is automation important in DevOps?  
  **Answer:** Reduces human error, speeds up deployments, ensures consistency, and improves reliability.

- **Question:** How would you automate Laravel deployments?  
  **Answer:** Use GitHub Actions or Forge to run composer install, npm build, migrations, and cache clear on push or merge.

- **Question:** What is environment parity?  
  **Answer:** Keeping development, staging, and production environments consistent to prevent “it works on my machine” issues.

- **Question:** What is blue-green deployment?  
  **Answer:** Two environments (blue = live, green = staging); traffic switches to green after successful deployment to avoid downtime.

- **Question:** What’s the purpose of monitoring and logging?  
  **Answer:** Detect issues, measure performance, and provide visibility into system health and user behavior.

- **Question:** What are some tools for server monitoring?  
  **Answer:** Prometheus, Grafana, New Relic, Datadog, Elastic Stack (ELK).

- **Question:** What’s the role of Nginx in a web deployment?  
  **Answer:** Acts as a reverse proxy, load balancer, and static file server.

- **Question:** What’s the difference between a rolling and canary deployment?  
  **Answer:** Rolling replaces instances gradually; canary deploys to a small user group before full rollout.

- **Question:** How would you back up a MySQL database on a production server?  
  **Answer:** Use `mysqldump` via cron job, automate upload to cloud storage (e.g., S3), and verify restore process regularly.

---

## 🧠 Advanced Level

- **Question:** What is Kubernetes and why use it?  
  **Answer:** A container orchestration system that automates deployment, scaling, and management of containerized apps.

- **Question:** Explain how CI/CD pipelines integrate testing and deployment.  
  **Answer:** Each commit triggers builds, tests, linting, and deployments automatically based on pipeline configuration.

- **Question:** How would you secure a CI/CD pipeline?  
  **Answer:** Use secret management, least privilege access, signed commits, code scanning, and verified build artifacts.

- **Question:** How would you design a zero-downtime deployment for a Laravel app?  
  **Answer:** Use blue-green or rolling strategies with atomic symlink swaps, queue draining, and cache pre-warming.

- **Question:** What is a microservices architecture?  
  **Answer:** An approach where an app is divided into independent services that communicate via APIs.

- **Question:** What are the challenges of microservices?  
  **Answer:** Increased complexity, distributed logging, versioning, service discovery, and network reliability.

- **Question:** How would you scale a Laravel application?  
  **Answer:** Horizontal scaling via load balancing, queue workers, caching (Redis), optimizing DB queries, and using CDN.

- **Question:** What’s the difference between stateful and stateless applications?  
  **Answer:** Stateless apps don’t store session data on the server, enabling easy scaling; stateful apps require session persistence.

- **Question:** What is GitOps?  
  **Answer:** Managing infrastructure and deployment pipelines declaratively through Git repositories.

- **Question:** How do you monitor and respond to deployment failures?  
  **Answer:** Set up alerts, automated rollbacks, version tagging, and post-deployment validation tests.

---

## 🧩 Quick Reference Summary

- **Core Concepts:** CI/CD, Infrastructure as Code, Automation, Monitoring, Scaling
- **Key Tools:** Docker, Nginx, GitHub Actions, Terraform, Kubernetes
- **Best Practices:**
  - Automate everything
  - Keep environments consistent
  - Secure pipelines and secrets
  - Monitor performance and errors
  - Enable rollbacks and backups
