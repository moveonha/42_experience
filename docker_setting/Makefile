all:
	make up
build:
	docker-compose build -f ./docker-compose.yml
go:
	docker exec -it Dock /bin/bash
up:
	docker-compose -f ./docker-compose.yml up -d
	docker exec -it Dock /bin/bash
down:
	docker-compose down -f ./docker-compose.yml
clean:
	docker-compose -f ./docker-compose.yml down
	docker volume rm $$(docker volume ls -q) || true
fclean:
	docker-compose -f ./docker-compose.yml down
	docker volume rm $$(docker volume ls -q) || true
	docker image rm $$(docker images -aq) || true
re:
	make fclean
	make all
.PHONY : all build up down clean fclean re
