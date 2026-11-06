# PROGRAM 6: DESIGN AN AUTOMATED BUILD PIPELINE USING DOCKER HUB

## 1. Check Prerequisites

```bash
git --version
docker --version
node --version
npm --version
```

## 2. Create Project Folder

```bash
mkdir program-6
cd program-6
```

## 3. Create package.json

```bash
npm init -y
```

## 4. Create JavaScript File

```bash
nano index.js
```

## 5. Install Dependencies

```bash
npm install
```

## 6. Create Dockerfile

```bash
nano Dockerfile
```

## 7. Build Docker Image

```bash
docker build -t program-6 .
```

## 8. Check Docker Images

```bash
docker images
```

## 9. Run Docker Image

```bash
docker run program-6
```

## 10. Create Docker Hub Repository

1. Open https://hub.docker.com/
2. Login to Docker Hub.
3. Create a repository named `program-6`.
4. Select Public.

## 11. Login to Docker Hub

```bash
docker login -u prathikshakotian
```

Enter your Docker Hub access token when prompted.

## 12. Tag Docker Image

```bash
docker tag program-6 prathikshakotian/program-6:latest
```

## 13. Push Image to Docker Hub

```bash
docker push prathikshakotian/program-6:latest
```

## 14. Generate GitHub Personal Access Token

1. Open GitHub Settings.
2. Select Developer Settings.
3. Select Personal Access Tokens.
4. Select Tokens (classic).
5. Generate a token with the required permissions.
6. Copy and save the token securely.

## 15. Tag Image for GitHub Container Registry

```bash
docker tag program-6 ghcr.io/Prathiksha14k/program-6:latest
```

## 16. Login to GitHub Container Registry

```bash
echo YOUR_GITHUB_PAT | docker login ghcr.io -u Prathiksha14k --password-stdin
```

Replace `YOUR_GITHUB_PAT` with your GitHub token.

## 17. Push Image to GHCR

```bash
docker push ghcr.io/Prathiksha14k/program-6:latest
```

## 18. Initialize Git Repository

```bash
git init
```

## 19. Configure Git Username and Email

```bash
git config --global user.name "Prathiksha14k"
```

```bash
git config --global user.email "YOUR_GITHUB_EMAIL"
```

## 20. Connect GitHub Repository

```bash
git remote add origin https://github.com/Prathiksha14k/program-61.git
```

Verify:

```bash
git remote -v
```

## 21. Add Project Files

```bash
git add .
```

## 22. Commit Files

```bash
git commit -m "Initial commit"
```

## 23. Set Main Branch

```bash
git branch -M main
```

## 24. Push Source Code to GitHub

```bash
git push -u origin main
```

## 25. Verify GitHub

```bash
git status
```

```bash
git log --oneline
```

```bash
git remote -v
```

## 26. Verify Docker

```bash
docker images
```

```bash
docker ps
```

## 27. Verify Application

```bash
docker run -p 3000:3000 program-6
```

Open browser:

```text
http://localhost:3000
```

## Expected Outcome

- Source code uploaded to GitHub.
- Docker image created successfully.
- Docker image pushed to Docker Hub.
- Docker image pushed to GitHub Container Registry.
- GitHub and Docker Hub repositories verified.
