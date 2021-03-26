arm64:
	cd lib && swift build -c release --arch arm64
	cp lib/.build/arm64-apple-macosx/release/liblib.a liblib_arm64.a

x86_64:
	cd lib && swift build -c release
	cp lib/.build/x86_64-apple-macosx/release/liblib.a liblib_x86_84.a

swiftmodule:
	cp lib/.build/release/lib.swiftmodule ./

fat: arm64 x86_64 swiftmodule
	lipo -create liblib_x86_84.a liblib_arm64.a -output liblib.a

main: fat main.swift
	swiftc main.swift -I . -L . -llib
