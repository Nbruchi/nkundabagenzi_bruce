# 🚀 DevOps Express App

A simple Express.js web server, containerized with Docker, and exposed via Nginx reverse proxy.

---

## 🛠️ Quick Start

1. **Build & Run Express App**
   ```sh
   docker build -t devops-express-app .
   docker run -d --name express-app -p 3000:3000 devops-express-app
   ```
2. **Run Nginx Proxy**
   ```sh
   docker run --name nginx-proxy -d -p 80:80 -v ${PWD}/nginx.conf:/etc/nginx/nginx.conf:ro nginx
   ```
3. **Test It!**
   ```sh
   curl http://localhost
   # → Hello, DevOps!
   ```

---

## 📁 Files

- `app.js` – Express server
- `package.json` – Node.js dependencies
- `Dockerfile` – Container setup
- `nginx.conf` – Nginx reverse proxy config
