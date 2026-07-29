# Splunk Queries – Event ID 4688

## 1. View All Process Creation Events

```spl
index=main EventCode=4688
```

## 2. Display Important Fields

```spl
index=main EventCode=4688
| table _time New_Process_Name Creator_Process_Name host
```

## 3. Total Process Count

```spl
index=main EventCode=4688
| stats count
```

## 4. Top Executed Processes

```spl
index=main EventCode=4688
| stats count by New_Process_Name
| sort -count
```

## 5. Top Parent Processes

```spl
index=main EventCode=4688
| stats count by Creator_Process_Name
| sort -count
```

## 6. Process Timeline

```spl
index=main EventCode=4688
| timechart count
```

## 7. Search PowerShell

```spl
index=main EventCode=4688
New_Process_Name="*powershell.exe"
```

## 8. Search CMD

```spl
index=main EventCode=4688
New_Process_Name="*cmd.exe"
```

## 9. Search Registry Process

```spl
index=main EventCode=4688
New_Process_Name="*reg*"
```

## 10. Display Process with Parent

```spl
index=main EventCode=4688
| table _time Creator_Process_Name New_Process_Name host
```