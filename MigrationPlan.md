## This diagram shows the key components of the application:
1. Frontend (NGINX): Two web servers handle the frontend requests.
2. Backend (Node.js API): Two API servers to process requests.
3. PostgreSQL Database: A central database server for storing patient data.
4. Redis: Caching layer for better performance.
5. HAProxy: Load balancer to distribute traffic across NGINX web servers and Node.js API servers.
6. Backup System: A local Linux-based backup system to back up the system’s data.

<img width="512" alt="image" src="https://github.com/user-attachments/assets/ddd9056d-1314-4719-a7f8-f71dd1ad8f31" />




## 1. Discovery and Tooling Setup

**Tools:**  Use Azure Migrate (appliance for agentless discovery and assessment).

**Data to collect:**  OS, software inventory, performance metrics, dependencies, backup schedules.

**Credentials and Permissions:**  Managed using Azure Active Directory and Azure Key Vault for secure storage.

