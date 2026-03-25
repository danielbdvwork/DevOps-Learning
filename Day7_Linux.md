## 📓 Daily DevOps Log — Day 7

**Date:** 2026-03-22  
**Focus:** Service management, systemd, logs & debugging  

---

## ✅ Summary

Today I focused on understanding Linux service management using systemd, expanding from nginx-specific work to a more general system-level approach.

---

## 🔧 Tasks completed

1. Service management basics  
   - Used `systemctl` to manage services (`start`, `stop`, `restart`, `reload`)  
   - Listed services with:  
     `systemctl list-units --type=service`  

2. Service lifecycle testing  
   - Stopped and started services (ssh, nginx)  
   - Observed states: `active`, `inactive`, `failed`  

3. Logs and diagnostics  
   - Used `journalctl -u <service>`  
   - Followed logs in real time:  
     `journalctl -u nginx -f`  

4. Restart vs Reload (key concept)  
   - `restart`: stops and starts the service (new PID)  
   - `reload`: reloads config without stopping (same PID)  

5. Process inspection  
   - Used `ps aux` to inspect nginx processes  
   - Verified PID behavior between restart and reload  

---

## 🐛 Debugging

- Debugged nginx monitoring script  
- Fixed issues with variable updates and condition checks  
- Achieved correct behavior:  
  - detects service state  
  - exits loop when nginx is active  

---

## 🧠 Key learnings

- systemd is key for service management  
- `journalctl` is essential for diagnostics  
- Understanding PID explains service behavior  
- `reload` vs `restart` is critical in production  
- Debugging requires validating real execution flow  

---

## 📌 Next steps

- Improve automation scripts  
- Combine practice with structured courses  
- Prepare transition to cloud fundamentals  
