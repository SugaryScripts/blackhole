#### File

file_path = absolute | relative
w = write / overwrite
x = write if doesn't exists
a = data will be appended

**TEXT**
```python
employees = ["first", "second"]

import json
# key value or dictionary
employee = { "first": "hello", "second": "There" }

import csv
employee = [["id", "name"], ["1", "First"]]

with open(file_path, "w") as file:
  
  for employee in employees:
    file.write("\n" + employee)

  json.dump(employee, file, indent=2)
  
  writer = csv.writer(file)
    for row in employee:
      writer.writerow(row)
      
  # except FileExistsError
```


#### Error Handling
```python
try:
  int("pizza")
except ZeroDivisionError:
except Exception:
finally:
  # done
```