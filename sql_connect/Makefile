WORK_PATH=$(shell pwd)

BIN=sql_connect
CC=g++
INCLUDE= -I${WORK_PATH}/mysql_lib/include/mysql -I.
LIB_PATH= -L${WORK_PATH}/mysql_lib/lib/mysql
LD_FLAGS=-lpthread -ldl -lrt
SRC=sql_connect.cpp

LIB_NAME=-lmysqlclient

${BIN}:${SRC}
	${CC} -o $@ $^ ${INCLUDE} ${LIB_PATH} ${LIB_NAME} $(LD_FLAGS) -g -D_DEBUG_
.PHONY:clean
clean:
	rm -f ${BIN}

