# HTTPie

# POST nested json
```json
{
 "data": {
   "make": "ford",
   "model": "focus"
 }
}
```
* `http -v POST :4000 /api/cars  data:='{"make":"ford", "model":"focus"}'`
