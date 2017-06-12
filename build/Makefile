PHONY: all clean

all: build.jar

build.class: build.java
	javac $^
build.jar: build.class
	jar -cfe $@ Hello $^
clean:
#	-rm -f build.jar build.class
