### **Slide 1: Title Slide**  
**Title:** Secure Web Hosting Using Nginx  
**Subtitle:** A Technology-Driven Approach to Deployment and Security  

---

### **Slide 2: Project Objectives**  
- Explore **Nginx** as a high-performance, lightweight web server.  
- Implement **virtual hosting** to serve multiple websites efficiently.  
- Secure connections using **SSL/TLS** for encrypted communication.  
- Enhance server protection with **UFW** (firewall) and **Fail2ban** (intrusion prevention).  
- Discuss the technologies, their use cases, and integration.  

---

### **Slide 3: Why Nginx for Web Hosting?**  
- **High Performance**:  
  Handles high concurrency with an asynchronous event-driven architecture.  
- **Flexibility**:  
  Supports reverse proxy, load balancing, and static file serving.  
- **Virtual Hosting**:  
  Easily manage multiple websites on a single server.  
- **SSL/TLS Support**:  
  Integrates with tools like Certbot for secure HTTPS connections.  

**Comparison with Alternatives**:  
- **Apache**: More feature-rich but heavier.  
- **LiteSpeed**: High performance but proprietary (Nginx is open-source).  

---

### **Slide 4: SSL/TLS and Certbot**  
- **What is SSL/TLS?**  
  - Protocols to encrypt communication between client and server.  
  - Provides authentication (via certificates) and data integrity.  
- **Why Certbot?**  
  - Automates the generation and renewal of free SSL/TLS certificates from Let’s Encrypt.  
  - Simplifies integration with Nginx for HTTPS.  

**Technological Impact**:  
- Boosts trust and SEO rankings for websites.  
- Enables modern web security standards (e.g., HTTP/2, HSTS).  

---

### **Slide 5: Virtual Hosting with Nginx**  
- **Concept**:  
  Host multiple websites (domains) on a single server using Nginx.  
- **How It Works**:  
  - Nginx routes requests based on the `server_name` directive.  
  - Separate configuration files for each domain.  
- **Use Case**:  
  Ideal for startups or small businesses hosting multiple sites with limited resources.  

**Technological Benefits**:  
- Cost-efficient server utilization.  
- Streamlined management of multiple web services.  

---

### **Slide 6: Firewall Technology: UFW**  
- **What is UFW (Uncomplicated Firewall)?**  
  - Simplified interface for managing `iptables`.  
  - Designed for Linux systems to allow or deny traffic.  
- **Role in the Project**:  
  - Allowed only essential traffic: HTTP (80), HTTPS (443), and SSH (22).  
  - Blocked unauthorized access to improve server security.  

**Advantages**:  
- Reduces attack surface by limiting open ports.  
- Simple configuration makes it accessible to beginners.  

---

### **Slide 7: Intrusion Prevention with Fail2ban**  
- **What is Fail2ban?**  
  - Monitors log files for malicious behavior (e.g., failed login attempts).  
  - Dynamically bans offending IPs for a configurable duration.  
- **Role in the Project**:  
  - Protected Nginx from brute-force attacks using the HTTP 401 error log.  
  - Integrated with UFW for banning IPs at the firewall level.  

**Technological Challenges**:  
- Regex accuracy in identifying attack patterns.  
- Compatibility with existing firewall rules.  

---

### **Slide 8: Challenges and Lessons Learned**  
- **Challenge 1**:  
  **Fail2ban Not Banning IPs**  
  - Root Cause: Incorrect log paths and regex patterns.  
  - Solution: Adjusted configurations and tested with `fail2ban-regex`.  
- **Challenge 2**:  
  **Firewall and Fail2ban Conflicts**  
  - Solution: Aligned Fail2ban's `banaction` with UFW rules.  
- **Challenge 3**:  
  **SSL/TLS Automation Testing**  
  - Solution: Used Certbot’s `--dry-run` option to verify renewal processes.  

---

### **Slide 9: Technology Integration and Demonstration**  
- **Nginx**:  
  - Hosts multiple domains and manages SSL/TLS termination.  
- **Certbot**:  
  - Provides automated, renewable certificates for HTTPS.  
- **UFW**:  
  - Enforces strict access control at the network level.  
- **Fail2ban**:  
  - Monitors access logs and prevents brute-force attacks dynamically.  

**Demonstration**:  
- Show virtual hosting in action with valid HTTPS connections.  
- Simulate failed login attempts and validate Fail2ban bans.  
- Test firewall restrictions for unauthorized traffic.  

---

### **Slide 10: The Future of Secure Web Hosting**  
- **Adopting HTTP/3**:  
  Improve performance with the next-generation protocol.  
- **Further Automation**:  
  Integrate deployment tools like Ansible or Terraform.  
- **Enhanced Monitoring**:  
  Use tools like Prometheus and Grafana for real-time analytics.  

**Conclusion**:  
The integration of Nginx, Certbot, UFW, and Fail2ban showcases how open-source technologies can create a scalable, secure, and cost-effective web hosting solution.  

**Questions and Discussion**  
