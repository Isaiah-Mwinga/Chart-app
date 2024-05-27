postgresinit:
    docker run --name postgres15 -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=root -d postgres:15-alpine

postgres:
    docker exec -it postgres15 psql --username=postgres -c "\l"

createdb:
	docker exec -it postgres15 createdb --username=postgres --owner=postgres go-chart

dropdb:
	docker exec -it postgres15 dropdb go-chart		

.PHONY: postgresinit
