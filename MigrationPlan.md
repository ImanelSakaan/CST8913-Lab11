## This diagram shows the key components of the application:
1. Frontend (NGINX): Two web servers handle the frontend requests.
2. Backend (Node.js API): Two API servers to process requests.
3. PostgreSQL Database: A central database server for storing patient data.
4. Redis: Caching layer for better performance.
5. HAProxy: Load balancer to distribute traffic across NGINX web servers and Node.js API servers.
6. Backup System: A local Linux-based backup system to back up the system’s data.

<img width="512" alt="image" src="https://github.com/user-attachments/assets/ddd9056d-1314-4719-a7f8-f71dd1ad8f31" />

## <ins>1. Discovery and Tooling Setup</ins>
### Tools for Discovery
- **Azure Migrate Appliance:** The Azure Migrate appliance will be deployed on the on-premises servers to collect data about the infrastructure, including server performance, configurations, and dependencies. It will help gather the information needed for a detailed assessment.
- **Agentless Discovery:** For environments where deploying an agent may be difficult, the agentless approach will be used to scan the servers and gather essential data.
- **Azure Migrate:** Server Assessment: This tool will provide insights into the on-premises workloads and suggest the optimal sizing, cost estimation, and performance metrics for Azure-based resources.

### Types of Data to Collect
- **Operating System Information:** Version of Ubuntu Linux running on the servers (to ensure compatibility with Azure services).
- **Software Inventory:** Information about installed software packages, including NGINX, Node.js, PostgreSQL, Redis, and HAProxy.
- **Dependencies:** Identify interdependencies between the web servers (frontend), API servers (backend), database (PostgreSQL), and cache (Redis).
- **Server Performance Metrics:** CPU, memory, storage, and network utilization for each of the components to determine the sizing requirements for Azure.
- **Backup and Restore Data:** Current backup schedules and configurations to ensure compliance with Tailwind OpenCare’s backup and recovery requirements.

### Credentials and Permissions Management
- **Azure Active Directory (AAD):** All migration tools and processes will authenticate through Azure Active Directory to ensure secure access management.
- **Role-Based Access Control (RBAC):** Azure RBAC will be configured to ensure that only authorized users and groups have the necessary permissions to perform discovery, assessment, and migration tasks.
- **Credential Storage:** Credentials, such as API keys and database connection details, will be securely stored in Azure Key Vault, ensuring that sensitive information is protected during the migration process.

 

