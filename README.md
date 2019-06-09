----
To compile on Windows using Microsoft Visual Studio 2019
----

1. Clone the source code in following directory structure:
~~~~
    src/
        apr/
        apr-iconv/
        apr-util
        libexpat/
~~~~
2. Checkout following branches in apr, apr-iconv and apr-util *(notice that these are **not tags**, but **branches** I have created)*
    1. git checkout v1.7.0 **(in apr) **
    1. git checkout v1.2.2 **(in apr-iconv)**
    1. git checkout v1.6.1 **(in apr-util)**
1. Open the aprutil.sln in apr-util directory
1. Right click on libaprutil-1 and select *Project Only -> Build Only libaprutil-1*
1. Compilation will fail complaining about a missing library. Right click on the project for that library and again select *Project Only -> Build Only ...* until libaprutil-1 is successfuly compiled.
