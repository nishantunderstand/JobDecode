Docker
│
├── 🔹 Why Docker? (Problem Statement)
│     ├── Before → Virtual Machines (VMware)
│     ├── Issues:
│     │     ├── Heavy (Full OS per app)
│     │     ├── Slow startup
│     │     ├── Resource waste
│     │     └── Environment mismatch
│     └── Solution:
│           └── Lightweight containers (shared kernel)
│
├── 🔹 Core Concepts
│     ├── Image
│     │     └── Blueprint (App + Dependencies)
│     │
│     ├── Container
│     │     └── Running instance of Image
│     │
│     ├── Docker Engine
│     │     └── Runtime that runs containers
│     │
│     ├── Kernel
│     │     └── Shared OS core (Linux-based)
│     │
│     └── Registry
│           └── Stores images (Docker Hub)
│
├── 🔹 Docker vs Virtual Machine
│     ├── VM → Full OS ❌
│     └── Docker → Shared OS ✔️
│
├── 🔹 Dockerfile (How to build image)
│     ├── FROM → Base Image
│     ├── WORKDIR → Working directory
│     ├── COPY → Copy files
│     ├── RUN → Execute during build
│     ├── EXPOSE → Port info
│     └── ENTRYPOINT/CMD → Run app
│
├── 🔹 Base Image
│     ├── Java → OpenJDK / Eclipse Temurin
│     ├── Node → Node image
│     └── Can be anything (depends on app)
│
├── 🔹 Lifecycle
│     ├── Code → JAR
│     ├── JAR → Docker Image
│     ├── Image → Container
│     └── Container → Running App
│
├── 🔹 Spring Boot + Docker
│     ├── Build JAR (mvn clean package)
│     ├── Create Dockerfile
│     ├── Build Image
│     └── Run Container
│
├── 🔹 Key Advantages
│     ├── Fast startup
│     ├── Lightweight
│     ├── Portable
│     └── Consistent environments
│
├── 🔹 Docker vs Kubernetes
│     ├── Docker → Runs container
│     └── Kubernetes → Manages containers at scale
│
└── 🔹 Real-world Use
      ├── Microservices
      ├── CI/CD pipelines
      └── Cloud deployment