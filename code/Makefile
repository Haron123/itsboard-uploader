all: build-linux build-windows build-macos copy-bins

build-linux:
	cargo build --release --target x86_64-unknown-linux-gnu

build-windows:
	cargo build --release --target x86_64-pc-windows-gnu

build-macos:
	cargo build --release --target x86_64-apple-darwin
	cargo build --release --target aarch64-apple-darwin

copy-bins:
	cp target/x86_64-pc-windows-gnu/release/uploader.exe uploader.exe
	cp target/x86_64-unknown-linux-gnu/release/uploader uploader
	cp target/x86_64-apple-darwin/release/uploader uploader-macos-x86_64
	cp target/aarch64-apple-darwin/release/uploader uploader-macos-arm64