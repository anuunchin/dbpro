## HI!

> The build makefile has been adjusted to include the `/modules/tpch-data/` directory in the SQLite kernel. `/modules/tpch-data/` has the tables and queries from TPC-H, as well as a setup script that creates and populates tables from the files.

1. Run:
    ```
    git submodule update --init --recursive
    ```

2. Add `-D_FORTIFY_SOURCE=0` flag to `/apps/sqlite/GET`.

    ```
    cc -O2 -fPIC -Wall -shared -DHAVE_MREMAP=0 -D_FORTIFY_SOURCE=0 -o libsqlite3.so.0 upstream/sqlite-amalgamation-$VERSION/*.c
    ```

3. To build the image:
    ```
    ./scripts/build image=sqlite
    ```

4. To run the image:
    ```
    ./scripts/run.py
    ```
