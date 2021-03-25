build_static_lib:
	cd lib && swift build -c release
	cd lib/.build/release && ar -rcs liblib.a lib.build/lib.swift.o

compile_main:
	swiftc main.swift -I lib/.build/release -L lib/.build/release -llib
