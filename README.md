# luasocket
luasocket for lua5.3

## 先编译安装lua
	sudo apt-get install libreadline-dev curl
	curl -R -O http://www.lua.org/ftp/lua-5.3.2.tar.gz
	tar zxf lua-5.3.2.tar.gz
	cd lua-5.3.2
	在CFLAGS为lua添加-fPIC编译选项， 
	vim src/Makefile
	CFLAGS= -O2 -Wall -fPIC -Wextra -DLUA_COMPAT_5_2 $(SYSCFLAGS) $(MYCFLAGS)
	编译安装
	sudo make linux && make install

## 编译安装luasocket
	git clone https://github.com/jinzt/luasocket.git
	cd luasocket/
	sudo make && make install