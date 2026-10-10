Changed

- **Dev and test builds keep line tables and drop dependency debug info.** Workspace crates still panic with a file and line. Third-party crates compile with no debug info, so `target/dev` and rustc use less disk and RAM.
