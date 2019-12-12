쉽게 얘기하면 elasticsearch 에서 index 는 database에서 table이라고 보면 된다. <br>
Index in elasticsearch can (it's different but.. make my understanding clear)
be said to be same as tables in databases.

<hr>

To make a customer index with type name _doc<br>
customer 라는 index, type은 _doc 이라고 만들려면 terminal 에서 아래와 같이 타이핑 한다.
```
in terminal : 
curl -X PUT "localhost:9200/customer/_doc" -H 'Content-Type: application/json' -d'
```
   