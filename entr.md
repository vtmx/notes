
## entr

```sh
# http://eradman.com/entrproject

# With file exec
echo filename.sh | entr ./filename.sh

# Clear terminal
echo filename.sh | entr -c ./filename.sh

# No file exec
echo ls *.sh | entr /bin/bash filename.sh
```
