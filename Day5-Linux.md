
echo "## 📓 Daily DevOps Log — Day 5

**Date:** 2026-03-19  
**Focus:** Permissions, nginx, automation script  

**Tasks completed:**

1. **User and permissions practice**
   - Created test user \`devtest\` and added to \`sudo\` group.
   - Explored ownership and permissions with \`chown\` and \`chmod\`.
   - Identified why nginx could not serve files when \`www-data\` lacked access.

2. **Debugging nginx**
   - Observed \`curl\` vs browser behavior; understood that timeouts were due to incorrect folder permissions.
   - Fixed ownership and permissions of \`/var/www/html\` and parent folders (\`chown -R www-data:www-data\`, \`chmod -R 755\`).

3. **Automation script**
   - Created \`check_nginx.sh\` to:
     - Verify if nginx is running.
     - Restart nginx automatically if down.
     - Log all actions to \`~/nginx_check.log\`.
   - Explained script step by step: shebang, variables, command substitution \`$()\`, \`if\` with command vs \`if [ ]\` for conditionals.
   - Tested script by stopping nginx manually and verifying auto-restart and log entries.

4. **Advanced concepts**
   - Discussed importance of using \`$HOME\` for consistent log path.
   - Capturing command output with \`$(...)\`.
   - Conditional checks in bash (\`[ ]\`) vs executing commands directly.

**Key learnings:**

- How to debug service failures caused by permissions.
- Difference between local test (\`curl\`) and external access (browser, VM networking).
- Basics of automation and monitoring via bash scripts.
- Understanding ownership and file permissions is critical for DevOps tasks.

**Next steps:**

- Focus on processes and system monitoring tomorrow (Day 6).
- Learn to simulate service failures and recover them automatically.
- Expand automation scripts to detect errors in logs and respond.
" > day5_log.md
