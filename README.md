# Kroeg

> kroeg noun - pub - bar

This is a collection of repositories forked from work by [Puck Meerburg](https://puck.moe).

- [server](https://puck.moe/git/kroeg/server)
- [cellar](https://puck.moe/git/kroeg/cellar)
- [tap](https://puck.moe/git/kroeg/tap/)
- [jsonld-rs](https://github.com/kroeg/jsonld-rs)

## how to run

1. [install rust](https://www.rust-lang.org/tools/install)
2. build the project with `cargo build` 
   - (optionally include `--release` for an optimized build without debug info)
3. start up a postgres instance with `cellar/schema/db.sql`
4. copy `server/server.toml.example` to `sever/server.toml`, and "set it up as required"
5. create root users with 
   - `cargo run --bin kroeg-call create https://example.com/~exampleUser exampleUser "Example User"`
6. get an authorization key by running 
   - `cargo run --bin kroeg-call auth https://example.com/~exampleUser`
   - use this authorization key in the header of any requests
7. use `cargo run --bin kroeg` to actually run the server
