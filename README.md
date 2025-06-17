# BIBLIOTECA          
    
Group files in current directory by prefix separated by `.`       
Store the following to a `cleanup.sh` and run chmod +x and ./ execute.     
```
#!/bin/bash

for file in *.*; do
    prefix="${file%%.*}"  # Get the prefix before the first dot
    mkdir -p "$prefix"    # Create a directory for the prefix
    mv "$file" "$prefix/"  # Move the file into the directory
done
```

