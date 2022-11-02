Kayla Mochizuki
# Lab Report 3
---
## find Commands
**1) find ./[directory name]/[sub directory name]/...**
 - Helps look through directories.

example 1)

input:
```
find ./technical/911report
```
output:
```
./technical/911report
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

This command is finding all files in the sub directory 911report, of the main directory technical. This is useful because this command easily shows me all the files in my sub directory without me having to actually look through techincal myself.

example 2)

input:
```
find ./*/911report
```

output:
```
./technical/911report
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

This command does the same as the command above and finds files in the sub directory 911report. This command is useful because shows that you can use * as a placeholder and that find can sort just by using 911report.

example 3)

input:
```
find ./technical/government/Alcohol_Problems/Session*
```

output:
```
./technical/government/Alcohol_Problems/Session2-PDF.txt
./technical/government/Alcohol_Problems/Session3-PDF.txt
./technical/government/Alcohol_Problems/Session4-PDF.txt
```

This command is finding all files in the sub-sub directory Alcohol_Problems that conatins Session. This is a useful command because it shows that I can go through multiple directories at once, as I went through technical to get to government and went through government to get to Alcohol_Problems.

---
**2) find ./[directory name] -type f -size [size amount]**
  - Sorts by files sizes.

example 1)

input:
```
find ./technical  -type f -size -1000c
```

output:
```
./technical/plos/pmed.0020191.txt
./technical/plos/pmed.0020226.txt
```
This command is finding all files in technical that are smaller than 1000 bytes. This is useful if you are looking for small files in a directory.

example 2)

input:
```
find ./technical  -type f -size +100000c
```

output:
```
./technical/government/About_LSC/commission_report.txt
./technical/government/About_LSC/State_Planning_Report.txt
./technical/government/Env_Prot_Agen/multi102902.txt
./technical/government/Env_Prot_Agen/ctm4-10.txt
./technical/government/Env_Prot_Agen/bill.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Gen_Account_Office/d0269g.txt
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
./technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
./technical/government/Gen_Account_Office/d01376g.txt
./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
./technical/government/Gen_Account_Office/pe1019.txt
./technical/government/Gen_Account_Office/gg96118.txt
./technical/government/Gen_Account_Office/d01591sp.txt
./technical/government/Gen_Account_Office/im814.txt
./technical/government/Gen_Account_Office/ai9868.txt
./technical/government/Gen_Account_Office/May1998_ai98068.txt
./technical/government/Gen_Account_Office/d02701.txt
./technical/biomed/1471-2105-3-2.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-12.txt
```

This command gives all files in technical that are greater than 100000 bytes. This is useful because it shows that you can also sort by if a file size in greater and not just by smaller sizes.

example 3)

input:
```
find ./technical/911report  -type f -size -1M
```

output:
```
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

This command gives the files in the sub directory 911report, that are less than 1 Mb. This command is useful because it displays that you can not only look through subdirectories but also use different sizes like Mb.

---
**3) find ./[directory name] -iname [file name]**
  - Case insensitive search.

example 1)

input:
```
find ./technical -iname chaptEr*
```

output:
```
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-9.txt
./technical/911report/chapter-8.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
```

This command shows all files that match the name chapter through a case insensitive search. This is useful because it shows that if you are looking for files but make a mistake with caps, it won't affect your search.

example 2)

input:
```
find ./technical -iname report*
```

output:
```
./technical/government/About_LSC/reporting_system.txt
./technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
```

This command shows files that match the word report even though one of the files has the R capitilized while the other does not. This is useful because it displays that if you are trying to search for multiple files containing a certain word but you didn't write them in the same format, you can still easily get all files.

example 3)

input:
```
find ./technical/government -iname report*
```

output:
```
./technical/government/About_LSC/reporting_system.txt
./technical/government/Post_Rate_Comm/ReportToCongress2002WEB.txt
```

This command gives me the same files as the previous one but specifiys that it's looking in the sub directory, government. Say if I want all files with the word report but I didn't format them all the same and don't know if there are report files in other directories, I can narrow my search.

