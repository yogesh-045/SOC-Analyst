# SOC Investigation Report

## Incident Title

Windows Process Creation Monitoring using Event ID 4688

## Event Summary

| Field | Value |
| :----- | :---- |
| **Event ID** | `4688` |
| **Event Type** | Process Creation |
| **Host** | DESKTOP-LDBFHIM |
| **Source** | WinEventLog:Security |
| **SIEM** | Splunk Enterprise 10.4 |


## Investigation Steps

### Step 1

Collected Windows Security Logs from Splunk.


### Step 2

Filtered only Event ID 4688.

```spl
index=main EventCode=4688
```

### Step 3

Observed all newly created Windows processes.

Examples:

 lsass.exe

 services.exe

 csrss.exe

 smss.exe

 winlogon.exe

 wininit.exe

 autochk.exe

### Step 4

Verified parent-child process relationships.

Example:

```
Parent Process:
wininit.exe

↓

Child Process:
lsass.exe
```

This indicates a normal Windows boot process.


### Step 5

Generated statistics to identify frequently executed processes.

```spl
index=main EventCode=4688
| stats count by New_Process_Name
```

Result:

SMSS.exe appeared most frequently, followed by CSRSS.exe and LSASS.exe.

### Step 6

Created timeline visualization.

```spl
index=main EventCode=4688
| timechart count
```

Used to observe process creation over time.


### Step 7

Searched for suspicious processes.

Queries executed:

```spl
index=main EventCode=4688 New_Process_Name="*powershell.exe"
```

```spl
index=main EventCode=4688 New_Process_Name="*cmd.exe"
```

No matching events were found because these processes were not executed during the log collection period.


## Findings

Observed only legitimate Windows system processes.

No suspicious PowerShell execution detected.

No CMD abuse detected.

No malicious parent-child relationships identified.

Process creation behavior appeared normal.

## Conclusion

The Windows system generated standard operating system processes during startup. Analysis of Event ID 4688 did not reveal evidence of malicious activity. The investigation demonstrates how Splunk can be used to monitor process creation events, analyze parent-child relationships, and detect suspicious process execution as part of a SOC Analyst workflow.


## Skills Demonstrated

Windows Security Monitoring

 Event ID 4688 Analysis

 Splunk SPL

 Process Investigation

 Dashboard Creation

 SOC Investigation