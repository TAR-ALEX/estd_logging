# estd_logging
Provides a proxy object for an ostream (ostream_proxy)

Example usage:

```c++
#include <iostream>
#include <fstream>
#include <estd/ostream_proxy.hpp>

int main(){
    std::ofstream outputHereAsWell("cout.txt");
    estd::ostream_proxy cout{ {&std::cout, &outputHereAsWell }};
    cout << "Will output to the file and stdout" << std::endl;
}
```

The makefile will build and run the main file. (modify the main file to try out the library)


To use this project with a dependency manager install the cpp-dependency-manager project from https://github.com/TAR-ALEX/Cpp-Dependency-Manager.git

and create a vendor.txt file and add the following entries:

```
git "https://github.com/TAR-ALEX/substreams_cpp" main "./include" "./vendor/include",

```