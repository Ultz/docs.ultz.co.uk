# Common exceptions
## PlatformNotSupportedException: Couldn't find a suitable windowing platform.
### Symptoms
When attempting to call Window.Create, a NotSupportedException is thrown with a message indicating that the windowing system couldn't find a windowing platform.

### Cause
There are multiple causes for this particular exception, however the most common are:
1. The underlying windowing API could not be loaded.
2. The underlying windowing API does not support the current platform.

### Resolution
#### Ensure the underlying API is present on the system
Silk.NET should do a good job of copying the appropriate native libraries upon build by default, and will search your PATH for them if not present in the output directory.

However, in some environments this system is not reliable and you will need to provide the binaries yourself. To do so:
1. Download or build your chosen native API (you will be able to find instructions on how to do this in their repositories)
   - GLFW: https://github.com/glfw/glfw
   - Allegro: https://github.com/liballeg/allegro5/
2. Retreive the resultant binary files and place them in your program's output directory.
3. Ensure the file names match what Silk.NET expects, as illustrated by the table below:

| Platform | Underlying API | File Name            |
|----------|----------------|----------------------|
| Windows  | GLFW 3.3       | glfw3.dll            |
| Linux    | GLFW 3.3       | libglfw.so.3         |
| MacOS    | GLFW 3.3       | libglfw.3.dylib      |
| Windows  | Allegro 5.2    | allegro-5.2.dll      |
| Linux    | Allegro 5.2    | liballegro.so.5.2    |
| MacOS    | Allegro 5.2    | liballegro.5.2.dylib |
| iOS      | Allegro 5.2    | TBD                  |
| Android  | Allegro 5.2    | TBD                  |

#### Ensure the underlying API supports the current platform

You should be using a version of Silk.NET and an appropriate windowing backend that support the platform you are trying to run on. See the below table for first-party support.

| Silk.NET Version | Underlying API | Supported platforms                 | Packages                   |
|------------------|----------------|-------------------------------------|----------------------------|
| 1.X, 2.X         | GLFW 3.3       | Windows, MacOS, Linux               | Silk.NET.Windowing.Desktop |
| 2.X              | Allegro 5.2    | Windows, MacOS, Linux, iOS, Android | Silk.NET.Windowing.Allegro |
