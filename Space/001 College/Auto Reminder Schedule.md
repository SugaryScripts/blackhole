#### Webs
![[whatsapp reminder web wireframe.jpg]]
#### App Script
##### Possibility
Eat medicine # daily # 15.00 # 3
Eat medicine # daily # 15.00 # 5/8/24
Eat medicine # daily # 15.00 # 4/8/24 # 5/8/24
Eat medicine # daily # 15.00 # 4/8/24 # [quantity]

Eat medicine # weekly # 15.00 # 3
Eat medicine # weekly # 15.00 # 5/8/24
Eat medicine # weekly # 15.00 # 4/8/24 # 5/8/24
Eat medicine # weekly # 15.00 # 4/8/24 # [quantity]

##### Further info required
Weekly quantity case:
Now is 9.00 AM. Monday
input = 3.00 AM  --  3 times
Result = Start Tuesday tomorrow, so on until 3 times

##### daily
- time # date_end
- time # date_start # date_end
- time # quantity

##### weekly
- time # date_start # date_end
- time # quantity


##### table
- phone
- description
- interval = weekly | daily
- time
- quantity
- date_start
- date_end
- status = new | progress | successful | error
- message


[Patient Schedule Log - Google Spreadsheet](https://docs.google.com/spreadsheets/d/1-ltsPs2t2zGPD1bJKIOiRLtoDpXD_fZdbielqIIIDNs/edit?usp=sharing)


#### Algorithm
```
split data input

# quantity
quantity = ambigous val
check time -> + 1 if past

# full
Merged start_date + time


# harian
if time past,
date_start + 1



```


#### http request to google app script
[How to send HTTP requests using Google App Script - Automation Help](https://automation-help.com/http-requests-google-app-script/)
[How to Handle GET and POST HTTP Requests in Google Apps Script - Digital Inspiration](https://www.labnol.org/code/19871-get-post-requests-google-script)



App name
komunitas relawan paliatif 'berbagi kasih'


