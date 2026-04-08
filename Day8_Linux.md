## 📓 Daily DevOps Log — Day 8

**Date:** 2026-04-08 
**Focus:** Bash scripting, service automation & control flow  

---

## ✅ Summary

Today I focused on building a Bash script from scratch to monitor and manage a Linux service, understanding each step instead of copying code.

---

## 🔧 Tasks completed

1. **Basic script structure**
   - Created a script using `#!/bin/bash`
   - Stored command output in variables:
     ```bash
     STATUS=$(systemctl is-active nginx)
     ```

2. **Conditional logic**
   - Implemented `if` statements to evaluate service state  
   - Compared values using `[[ ]]`  

3. **Service state handling**
   - Identified different states:
     - `active`
     - `inactive`
     - `failed`  

4. **Automation logic**
   - If `active` → no action  
   - If `inactive` → `start` service  
   - If `failed` → `restart` service  

5. **Verification step**
   - Re-checked service status after action  
   - Confirmed whether recovery was successful  

---

## 🐛 Key learning

- Difference between:
  - controlled stop (`inactive`)
  - forced failure (`failed`, e.g. using `kill -9`)  
- Importance of re-evaluating state after changes  

---

## 🧠 Scripting concepts

- Variable usage (`$VAR`, `$1`)  
- Command substitution `$(...)`  
- Conditional evaluation with `if`, `[ ]`, `[[ ]]`  
- Importance of quoting variables  

---

## 📌 Next steps

- Improve script structure and readability  
- Make the script reusable for any service  
- Add input validation and error handling  
- Continue moving towards automation tools and cloud integration  
