## sed

### Against variables
sed ‘s/Hello/Hi/g’ <<< “$var”

### Against file

sed ‘s/Hello/Hi/g’ -i /path/goes/here.txt

### Delete a line

sed ‘/pattern/d’

### Replace with string

sed ‘s/pattern/string/g’

## Run portion of Bash script as another user
```bash
if [[ $(id -u) -eq 0 ]]; then
  su - target_user -c "$(cat << 'EOF'
    # command1
    # command2
    EOF
  )"
else
  echo "Exiting as not root..."
fi
```