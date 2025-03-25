## This diagram shows the key components of the application:
1. Frontend (NGINX): Two web servers handle the frontend requests.
2. Backend (Node.js API): Two API servers to process requests.
3. PostgreSQL Database: A central database server for storing patient data.
4. Redis: Caching layer for better performance.
5. HAProxy: Load balancer to distribute traffic across NGINX web servers and Node.js API servers.
6. Backup System: A local Linux-based backup system to back up the system’s data.

<img width="512" alt="image" src="https://github.com/user-attachments/assets/ddd9056d-1314-4719-a7f8-f71dd1ad8f31" />

## <ins>1. Discovery and Tooling Setup</ins>

**Tools:**  Use Azure Migrate (appliance for agentless discovery and assessment).
Azure Migrate is a comprehensive toolset that helps discover, assess, and migrate on-premises workloads to Azure.

### Types of Data to Collect
- **Operating System Information:** Version of Ubuntu Linux running on the servers (to ensure compatibility with Azure services).\
- **Software Inventory:** Information about installed software packages, including NGINX, Node.js, PostgreSQL, Redis, and HAProxy.\
- **Dependencies:** Identify interdependencies between the web servers (frontend), API servers (backend), database (PostgreSQL), and cache (Redis).\
- **Server Performance Metrics:** CPU, memory, storage, and network utilization for each of the components to determine the sizing requirements for Azure.\
- **Backup and Restore Data:** Current backup schedules and configurations to ensure compliance with Tailwind OpenCare’s backup and recovery requirements.


**Data to collect:**  OS, software inventory, performance metrics, dependencies, backup schedules.

**Credentials and Permissions:**  Managed using Azure Active Directory and Azure Key Vault for secure storage.

