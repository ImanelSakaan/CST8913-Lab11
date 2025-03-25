## This diagram shows the key components of the application:
1. Frontend (NGINX): Two web servers handle the frontend requests.
2. Backend (Node.js API): Two API servers to process requests.
3. PostgreSQL Database: A central database server for storing patient data.
4. Redis: Caching layer for better performance.
5. HAProxy: Load balancer to distribute traffic across NGINX web servers and Node.js API servers.
6. Backup System: A local Linux-based backup system to back up the system’s data.

![image](https://github.com/user-attachments/assets/a0f59694-c5b0-4116-8a16-21a9e61c7f6d)


## 1. Discovery and Tooling Setup

**Tools:**  Use Azure Migrate (appliance for agentless discovery and assessment).

**Data to collect:**  OS, software inventory, performance metrics, dependencies, backup schedules.

**Credentials and Permissions:**  Managed using Azure Active Directory and Azure Key Vault for secure storage.

