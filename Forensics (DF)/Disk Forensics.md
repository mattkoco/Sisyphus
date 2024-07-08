# Disk Analysis tools
```
- ★ Autopsy ★
- FTK Imager
- Sleuthkit
```
- Very straightforward category, **all tools listed are used for the same thing**.
- Most of the time will require a second step which will require tools from other categories

# Autopsy Checklist

#Initial Examination

    Basic Information Gathering
    - Note the file system type (NTFS, FAT32, EXT4, etc.).
    - Identify the operating system of the disk image.

    File System Analysis
    - Run a file system analysis to list all files and directories.
    - Check for hidden files and directories.

Keyword Searches

    Identify Relevant Keywords
    - Create a list of keywords related to the CTF challenge (e.g., flag formats, user names, known file names).
    - Run keyword searches on the entire disk image.

    Regular Expression Searches
    - Use regular expressions to find patterns relevant to flags or other critical data.

Timeline Analysis

    Generate Timeline
    - Create a timeline of file system events (file creation, modification, access, deletion).
    - Identify suspicious activities and timeframes.

File Analysis

    Identify Suspicious Files
    - Examine file names, sizes, and extensions for anomalies.
    - Identify encrypted, compressed, or otherwise obfuscated files.

    Extract and Analyze Files
    - Extract suspicious files for further analysis.
    - Use external tools if necessary (e.g., hex editors, malware analysis tools).

Metadata Analysis

    Extract Metadata
    - Review file metadata (creation date, modification date, author, etc.).
    - Look for inconsistencies or useful information.

Application and User Activity

    Browser and Internet Activity
    - Examine browser history, cache, and cookies.
    - Look for internet artifacts related to the CTF challenge.

    User Accounts and Activity
    - Identify user accounts and review user directories.
    - Analyze user activity logs (login times, recently accessed files).

Email and Communication Analysis

    Analyze Email Artifacts
    - Check for email databases (PST, OST files) and analyze them.
    - Look for communication patterns and relevant messages.

Advanced File Recovery

    Recover Deleted Files
    - Use Autopsy's file recovery tools to restore deleted files.
    - Analyze recovered files for relevant information.

Network Artifacts

    Network Analysis
    - Review network-related files and logs.
    - Identify network connections, IP addresses, and potential data exfiltration.

Reporting and Documentation

    Generate Report
    - Use Autopsy’s reporting tools to generate a comprehensive report.
    - Ensure the report includes all relevant evidence and analysis.
