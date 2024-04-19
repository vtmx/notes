# find

```
# Extension
find src/ -name *.html

# Only files
find src/ -type f

# Show all file by extension separate by comma: 'file1.mp3' 'file2.mp3'
find $(pwd) -type f -name "*.mp3" -printf "'%p' "

# Print all file in unique line
find . -path "*.mp3" -print0


# Print all files with new line
find . -type f -name "*.mp3" -printf "\n%p "
```
