## HI!

> The build makefile has been adjusted to include the `/modules/tpch-data/` directory in the SQLite kernel. `/modules/tpch-data/` has the tables and queries from TPC-H.

1. To build the image:
    ```
    ./scripts/build image=sqlite
    ```

2. To run the image:
    ```
    ./scripts/run.py
    ```
