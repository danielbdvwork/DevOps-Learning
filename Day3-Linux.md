# Day 3 — Nginx & Network Diagnostics
17 March 2026

## Progress Today

1. Practiced creating directories and moving files (`mkdir`, `mv`, `chown`).  
2. Checked nginx status and confirmed it was running:
   ```bash
   systemctl status nginx

Investigated listening ports with:

sudo ss -tulnp | grep nginx

Verified connectivity inside the VM using:

curl localhost

Learned to read VM IP with:

ip a

Adjusted nginx configuration to listen on all interfaces (listen 80).

Restarted nginx:

sudo systemctl restart nginx

Checked firewall rules and opened port 80:

sudo ufw allow 80/tcp

Tested access from host browser and confirmed page loads.

Key Learnings

How to check processes and ports with ss or netstat.

How to troubleshoot connectivity issues step by step.

Relationship between service configuration, firewall, and VM network setup.

Logs and access verification (curl / tail -f /var/log/nginx/access.log).

Mini-diagram: Nginx / Network Flow
[Check nginx service] ---> systemctl status nginx
           |
           v
[Check listening ports] ---> sudo ss -tulnp | grep nginx
           |
           v
[Test local connectivity] ---> curl localhost
           |
           v
[Check VM IP] ---> ip a
           |
           v
[Adjust configuration] ---> edit /etc/nginx/sites-available/default (listen 80)
           |
           v
[Restart nginx] ---> sudo systemctl restart nginx
           |
           v
[Firewall check] ---> sudo ufw allow 80/tcp
           |
           v
[Browser test] ---> http://VM_IP
