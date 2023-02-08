
# Triton package to json

Library for converting triton(.tpkg) structural package to JavaScript Object Notation(JSON)


## Features

- Fast work
- Comfortable

## Last update

| Version             | What`s new                                                                |
| ----------------- | ------------------------------------------------------------------ |
| 1.0.0.0 | Release for tpl |
| 1.0.0.1 | Added Refactoring |
| 1.0.0.2 | New Line Fix |
| 1.0.0.2 | Separate repository |





## Installation

Install Triton package to json with git

```bash
  cd my-project
  git clone https://github.com/Lofinaf/triton-.tpkg-structure-to-json
```
    
## Building to DLL

To build to dll file

```bash
cd my-project
make
```


## Usage/Examples

From C#(Need build dll with Makefile)
```csharp
using System;
using System.Runtime.InteropServices;

public enum Parse_Result
{
    SUCCESS,
    BAD_INPUT,
    INVALID_FIELD,
    NOT_SUCH_FILE,
    EMPTY_FILE,
    LARGE_FILE,
    ACCESS_DENIED
}

[DllImport("packet_parser.dll", CallingConvention = CallingConvention.Cdecl)]
public static extern Parse_Result parse_packet(string packet_path, string output_path);

var Result = parse_packet("test.tpkg", "test.json");
Console.WriteLine(Result.toString());
```

From C++

```cpp
#include<stdio.h>
extern "C" {
    #include "packet_parser.h"
}
int main() {
    Parse_Result Result = parse_packet("test.tpkg", "test.json");
    printf("%s", parse_result_to_cstr(Result));

    return 0;
}
```


## Authors

- [@РАСТР_НЕ_ВЕКРОТ](https://github.com/Nikita-bunikido)

