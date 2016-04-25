.PHONY: main

INVENTORY 				:=
UNAME_S := $(shell uname -s)
ifeq ($(UNAME_S),Linux)
    INVENTORY += inventory-docker
endif
ifeq ($(UNAME_S),Darwin)
    INVENTORY += inventory-docker-machine
endif

all:
	ansible-playbook -i $(INVENTORY) -l centos,localhost main.yml -vvvv
	#ansible-playbook -i $(INVENTORY) -l ubuntu,localhost main.yml -vvvv

