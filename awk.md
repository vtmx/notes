# AWK

```
# Remove blankline of file
awk NF file.txt

# Print entire line from pattern
awk '/\<span.*/ {print $0}'
```
