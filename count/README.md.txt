# Count

## Count Files In A Directory

wc -l

## Count Files In Subdirectories

find . -maxdepth 1 -type d | while read -r dir
do printf "%s:\t" "$dir"; find "$dir" -type f | wc -l; done;