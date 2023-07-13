## sed

### Against variables
sed ‘s/Hello/Hi/g’ <<< “$var”

### Against file

sed ‘s/Hello/Hi/g’ -i /path/goes/here.txt

### Delete a line

sed ‘/pattern/d’

### Replace with string

sed ‘s/pattern/string/g’
