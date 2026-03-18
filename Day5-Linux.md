📘 DevOps Lab — Day 4
✅ Summary / Objectives

Connect via SSH to the VM from Windows host

Edit files remotely using nano or vim

Restart and manage services (systemctl)

Monitor logs in real-time (access.log and error.log)

Practice debugging with intentional configuration errors

🔹 Commands Used
1️⃣ SSH Connection
ssh devuser@<VM_IP>
2️⃣ Edit nginx page
sudo nano /var/www/html/index.nginx-debian.html
# changed content to: <h1>Dani DevOps Lab - Day 4</h1>
3️⃣ Restart nginx
sudo systemctl restart nginx
4️⃣ Real-time logs
# Access log
tail -f /var/log/nginx/access.log

# Error log
tail -f /var/log/nginx/error.log
5️⃣ Intentional errors for practice

Wrong root folder:

root /var/www/noexiste;

Invalid directive:

invalid_directive on;

Test configuration:

sudo nginx -t
🔹 Key Learnings

SSH allows secure remote connection to the VM

Nginx must listen on a port to serve HTTP traffic

Access.log logs all HTTP requests (including 404)

Error.log logs server errors, not 404 pages

Always test configuration with nginx -t before restarting

Debugging is part of the workflow: simulate errors to see real logs

🔹 Mini Challenge Completed

Connected via SSH from Windows

Edited nginx index page remotely

Restarted nginx and verified changes in browser

Observed access.log updating in real-time

Generated intentional errors to populate error.log
