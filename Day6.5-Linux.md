Daily DevOps Log — Day 6.5

Date: 2026-03-21
Focus: Processes, signals, nginx recovery & script debugging

✅ Summary

Today I worked on process management and service recovery, focusing on how Linux handles real failures.

🔧 Tasks completed
Process analysis
Used ps aux and top to inspect running processes
Identified nginx structure: master process + worker processes
Signals and service behavior
Tested kill (SIGTERM) vs kill -9 (SIGKILL)
Observed how systemd reports service states:
active → running correctly
inactive → stopped cleanly
failed → unexpected failure
Failure simulation
Simulated real failure using kill -9
Verified service state transitions and system response
Recovered nginx using systemctl
Script improvement (automation)
Enhanced check_nginx.sh:
Detects service state before acting
Implements retry logic (max 3 attempts)
Logs output and displays it using tee
🐛 Debugging session (key part)
Script correctly restarted nginx
However, it continued executing retry attempts even when nginx was already active
Identified that:
The issue is likely related to status validation or script flow
Further debugging is needed to ensure proper exit conditions
🧠 Key learnings
Difference between graceful shutdown and forced termination
Importance of system state interpretation (systemctl)
Real-world automation requires:
proper validation
controlled retries
safe exit conditions
Debugging is a core skill in DevOps, not just writing scripts
📌 Next steps
Debug script logic to correctly stop after successful recovery
Improve status validation and control flow
Continue with advanced process handling and automation
