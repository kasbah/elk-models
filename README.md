# ELK Models Repository

This repository holds test models for the [Eclipse Layout Kernel](https://github.com/eclipse/elk) project.
These test files are used while developing our layout algorithms, to reproduce and fix bugs, and to run automated tests to ensure the bugs remain fixed.


## Repository Layout

On the top level, the repository contains the following folders:

Folder     |  Description
-----------|-------------
`tests`    | Test graphs written or generated by us.
`realworld`| Graphs obtained by converting examples from the real world into formats we can use.
`tickets`  | Graphs that reproduce problems described in GitHub tickets.

Both `tests` and `tickets` are further subdivided into folders specific to layout algorithms (`layered`, `force`, etc) or applicable to all algorithms (`common`). In the `test` tree, these folders may contain further folders specific to the respective tickets, if more than one file is produced for a given ticket.


## File Types

The file types we use are the following:

Type      | Description
----------|--------------------
`.elkt`   | Textual ELK graph language. See [the specification](https://www.eclipse.org/elk/documentation/tooldevelopers/graphdatastructure/elktextformat.html).
`.elkg`   | EMF's XMI-based representation of ELK graphs.
`.json`   | JSON files. See [the specification](https://www.eclipse.org/elk/documentation/tooldevelopers/graphdatastructure/jsonformat.html).
`.md`     | Readme files can be placed in folders to describe their purpose.


## License Headers

All files except for the JSON files must contain a proper licence at the file header.
The `license.py` script in the repository's root folder can help.
Common use cases:

```bash
# Ensure all files have licence headers
python3.6 license.py --verbose --company "Your company's name"

# Add licence headers to files staged for commit
python3.6 license.py --verbose --staged --company "Your company's name"

# Also update existing licence headers to include the current year
python3.6 license.py --verbose --staged --update --company "Your company's name"
```

To see what the script would do, add the `--dry-run` option (or `-n` for short).

See the command-line help for more options (`--help`).
