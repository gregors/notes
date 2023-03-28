# Ruby


## using Ruby in cli pipelines

```ruby
cat boom.txt | sort | uniq | wc -l
50

cat boom.txt | ruby -n -e 'puts $_.downcase.chomp' | sort | uniq | wc -l
25
```
