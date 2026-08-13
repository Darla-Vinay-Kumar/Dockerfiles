# 🐳 Dockerfiles — Hands-On Dockerfile Examples

A practical collection of **Dockerfile examples** demonstrating the most commonly used Dockerfile instructions.

This repository is created as a hands-on reference for understanding how Docker images are built, configured, and executed.

## 📚 Dockerfile Instructions Covered

| Instruction | Purpose |
|---|---|
| `FROM` | Defines the base image |
| `RUN` | Executes commands while building the image |
| `COPY` | Copies files from the build context |
| `ADD` | Copies files and supports additional features such as remote URLs |
| `CMD` | Defines the default command for a container |
| `ENTRYPOINT` | Defines the primary executable |
| `ENV` | Sets environment variables |
| `ARG` | Defines build-time variables |
| `EXPOSE` | Documents the container's listening port |
| `USER` | Specifies the user used to run the container |
| `WORKDIR` | Sets the working directory |
| `LABEL` | Adds metadata to an image |
| `ONBUILD` | Defines instructions executed by child images |

---

## 📁 Repository Structure

```text
Dockerfiles/
├── ADD/
│   └── Dockerfile
├── ARG/
│   └── Dockerfile
├── CMD/
│   └── Dockerfile
├── COPY/
│   └── Dockerfile
├── ENTRYPOINT/
│   └── Dockerfile
├── ENV/
│   └── Dockerfile
├── EXPOSE/
│   └── Dockerfile
├── FROM/
│   └── Dockerfile
├── LABEL/
│   └── Dockerfile
├── ONBUILD/
│   └── Dockerfile
├── RUN/
│   └── Dockerfile
├── USER/
│   └── Dockerfile
└── WORKDIR/
    └── Dockerfile
```

---

# 🚀 Getting Started

## Prerequisites

Install:

- Docker
- Git

Verify Docker:

```bash
docker --version
```

---

# 🧪 Running an Example

Navigate to any instruction directory.

Example:

```bash
cd CMD
```

Build the image:

```bash
docker build -t dockerfile-cmd .
```

Run the container:

```bash
docker run dockerfile-cmd
```

You can repeat the same process for the other examples.

---

# 🔍 Example

### CMD

Example Dockerfile:

```dockerfile
FROM almalinux:9

CMD ["sleep", "100"]
```

Build:

```bash
docker build -t cmd-example .
```

Run:

```bash
docker run -d --name cmd-container cmd-example
```

Inspect:

```bash
docker ps
```

---

# 🎯 Learning Objectives

This repository demonstrates:

- Dockerfile syntax
- Image creation
- Build-time configuration
- Runtime configuration
- Container commands
- Environment variables
- Build arguments
- Working directories
- Container users
- Image metadata
- Container networking concepts
- Docker image optimization concepts

---

# 🏗️ Docker Image Lifecycle

```text
Dockerfile
    │
    ▼
docker build
    │
    ▼
Docker Image
    │
    ▼
docker run
    │
    ▼
Container
```

---

# 🛡️ Docker Best Practices

When creating production Dockerfiles:

- Use minimal base images where appropriate
- Pin important image versions
- Use `.dockerignore`
- Prefer `COPY` over `ADD` when possible
- Avoid running containers as root
- Use multi-stage builds
- Keep images small
- Don't store secrets in Dockerfiles
- Use environment variables for configuration
- Scan images for vulnerabilities

---

# 📌 Why This Repository?

This repository is part of my hands-on DevOps learning and serves as a reference for Dockerfile instructions used in real-world containerized environments.

---

# 👨‍💻 Author

**Darla Vinay Kumar**

DevOps Engineer | AWS | Terraform | Kubernetes | Docker | CI/CD | DevSecOps

GitHub: [Darla-Vinay-Kumar](https://github.com/Darla-Vinay-Kumar)

---

⭐ If you find this repository useful, consider giving it a star.
