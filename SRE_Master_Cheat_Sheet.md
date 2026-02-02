# 🚀 SRE & App Ops Ultimate Master Grid (4x4 Ultra-Wide)

**Optimization:** 1920x1080 Screens | **Role:** SRE / L2 / App Ops | **Focus:** Linux, SQL, Java, K8s, AWS

---

## 🏗️ Row 1: Systems, Network & Database Deep-Dive

| **1. LINUX ADMIN, PERMISSIONS & COMMANDS** | **2. NETWORK & PORT TROUBLESHOOTING** | **3. SQL DEEP-DIVE: JOINS & READS** | **4. SQL DEEP-DIVE: DDL, DML & PERF** |
| :--- | :--- | :--- | :--- |
| **`w`**<br>_Show who is logged in, uptime, & system load avg._ | **`ss -tuln`**<br>_Fast view of listening TCP/UDP ports._ | **15th User Query:**<br>`SELECT * FROM users ORDER BY id LIMIT 1 OFFSET 14;`<br>_(Offset 14 skips first 14 rows)._ | **`DROP TABLE old_logs;`**<br>_DDL: Deletes table structure permanently._ |
| **`uname -a`**<br>_Print Kernel version, Architecture & System info._ | **`netstat -tulpn`**<br>_Checks ports + Process IDs (PID) owning them._ | **Union (No Dupes):**<br>`SELECT * FROM t1 UNION SELECT * FROM t2;`<br>_(Combines rows; REMOVES duplicates)._ | **`DELETE FROM users WHERE id=15;`**<br>_DML: Removes specific data row (User 15)._ |
| **`hostnamectl`**<br>_Query/Change Hostname, OS Release & Virt info._ | **`lsof -i :8080`**<br>_"List Open Files" - finds exactly who locked port._ | **Union All (Keep Dupes):**<br>`SELECT * FROM t1 UNION ALL SELECT * FROM t2;`<br>_(Combines rows; KEEPS all duplicates)._ | **`ALTER TABLE users ADD COLUMN phone TEXT;`**<br>_DDL: Modifies schema to add a new field._ |
| **`systemctl status <svc>`**<br>_Check if Tomcat/DB is active. Restart fixes hung app._ | **`telnet <IP> <Port>`**<br>_Test if a remote server port is open/reachable._ | **INNER JOIN:**<br>`SELECT * FROM users u JOIN orders o ON u.id=o.uid;`<br>_(Matches records present in BOTH tables)._ | **`TRUNCATE TABLE temp_data;`**<br>_DDL: Empties table but keeps structure (Fast)._ |
| **`journalctl -u <svc> -xe`**<br>_Deep dive into system logs/boot errors for service._ | **`nc -zv <IP> <Port>`**<br>_Netcat stealth port scan (faster than telnet)._ | **LEFT JOIN:**<br>`SELECT * FROM users u LEFT JOIN orders o ON u.id=o.uid;`<br>_(Finds ORPHANS: Users without Orders)._ | **`EXPLAIN ANALYZE SELECT ... ;`**<br>_Debugs slow queries by showing execution cost._ |
| **`chmod 755 <file>`**<br>_rwxr-xr-x. Owner=Full, Group/Others=Read+Exec._ | **`curl -Iv <URL>`**<br>_Fetches Headers (-I) & Verbose (-v) for status._ | **RIGHT JOIN:**<br>_Keeps all Right table rows (Rarely used)._ | **`SELECT pid, state, query FROM pg_stat_activity;`**<br>_Finds stuck/long-running queries in DB._ |
| **`chown -R user:group <dir>`**<br>_Recursively fixes "Permission Denied" errors._ | **`traceroute <IP>`**<br>_Shows every network hop/router to destination._ | **FULL OUTER JOIN:**<br>`SELECT * FROM t1 FULL OUTER JOIN t2 ON t1.id=t2.id`<br>_(Keep EVERYTHING: Match + No Match)._ | **`VACUUM (VERBOSE, ANALYZE);`**<br>_Reclaims storage and updates DB stats._ |
| **`find /path -mtime +7 -delete`**<br>_Automation to delete logs older than 7 days._ | **`nslookup <domain>`**<br>_Debugs DNS resolution issues (IP vs Name)._ | **EXISTS / SUBQUERIES:**<br>`SELECT * FROM u WHERE EXISTS (SELECT 1...);`<br>_(Fast filter "at least one related row")._ | **UPSERT (Insert or Update):**<br>`INSERT INTO ... ON CONFLICT (id) DO UPDATE ...` |
| **`grep -r "ERROR" /var/log`**<br>_Recursive search for error text in all files._ | **`ip route show`**<br>_Shows the routing table (Gateway/Interface)._ | **Primary Key vs Unique:**<br>_PK = Unique + Not Null. Unique = Allows 1 Null._ | **LOCKS CHECK:**<br>`SELECT pid, mode FROM pg_locks...`<br>_(Identifies queries blocking others)._ |

---

## ☕ Row 2: Application, Cloud & Kubernetes

| **1. JAVA, OOPS & SPRING FRAMEWORK** | **2. KUBERNETES (K8S) COMPONENTS** | **3. AWS CLOUD INFRASTRUCTURE** | **4. CLOUDWATCH, LOGGING & MONITORING** |
| :--- | :--- | :--- | :--- |
| **Class vs Object**<br>_Class is Blueprint. Object is the specific Instance._ | **`kubectl get pods -n <ns>`**<br>_Lists Pod status (Running/Error) & Restart counts._ | **EC2 / S3 / IAM / VPC**<br>_Compute, Storage, Identity, and Network layers._ | **CloudWatch Metrics**<br>_CPU, Memory, Disk I/O, ELB Latency, 5xx Count._ |
| **int vs Integer**<br>_Primitive (fast, no null) vs Wrapper (Object)._ | **`kubectl describe pod <name>`**<br>_Critical for debugging "Pending/CrashLoop" events._ | **IAM Role**<br>_Safe permissions for machines (EC2/EKS/Lambda)._ | **Splunk / Nieman**<br>_Log Aggregation. Search for "Exception" or "Error"._ |
| **Inheritance / Polymorphism**<br>_Reusing Parent code / Method Overloading._ | **`kubectl logs -f <pod>`**<br>_Streams live application logs (Stack Traces)._ | **Security Group (SG)**<br>_Stateful Firewall (Instance level). Allow In=Out._ | **Postman / Curl**<br>_Trace API calls to reproduce 400/500 errors._ |
| **IOC / Dependency Injection**<br>_Spring manages object lifecycle & injects deps._ | **`kubectl top nodes`**<br>_Checks CPU/Memory saturation on nodes._ | **NACL (Network ACL)**<br>_Stateless Firewall (Subnet level). Explicit rules._ | **Distributed Tracing**<br>_Tracking a Request-ID across Microservices._ |
| **@RestController / @Service**<br>_API Layer (JSON) -> Business Logic Layer._ | **Deployment / StatefulSet**<br>_Manages stateless apps vs stateful DB apps._ | **ALB / Target Group**<br>_ALB routes traffic; TG performs Health Checks._ | **"Monarch" / Azure One**<br>_Specific tools mentioned in JD. Know their purpose._ |
| **Maven (`pom.xml`)**<br>_Manages dependencies (jars) and build process._ | **Service / Ingress**<br>_Service = Internal LB; Ingress = External Route._ | **VPC Endpoint**<br>_Private tunnel to S3 (No Internet Gateway needed)._ | **Alerts & Alarms**<br>_Set on thresholds (e.g., CPU > 80% for 5 mins)._ |
| **Hibernate / JPA**<br>_ORM. Maps Java Objects directly to SQL Tables._ | **ConfigMap / Secret**<br>_Decouples config files & passwords from code._ | **Route 53**<br>_AWS Managed DNS (Domain Name Service)._ | **Dashboards**<br>_Visualizing RED metrics (Rate, Errors, Duration)._ |

---

## 🛠️ Row 3: Flows, Automation & Process

| **1. SPRING MVC REQUEST FLOW** | **2. BASH AUTOMATION: LOG ROTATION** | **3. TROUBLESHOOTING STEPS (L2/SRE)** | **4. INCIDENT MANAGEMENT & TERMS** |
| :--- | :--- | :--- | :--- |
| **1. Request hits DispatcherServlet**<br>_The "Front Controller" receiving all HTTP calls._ | **Header:** `#!/bin/bash`<br>**Vars:** `LOG_DIR="/opt/tomcat/logs"`<br>`ARCHIVE="/opt/tomcat/archive"` | **1. Check Monitoring**<br>_Action: Check Splunk/CloudWatch for error spikes._ | **SLA (Service Level Agreement)**<br>_The Deadline (e.g., "99.9% Uptime")._ |
| **2. Maps URL to @Controller**<br>_Finds the right Java method for "/api/users"._ | **Date:** `DATE=$(date +%Y%m%d)` | **2. Trace API**<br>_Action: Use Postman/Curl to reproduce errors._ | **MTTR (Mean Time To Recovery)**<br>_Speed of fix. The #1 metric for SREs._ |
| **3. Calls @Service**<br>_Service layer executes Business Logic._ | **Compress:**<br>`tar -czf $ARCHIVE/logs_$DATE.tgz $LOG_DIR/*.log` | **3. Check Service Health**<br>_Action: `systemctl status tomcat` (Is it active?)._ | **RCA (Root Cause Analysis)**<br>_The "Why" it happened & prevention plan._ |
| **4. Calls @Repository**<br>_Repository uses Hibernate to query Database._ | **Clear:**<br>`find $LOG_DIR -name "*.log" -exec truncate -s 0 {} +` | **4. Check Resources**<br>_Action: `top` (CPU/RAM) & `df -h` (Disk Full)._ | **SME (Subject Matter Expert)**<br>_The person who owns the App/Code logic._ |
| **5. Returns Data (Model)**<br>_SQL results converted back to Java Objects._ | **Cleanup:**<br>`find $ARCHIVE -mtime +7 -delete` | **5. DB & Java Deep-Dive**<br>_Action: Check SQL Joins & `jstack` (Threads)._ | **Bridge Call**<br>_Live Zoom/Teams call to triage P1 incidents._ |
| **6. Returns JSON (200 OK)**<br>_Data sent back to User/UI._ | **Schedule:** `crontab -e`<br>`0 0 * * * /path/script.sh` | **6. RCA (Root Cause Analysis)**<br>_Action: Document "Why" and "Fix" in Jira._ | **Handover**<br>_Transferring active tickets from India to US._ |

---

## 🚦 Row 4: Status Codes, Deployments & Interview Q&A

| **1. REST API STATUS CODES** | **2. TOMCAT & DEPLOYMENT OPS** | **3. INTERVIEW Q&A: TECH (HARI/KRISHNA)** | **4. INTERVIEW Q&A: PROCESS (SANJANA)** |
| :--- | :--- | :--- | :--- |
| **200 OK / 201 Created**<br>_Action: None. Request successful._ | **`bin/startup.sh` / `shutdown.sh`**<br>_Action: Manual Start/Stop scripts for Tomcat._ | **Q: "Troubleshoot K8s layers?"**<br>A: 1. Pod Logs (`kubectl logs`)<br>2. Events (`kubectl describe`)<br>3. Node Health (`kubectl top nodes`)<br>4. Network (ALB Health). | **Q: "Automation Example?"**<br>A: "I noticed manual log clearing caused disk alerts. I wrote a Bash script using `tar` and `truncate` to automate rotation via Crontab." |
| **400 Bad Request**<br>_Action: Client-side error. Check JSON payload._ | **`catalina.out`**<br>_Action: The MAIN log file. Look here for Stacks._ | **Q: "User 15 SQL Query?"**<br>A: "I use a LEFT JOIN to find missing data."<br>`SELECT u.name, o.id FROM users u`<br>`LEFT JOIN orders o ON u.id=o.uid`<br>`WHERE u.id=15;` | **Q: "Handle P1 Incident?"**<br>A: 1. Acknowledge & Check SLA.<br>2. Open Bridge Call.<br>3. Focus on Mitigation (Restart) first.<br>4. Communicate every 30m.<br>5. RCA after service up. |
| **401 Unauth / 403 Forbidden**<br>_Action: Check Token expiry or IAM Permissions._ | **`work/` & `temp/`**<br>_Action: Delete folders to fix "Ghost" cache bugs._ | **Q: "500 vs 504?"**<br>A: "500 is Internal Error (App crashed/Code bug). 504 is Gateway Timeout (App waiting for DB/API)." | **Q: "Why SRE?"**<br>A: "I have mastered L1 monitoring. I want to move to L2/SRE to fix the root cause using my skills in Linux, SQL, and Automation." |
| **404 Not Found**<br>_Action: Check URL path or if WAR file is deployed._ | **`setenv.sh`**<br>_Action: Configure JVM Heap Memory (-Xmx / -Xms)._ | **Q: "Fix Unhealthy Target?"**<br>A: 1. Check Security Group (Port 8080).<br>2. Check App Process.<br>3. Check Health Path (`/health`). | **Q: "Shift Handover?"**<br>A: "I summarize all Open Tickets, pending P1/P2 incidents, and ongoing changes to the US team." |
| **500 Internal Error**<br>_Action: Java Crash. Check Logs for Exceptions._ | **`server.xml`**<br>_Action: Configures Ports (8080) and Connectors._ | | |
| **503 Unavail / 504 Timeout**<br>_Action: DB slow, Downstream dead, or LB timeout._ | **`systemctl restart tomcat`**<br>_Action: The standard way to restart the app._ | | |