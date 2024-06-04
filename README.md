# Problem 1: Temukan jumlah substring

```Python
def substring_count(string, substring):
    count = 0
    start_index = 0

    while start_index <= len(string) - len(substring):
        index = string.find(substring, start_index)

        if index != -1:
            count += 1
            start_index = index + 1
        else:
            break

    return count


result = substring_count('ABCDCDC','CD')
print(f"Output: {result}")
```

``` Python
substring_count('ABCDCDC', 'CDC')
#Expected output= 2
```

``` Python
 result = substring_count('DEDFDEDEDEG', 'DED')
 print(f"Output: {result}")
```

``` Python
def substring_count(string, subs):
    count = 0
    for i in range(0, len(string)):
        potongan = string[i:i + len(subs)]
        if potongan == subs:
            count += 1
    return count

substring_count('ABCDCDC','CD')

substring_count('ABCDCDC', 'CDC')

substring_count('DEDFDEDEDEG', 'DED')

```


# Problem 2: Berapa banyak huruf berbeda yang ada di string?

```Python
def diff_letters(input_string):
    unique_letters = set(input_string)
    return len(unique_letters)


input_str = 'AAAAAAAAAB'
result = diff_letters(input_str)
print(f"Output: {result}")
```
``` Python
input_str = 'ABCDAAAABBCCCE'
result = diff_letters(input_str)
print(f"Output: {result}")
```
```Python
input_str = 'ABCDAAAABBCCCENWKLDDIITJDDTTDFGGGANR'
result = diff_letters(input_str)
print(f"Output: {result}")
```
``` Python
def diff_letters(string):
    liststring = [x for x in string]
    setstring = set(liststring)
    return len(setstring)

diff_letters('AAAAAAAAAB')

diff_letters('ABCDAAAABBCCCE')
```

# Problem 3: Temukan Jarak Antara Dua Koordinat - Medium
``` Python
def distance(koordinat_string):
    koordinat = [tuple(map(int, x.strip('()').split(','))) for x in koordinat_string.split('), (')]

    jarak = math.sqrt((koordinat[0][0] - koordinat[1][0])**2 + (koordinat[0][1] - koordinat[1][1])**2)

    return f"The distance is {int(jarak)}" if jarak.is_integer() else f"The distance is {jarak}"
```
``` Python
## Example
a = '(5,5), (1,2)'

distance(a)

# when you run this cell, it is expected that the output will be:
# 'The distance is 5'
```
``` Python
string = distance('(0,-1), (-3,2)')
string
```
``` Python
string = distance('(5,-5), (1,2)')
string
```
``` Python
string = 'A5CDEF5GHIJK'

x1 = string[1]

x1
```
``` Python
string = 'A5C-EF5GHIJK'
x2 = string[3]
x2
```
