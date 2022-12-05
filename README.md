# Kroeg

> kroeg noun \- pub \- bar

This is a [collection of repositories](https://puck.moe/git/kroeg/) forked from work by [Puck Meerburg](https://puck.moe).

## how to run

1. [install rust](https://www.rust-lang.org/tools/install)
2. check that the project builds with `cargo build` 
3. install postgresql
   - create a new db with `psql postgres -c 'CREATE DATABASE kroeg;'`
   - initialize the schema with `psql kroeg -f cellar/schema/db.sql`
4. `cd kroeg` to enter the folder of the main cli tool
5. use `cargo run --bin kroeg serve` to run the server
6. use `cargo run --bin kroeg actor name create` to create a new actor named `name`
7. run `cargo doc` to build helpful docs
