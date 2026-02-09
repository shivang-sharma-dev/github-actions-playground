# 🚀 GitHub Actions CI/CD Playground

This repository demonstrates a **complete CI/CD pipeline using GitHub Actions**, Docker, and **GitHub Container Registry (GHCR)**.

It is designed as a **learning + showcase project** for understanding how real-world CI/CD pipelines are built, tested, and delivered.

---

## 🧠 What This Project Demonstrates

✅ Continuous Integration (CI) using GitHub Actions  
✅ Running automated tests on Pull Requests  
✅ Dependency caching for faster pipelines  
✅ Docker-based CI (tests run inside containers)  
✅ Building Docker images in CI  
✅ Pushing Docker images to GitHub Container Registry (GHCR)  
✅ Secure authentication using GitHub-provided tokens  

---

## 🏗️ CI/CD Workflow Overview

### 🔹 CI (Pull Request)
When a Pull Request is opened:
1. Code is checked out
2. Dependencies are installed (with caching)
3. Tests are executed automatically
4. CI fails if any test fails (blocking merge)

### 🔹 CD (Main Branch)
When code is pushed to `main`:
1. Docker image is built using a `Dockerfile`
2. Image is tagged and pushed to **GHCR**
3. The pushed image is ready for deployment

---

## 🔄 Workflow Triggers

| Event | Action |
|------|-------|
| `pull_request` | Run CI tests |
| `push` to `main` | Build & push Docker image |

---

## 🐳 Docker

The project includes a `Dockerfile` that:
- Uses Node.js as the base image
- Installs dependencies
- Runs tests inside the container

This ensures:
> “It works the same in CI as it would in production.”

---

## 📦 GitHub Container Registry (GHCR)

Docker images are pushed to:


Authentication is handled securely using GitHub’s built-in `GITHUB_TOKEN`.

---

## 🔐 Security Practices

- No secrets are hardcoded
- Uses GitHub Actions permissions
- Uses built-in GitHub tokens for registry authentication

---

## 🧪 Technologies Used

- GitHub Actions
- Docker
- GitHub Container Registry (GHCR)
- Node.js
- YAML
- Linux runners (Ubuntu)

---

## 🎯 Why This Repo Exists

This repository was created to:
- Learn GitHub Actions deeply (not just copy-paste)
- Understand real CI/CD patterns
- Practice DevOps concepts for interviews and real-world use
- Serve as a reference CI/CD template

---

## 📌 How to Use

1. Fork or clone the repository
2. Create a Pull Request to see CI in action
3. Push to `main` to trigger Docker image build & push
4. Check **Packages** tab to see the published image

---

## 📈 Future Improvements

- Add image tagging using commit SHA
- Add versioned releases
- Add deployment stage (CD)
- Add multi-platform Docker builds

---

## 👤 Author

Built by Shivang Sharma
Learning DevOps & CI/CD through hands-on practice 🚀
