# crates-mirror

Crates-Mirror is a simple tool to provide a caching mirror for [crates.io](https://crates.io/). It's serving a local index which is synced with a remote index. All requested crates are downloaded and cached localy for further usage.


## Installing

You can install it using `cargo install crates-mirror`

## Usage

### Local
Stores the index localy on the filesystem.
```toml
base_path = "/path/to/store/crates"
listen_on = "localhost:3000"
remote_api = "https://crates.io"
poll_intervall = 60 #seconds
registry_config = {upstream_url = "https://github.com/rust-lang/crates.io-index"}
```
### Remote Index
Stores the index in a remote git repositority.
```toml
base_path = "/path/to/store/crates"
listen_on = "localhost:3000"
remote_api = "https://crates.io"
poll_intervall = 60 #seconds
registry_config = {upstream_url = "https://github.com/rust-lang/crates.io-index", origin_url = "git@own.host/whatever"}
```

## License

Licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.