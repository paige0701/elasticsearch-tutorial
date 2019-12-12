## Getting started with elasticsearch

macOS: Download the Elasticsearch archive for your OS
(일라스틱서치 다운로드)
```
curl -L -O https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.5.0-darwin-x86_64.tar.gz
```
<br>   

unzip downloaded es file (다운받은 elasticsearch 압축 해제한다)
 
change directory to bin folder (bin 폴더로 이동한다)
```
cd elasticsearch-7.5.0/bin
```
<br>

to start Elasticsearch (일라스틱서치 시작)
```
./elasticsearch 
```
<br>

you can start more instances of elasticsearch (일라스틱 서치 인스턴스 여러개 시작) 
```
./elasticsearch -Epath.data=data2 -Epath.logs=log2
./elasticsearch -Epath.data=data3 -Epath.logs=log3
```

<br>

to check three-node cluster is up and running from terminal (엘라스틱서치 인스턴스가 실행 되고 있는지 터미널에서 확인하기)
```
curl -X GET "localhost:9200/_cat/health?v&pretty"
```
node.total이 3으로 나와있는걸 확인 할 수 있다.<br>
You can see that node.total is 3



<br>

check if elasticsearch is up - type in browser (엘라스틱서치 떴는지 브라우저에서 확인)
```
http://127.0.0.1:9200/
```

if instance is not up and you try to access 
```
127.0.0.1:9200/animal/_doc/_search
```
You get an error ->  There was an error connecting to 127.0.0.1:9200/animal/_doc/_search. 