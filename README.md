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
3. install postgresql
   - create a new db with `psql postgres -c 'CREATE DATABASE kroeg;'`
   - initialize the schema with `psql postgres -f cellar/schema/db.sql`
4. create root users with 
   - `cargo run --bin kroeg-call create https://example.com/~exampleUser exampleUser "Example User"`
5. get an authorization key by running 
   - `cargo run --bin kroeg-call auth https://example.com/~exampleUser`
   - use this authorization key in the header of any requests
6. use `cargo run --bin kroeg` to actually run the server
