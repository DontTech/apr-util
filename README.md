----
To compile on Windows using Microsoft Visual Studio 2019
----

1. Clone the source code in following directory structure:
~~~~
    /
    |---apr/ (from https://github.com/DontTech/apr.git)
    |---apr-iconv/ (from https://github.com/DontTech/apr-iconv.git)
    |---apr-util (from https://github.com/DontTech/apr-util.git)
    |---libexpat/ (from libexapt release version 2.2.6, rename the extraced directory from libexpat-R_2_2_6/ to libexpat/)
~~~~
2. Checkout following branches in apr, apr-iconv and apr-util *(notice that these are **not tags**, but **branches** I have created that have new changes)*
    1. git checkout v1.7.0 **(in apr)**
    1. git checkout v1.2.2 **(in apr-iconv)**
    1. git checkout v1.6.1 **(in apr-util)**
3. First compile libexpat:
    1. Open expat.sln in libexpat\expat directory
    1. Build Solution
1. Open the aprutil.sln in apr-util directory
1. Right click on libaprutil-1 and select *Project Only -> Build Only libaprutil-1*
1. Compilation will fail complaining about a missing library. Right click on the project for that library and again select *Project Only -> Build Only ...* until libaprutil-1 is successfuly compiled.

Following projects should build without any hiccup:
1. apr
1. aprapp
1. apriconv
1. aprutil
1. libapr-1
1. libaprapp
1. libapriconv-1
1. libaprutil-1
