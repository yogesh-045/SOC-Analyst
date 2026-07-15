# What is SPL?
SPL (Search Processing Language) is the language used in Splunk to search, filter, and analyze logs.

Think of it like:

SQL → Databases

SPL → Splunk Logs

 Basic SPL (Search Processing Language)

## 🎯 Objective
Learn how to search and filter logs using Splunk's Search Processing Language (SPL).


## ✅ What I Did

 Opened the **Search & Reporting** app in Splunk.
 Learned the basics of **Search Processing Language (SPL)**.
 Performed searches using the `index` field.
 Filtered logs by **host**.
 Filtered logs by **source**.
 Filtered logs by **sourcetype**.
 Searched for specific keywords in log events.
 Combined multiple search conditions.
 Used wildcard (`*`) searches.
 Performed exact phrase searches using quotation marks.
 Practiced Boolean operators (`AND`, `OR`, `NOT`).
 Explored the search timeline, Events, Statistics, and Visualization tabs.
 Practiced multiple SPL queries on sample log data.

---

## 📚 What I Learned

 **SPL (Search Processing Language)** is used to search, filter, and analyze logs in Splunk.
 `index` specifies where logs are stored.
 `host` identifies the machine that generated the logs.
 `source` identifies the original log file location.
 `sourcetype` tells Splunk how to interpret the log format.
 Keywords help locate relevant log events.
 Wildcards (`*`) can be used to match multiple similar values.
 Quotation marks (`""`) search for an exact phrase.
 `AND` returns events matching all conditions.
 `OR` returns events matching any condition.
 `NOT` excludes matching events from the results.
 The **Timeline** shows when events occurred.
 The **Statistics** tab displays results in a table format.
 The **Visualization** tab converts search results into charts and graphs.


## 💻 SPL Queries Practiced

```spl
index=main
```

```spl
index=main error
```

```spl
index=main failed
```

```spl
index=main host=SERVER01
```

```spl
index=main sourcetype=syslog
```

```spl
index=main source="/var/log/auth.log"
```

```spl
index=main error AND ssh
```

```spl
index=main error OR warning
```

```spl
index=main admin*
```

```spl
"login failed"



