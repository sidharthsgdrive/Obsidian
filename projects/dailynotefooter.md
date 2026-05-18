`19/07/25`

## Aim
To write a program that adds a footer to each .md file in the folder starting from the file 060725-Sun.
The footer should consist of two parts: `***\n` and `next:[[{day+1}{month}{25}-{weekday+1]]}`. 

### Tools/Requisites
* Python 3.13
* `os` library ([documentation](https://docs.python.org/3/library/os.html))

#### Notes
This is not a flexible or robust program by any means, as I hardcoded most of the features. Still, it gave me a tiny bit of Python practice and familiarized me with the `os` library.

##### Code
```Python
import os

dir_name = "C:/Users/jainv/My Drive/Obsidian Sync/obsidian/dailynotes"
nameslist = os.listdir(dir_name)
nameslist.remove("dailynotes.md")
days = ("Mon","Tue","Wed","Thu","Fri","Sat","Sun")

for name in nameslist:
    if name[2:4] == "07" and int(name[0:2]) > 5:
        continue

    tmwdate = f'{(int(name[0:2])+1):02d}'
    if name[0:2] == "30":
        tmwmonth = "07" 
        # hardcoded for june; replace w/ smth like line 26 to extend.
    else:
        tmwmonth = f'{(int(name[2:4])):02d}'
    tmwyr = "25" # again, hardcoded.
    try:
        tmwday = days[days.index(name[7:10])+1]
    except:
        tmwday = "Mon"
    linkstr = '[['+tmwdate+tmwmonth+tmwyr+'-'+tmwday+']]'
    print(name + ' - ' + linkstr)
    
    filepath = os.path.join(dir_name, name)
    with open(filepath, 'a', encoding="UTF-8") as fp:
        fp.write(f"***\nnext: {linkstr}")
```