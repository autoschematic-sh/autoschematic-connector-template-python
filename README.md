## autoschematic-connector-template-python

This crate is a minimal starter template for building a new Autoschematic connector in Python. 

Start with these changes:

1. pip install autoschematic-sdk
2. Rename `DummyConnector` everywhere.
3. Start following the guide at [https://autoschematic.sh/guide/building-your-own-connectors-in-python/a-starter-template/](https://autoschematic.sh/guide/building-your-own-connectors-in-python/a-starter-template/)

Test import with `autoschematic import` .


This repo includes autoschematic.ron already hooked up to load the local python connector. Happy hacking!.


```rust
AutoschematicConfig(
    prefixes: {
        "main": Prefix(
            connectors: [
                Connector(
                    shortname: "dummy",
                    spec: PythonLocal(
                        // Absolute paths are also supported.
                        // path: "/home/chef/prog/ottercorp-connector-mything/mything.py",
                        path: "./connectors/dummy.py",
                    ),
                )
            ]
        )
    }
)