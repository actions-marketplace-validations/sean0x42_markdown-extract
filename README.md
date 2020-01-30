# Markdown Extract

Extract sections of a markdown file. This project mostly exists to help me learn
Rust, and to fill a niche requirement for extracting patch notes from
a `CHANGELOG.md`.


## Usage 

Start by installing `markdown-extract`. Requires Cargo.

```
cargo install markdown-extract 
```

View the help guide if you like.

```console
$ markdown-extract -h
markdown-extract 1.0.0
Extract sections of a markdown file

USAGE:
    markdown-extract [FLAGS] <pattern> <path>

FLAGS:
    -s, --case-sensitive          Treat pattern as case sensitive
    -f, --first                   Only return the first match
    -h, --help                    Prints help information
    -i, --ignore-first-heading    Do not include the top level section heading
    -r, --regex                   Compile pattern as a regular expression
    -V, --version                 Prints version information

ARGS:
    <pattern>    Pattern to match against section headings
    <path>       Path to markdown file
```

Then extract matching sections in a markdown file.

```console
$ markdown-extract --fr "^v1" CHANGELOG.md
## v1.0.0

...
```


## Use Cases

There aren't many. I created this tool to extract patch notes from a
`CHANGELOG.md` by version. If you have another use for this binary, please let
me know!
