# simple-intruder-list

## sql injection

### union-based

to count the columns and find which columns accept type string (up to 30): 
- run payloads from union-based-count-cols.txt

*note: if only the payloads with `FROM DUAL` pass, then you already know that oracle database is used*

### detect database

for blind sqli, add these to the payload:
- prefix: ' and CAST(
- suffix:  AS varchar)='true

for union-based sqli, add these to the payload:
- prefix: CAST(
- suffix:  AS varchar)

*note: there is a space before `AS`*
