# DNS-to-SQL-via-Powershell

The intent of this project is to be able to track and search DNS client queries without having to purchase additional software (use stuff you already have in house).   Using Powershell and an SQL backend allows this tracking of queries for domain names back to the clients that made the request, the resolving DNS server, and the DNS response.  There are several helper scripts to deploy, start, and stop the scheduled tasks.  There is a ReadMe.pdf that explains installation, any requirements, and how to query the SQL database.

This project consists of two sub-projects. 

Project #1

Parse the DNS Server debug log file and upload to SQL server.  This allows you to track client queries and the remote DNS Server responses.  The script requires Powershell v3+ to monitor the file via Tail.  If you just want to parse a single file in its entirety, you can use Powershell v2.  The "object output" version of this is release separately as Get-DnsDebugLogLineToObject.ps1  https://web.archive.org/web/20200319004745/https://gallery.technet.microsoft.com/DNS-Debug-Log-File-to-PS-f273c2f2

Project #2

Read the DNS Server cache and upload to SQL server.  This allows tracking of the DNS responses cached in the server's memory and the client IP addresses.  The script requires Powershell v2+.  The "object output" version of this is release separately as Get-DnsServerCacheToObject.ps1   https://web.archive.org/web/20200319004745/https://gallery.technet.microsoft.com/DNS-Server-Cache-to-PS-8f20997f

This is a reposting from my Microsoft Technet Gallery.
