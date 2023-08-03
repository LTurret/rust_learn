# Description

此[範例](./src/main.rs)示範如何做出等價於 Python 中的 `os.listdir()`

## Code

```rust
use std::fs;

fn main() {
    let paths = fs::read_dir("./").unwrap();

    for path in paths {
        println!("{}", path.unwrap().path().display());
    }
}
```

## Build

```shell
cargo run
```
