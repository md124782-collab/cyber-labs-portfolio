# Day 11 - Metasploitable 2: Listening Services

Date: YYYY-MM-DD

## Summary
Enumerated TCP listening services on Metasploitable 2 VM.

## Commands Used
```bash
ss -tuln > /tmp/ss-listen.txt
scp msfadmin@192.168.56.102:/tmp/ss-listen.txt ~/metasploitable-ss-listen.txt
cat ~/metasploitable-ss-listen.txt
Output Highlights
Local Address:Port	Service Guess	Notes
*:22	SSH	Default SSH port
*:80	HTTP	Web server
*:21	FTP	vsftpd
*:3306	MySQL	Database service
*:5432	PostgreSQL	Database service
Observations

SSH, HTTP, FTP, MySQL, and PostgreSQL are active.

Some high ports (e.g., 47971, 43397) may be ephemeral or backdoors (Metasploitable is intentionally vulnerable).

IPv6 addresses (::) indicate some services are listening on IPv6 as well.
