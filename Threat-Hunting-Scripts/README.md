log_file = "security_log.txt"

with open(log_file, "r") as f:
    logs = f.readlines()

for line in logs:
    if "4625" in line:  # Windows Event ID 4625 = failed login
        print("[ALERT] Failed login detected:", line.strip())
