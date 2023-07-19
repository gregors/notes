# Grep

## NOT grep commands
```bash
grep -v pattern
```

## OR grep commands
```bash
grep 'pattern1\|pattern2'
grep -E 'pattern1|pattern2'
egrep 'pattern1|pattern2'
grep -e pattern1 -e pattern2
```

## remove items that appear on a list
```bash
cat list1.txt | grep -vFf list2.txt > filtered_list.txt
```

## Get os pretty name
```bash
grep PRETTY_NAME /etc/os-release
```
