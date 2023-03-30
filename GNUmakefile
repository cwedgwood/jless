# cw overler makefile

# https://msfjarvis.dev/posts/building-static-rust-binaries-for-linux/

default: build

build:
	RUSTFLAGS='-C target-feature=+crt-static' cargo build --release --target x86_64-unknown-linux-gnu
	strip target/x86_64-unknown-linux-gnu/release/jless
	ldd target/x86_64-unknown-linux-gnu/release/jless
	ls -lh target/x86_64-unknown-linux-gnu/release/jless

clean:
	cargo clean --target x86_64-unknown-linux-gnu
	cargo clean

