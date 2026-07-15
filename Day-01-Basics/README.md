#  What is Splunk?
Splunk is a SIEM and log management platform used to collect, search, analyze, monitor, and visualize machine-generated data (logs) from different systems.

# What is a SIEM?
SIEM stands for Security Information and Event Management.

It collects logs from different devices, detects threats, correlates events, and helps security analysts investigate incidents.

# What is an Index?
An Index is a storage location where Splunk saves and organizes logs.

# Example:
windows

linux

firewall

antivirus

Think of it as a database for logs.

# What is a Host?
A Host is the machine or device that generated the log.

# Examples:
Windows PC

Linux Server

Firewall

Router

# Example:

Host = SERVER01
#  What is a Source?

A Source tells Splunk where the data came from.

# Example:

C:\Windows\System32\winevt\Logs\Security.evtx

or

/var/log/auth.log
#  What is a Sourcetype?
A Sourcetype tells Splunk what type of data it is so Splunk knows how to parse it.

# Examples:
WinEventLog

syslog

apache

nginx

csv
#  What is a Forwarder?
A Forwarder is a lightweight Splunk agent installed on a machine that collects logs and sends them to the Splunk Indexer.

# Example:

Windows PC
      ↓
Universal Forwarder
      ↓
Indexer
#  What is an Indexer?
The Indexer receives logs from forwarders, indexes them, stores them, and makes them searchable.

Think of it as the storage and processing engine.

# What is a Search Head?
The Search Head is where users search data, run queries, create dashboards, and investigate logs.

It sends search requests to Indexers and displays the results.

# What is the Search Bar used for?
The Search Bar is used to write SPL (Search Processing Language) queries to search and analyze logs.

# Example:

index=main
# What is the Time Picker used for?
The Time Picker filters logs based on time.

# Examples:
Last 15 minutes

Last 24 hours

Last 7 days

Custom time range
# What are Events?
An Event is a single log entry stored in Splunk.

# Example:
User John logged in successfully.

Each log line is one event.

# What is the Statistics Tab?
The Statistics tab displays search results in a table format.

It is useful for:
Counts

Grouping

Filtering

Aggregations

# Example:

|User |	Count |
|_____|________|
|John |	 15    |
|Admin|	30     |

#  What is the Visualization Tab?
The Visualization tab converts search results into charts and graphs.

# Examples:
Bar Chart

Pie Chart

Line Chart

Area Chart

Single Value

Maps

It helps create dashboards for easier analysis.

## 📘 Splunk 

| Concept | Definition |
|---------|------------|
| **Splunk** | Log management & SIEM platform |
| **SIEM** | Security Information and Event Management |
| **Index** | Stores logs |
| **Host** | Machine generating logs |
| **Source** | Original location of the log file |
| **Sourcetype** | Type or format of the log data |
| **Forwarder** | Sends logs from endpoints to Splunk |
| **Indexer** | Receives, stores, and indexes logs |
| **Search Head** | Runs searches and displays results |
| **Search Bar** | Used to write SPL (Search Processing Language) queries |
| **Time Picker** | Filters logs based on a selected time range |
| **Event** | A single log entry in Splunk |
| **Statistics** | Displays search results in table format |
| **Visualization** | Converts search results into charts and dashboards |