# Installation
```
pip install pbeasypostgres
```
# How to use?
```python
from easypostgres import Connection

with Connection("your host","your user","your password","your database") as connection:
  connection.Query('insert into "Client"("Login","Password") values(%s,%s);', ("John","qwerty"))
  client = connection.Query('select "Id","Login","Password" from "Client";')[0]
  print(client.Id, client.Login, client.Password)
```
