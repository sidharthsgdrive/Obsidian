```Python
import pathlib
import os

root = pathlib.Path("C:/Users/jainv/Downloads/Obsidian Sync")

# Leaving this project for now, since it would be a hassle to update all the links.
# A way to go about it would be to store the old and new names, and recursively go through each file and update the [[links]].

#to rename directories
for dir in root.rglob('*'):
    if dir.is_dir() and ".obsidian" not in dir.parts:
        new_dir_name = dir.stem.lower().strip('_').replace(" ", "_")
        if new_dir_name != dir.name:
            print(f"Renamed {dir.stem} ---> {new_dir_name}")
            dir.rename(dir.parent / new_dir_name)

#to rename files
for file in root.rglob('*.md'):
    if file.is_file():
        new_file_name = file.stem.lower().strip('_')
        print(file.stem)
```
