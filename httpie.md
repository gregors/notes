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
* `http -v POST :4000/api/cars  data:='{"make":"ford", "model":"focus"}'`

# PUT nested json
```json
{
 "good": "bye",
 "message": {
   "hey": "man"
 }
}
```
* ` http PUT :4000/api/data/boom hello=hey good=bye message:='{"hey": "man"}'`


# no verify for self signed ssl certs
* `--verify=no`

# with basic auth

* ` http --auth user:pass PUT :4000/api/data/boom hello=hey good=bye message:='{"hey": "man"}'`
