#CC=arm-linux-gnueabihf-gcc
#CC=gcc
CXX=g++
# 定义输出目录
OUTPUT_DIR=./build
BOARD_OUTPUT_DIR=/home/minglie/workspace/nfs/rootfs/home/workspace

server:$(OUTPUT_DIR)
	$(CXX) -Wall   -I./ -o $(OUTPUT_DIR)/server  ./main_server.c ./ws_com.c ./ws_server.c  -lpthread

board_server:$(OUTPUT_DIR)
	$(CXX) -Wall   -I./ -o $(BOARD_OUTPUT_DIR)/server  ./main_server.c ./ws_com.c ./ws_server.c  -lpthread


client:$(OUTPUT_DIR)
	$(CXX) -Wall  -I./  -o $(OUTPUT_DIR)/client ./main_client.c ./ws_com.c ./ws_server.c   -lpthread

# 创建输出目录
$(OUTPUT_DIR):
	mkdir  $(OUTPUT_DIR)


clean:
	rm -rf $(OUTPUT_DIR)/*
