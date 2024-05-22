## HI!

> The build makefile has been adjusted to include the `/modules/tpch-data/` directory in the SQLite kernel. `/modules/tpch-data/` has the tables and queries from TPC-H, as well as a setup script that creates and populates tables from the files.

1. Run:
    ```
    git submodule update --init --recursive
    ```

2. To build the image:
    ```
    ./scripts/build image=sqlite
    ```

3. To run the image:
    ```
    ./scripts/run.py
    ```
