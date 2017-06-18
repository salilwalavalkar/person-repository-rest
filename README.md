## Spring Boot, CRUD operations, REST and H2 Database

#### Reference: http://spring.io/guides/gs/accessing-data-rest/

List data:
curl http://localhost:5000/restrepository/people

Add new entry:
curl -i -X POST -H "Content-Type:application/json" -d "{  \"firstName\" : \"Tony\",  \"lastName\" : \"Stark\" }" http://localhost:5000/restrepository/people

curl -i -X POST -H "Content-Type:application/json" -d "{  \"firstName\" : \"Bruce\",  \"lastName\" : \"Wayne\" }" http://localhost:5000/restrepository/people

PUT replaces an entire record. Fields not supplied will be replaced with null. PATCH can be used to update a subset of items.

Update entry:
curl -X PUT -H "Content-Type:application/json" -d "{ \"firstName\": \"Elon\", \"lastName\": \"Stark\" }" http://localhost:5000/restrepository/people/1
curl -X PATCH -H "Content-Type:application/json" -d "{ \"firstName\": \"Elon\", \"lastName\": \"Stark\" }" http://localhost:5000/restrepository/people/1

Delete by id:
curl -X DELETE http://localhost:5000/restrepository/people/1

Search By Id:
curl http://localhost:5000/restrepository/people/1

Search by last name:
curl http://localhost:5000/restrepository/people/search/findByLastName?name=Stark

Search links:
curl http://localhost:5000/restrepository/people/search