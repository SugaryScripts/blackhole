up:: [[Python]]

#### Stars Print Loop
```python
# Number of rows in the pattern
rows = 3

# Loop through each row
for i in range(rows):
    # Print leading spaces
    for j in range(i):
        print(" ", end="")
    # Print stars
    for k in range(rows - i):
        print("*", end="")
    # Move to the next line after each row is printed
    print()
    
#####
 ###
  #
```

```python
# Number of rows in the pattern
rows = 4

# Loop through each row
for i in range(rows, 0, -1):
    # Print stars
    for j in range(i):
        print("*", end="")
    # Move to the next line after each row is printed
    print()
####
###
##
#
```