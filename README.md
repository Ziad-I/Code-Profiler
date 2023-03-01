# Code Profiler

A Code Profiler in C++  that allows you to profile your code and generate a JSON file that can be visualized in Chrome using the `chrome://tracing` tool. With this tool, you can get a detailed view of your code's execution time and identify performance bottlenecks.

## Installation

To use Code Profiler in your project, download the `Profiler.h` file and include it in your project. The `Profiler.h` file contains the necessary code to profile your functions and output the profiling data to a JSON file.

## Usage

To use the profiler in your code, you need to add the following line at the beginning of each function that you want to profile:

This will profile the execution time of the function and output the data to a JSON file.

```cpp
PROFILE_FUNCTION();
```

#### example

```cpp
#include "Profiler.h"

void myFunc()
{
    PROFILE_FUNCTION();
    // do something
}
```

You can also profile a scope block by using the following line:

This will profile the execution time of the scope block and output the data to a JSON file.

```cpp
PROFILE_SCOPE("Scope Name");
```

#### example

```cpp
#include "Profiler.h"

void myFunc()
{
    for(int i = 0; i < 100; i++)
    {
        PROFILE_SCOPE("Loop itr: " + i)
        // do something
    }
}
```

After running your code, you will get a result.json file that contains the profiling data. You can then load this file into `chrome://tracing` to visualize the data and identify performance bottlenecks.

`chrome://tracing` controls:

- `W` to zoom in
- `S` to zoom out
- `A` to move left
- `D` to move right
