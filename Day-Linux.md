Date: 2026-03-20
Title: Day 6 — Processes, Nginx & Script Automation

✅ Summary

Today I focused on consolidating Day 5 and stepping up to Day 6.

Key activities:

Mini review of Day 5

Checked permissions for /var/www/html

Verified script check_nginx.sh

Ensured nginx could be restarted properly and logs were recorded

Day 6 — Processes in Linux

Observed nginx master and worker processes using ps aux and top

Learned how SIGTERM vs SIGKILL affects process state

Killed nginx with kill -9 and compared with normal kill and systemctl stop

Diagnosed system response: active, inactive, failed

Recovered nginx and verified with curl and port check

Script improvements

Adjusted check_nginx.sh to detect service state before restarting

Implemented tee to output messages both to screen and $LOGFILE

🧠 Takeaways

Understanding process states and signals is critical for system administration

Automating detection + recovery logic in scripts requires observing before acting

Real-world debugging helps convert theory into tangible experience

📌 Next steps

Continue with Day 6.5: integrating processes into script automation

Prepare for upcoming Cloud environment practice
