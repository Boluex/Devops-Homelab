# 🧪 Home Lab Setup with Docker, Kubernetes, Wireshark, Snort, NGINX, BIND9, and Django

This is a full-featured home lab designed for DevOps, cybersecurity, and backend development learning. It includes containerized services, network security tools, a web stack, and DNS services — ideal for experimentation and simulation of real-world environments.

---

## 📦 Tech Stack Overview

| Component   | Role                                             |
|-------------|--------------------------------------------------|
| Docker      | Containerization of services                    |
| Kubernetes  | Orchestration and management of containers       |
| Wireshark   | Packet analysis and network traffic monitoring   |
| Snort       | Intrusion detection and prevention system (IDS) |
| NGINX       | Web server and reverse proxy                     |
| BIND9       | DNS server for domain resolution                 |
| Django      | Web application backend                          |


---

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/Boluex/Devops-Homelab.git
cd homelab
2. Run Locally with Docker Compose

docker-compose up -d --build
Django accessible at http://localhost:8000

NGINX at http://localhost

DNS requests to BIND9 at 127.0.0.1:53

3. Apply to Kubernetes Cluster

kubectl apply -f k8s/
You can use Minikube, Kind, or any cloud K8s cluster.

4. Monitor with Wireshark
Start Wireshark on your main interface (e.g., eth0, docker0, or cni0) and use filters like:


# DNS
dns

# HTTP traffic
http

# Snort alerts(pcap files by tcpdump)
snort
🧱 Container Details
Django
Custom Django app 

Exposes port 8000.

NGINX
Acts as a reverse proxy to Django.

Can serve static files or forward traffic to Django.

BIND9 DNS
Internal DNS resolver.

Custom zones can be defined to simulate enterprise DNS.

Snort
Passive monitoring of container network.
bash
Copy
Edit
Logs suspicious activity to volume-mounted logs.

Configuration via snort.conf.


Snort IDS will log/report on detections.

Wireshark gives full packet-level visibility.



⚙️ Requirements
Docker & Docker Compose

Kubernetes (Minikube or Kind recommended)

Wireshark installed

Snort image or host installation

Optional: VirtualBox/Vagrant for isolation

📓 Notes
BIND9 needs cap_add and privileged network access to bind to port 53.

Wireshark should be run with sudo or proper permissions for interface access.

Snort rules should be curated to avoid excessive false positives.

🔐 Optional Add-Ons
Feature	Integration
Github actions and workflow
Prometheus + Grafana	Monitor services

🧠 Learning Goals
Understand full-stack deployment and orchestration

Monitor and analyze network traffic

Set up and tune an IDS

Deploy scalable Django applications



---






