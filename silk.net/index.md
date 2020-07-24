[![NuGet Version](https://img.shields.io/nuget/v/Silk.NET)](https://nuget.org/packages/Silk.NET) [![Preview Feed](https://img.shields.io/badge/nuget-experimental%20feed-yellow)](https://dev.azure.com/UltzLimited/Silk.NET/_packaging?_a=feed&feed=Experimental) [![Build Status](https://dev.azure.com/UltzOS/Silk.NET/_apis/build/status/Ultz.Silk.NET?branchName=master)](https://dev.azure.com/UltzOS/Silk.NET/_build/latest?definitionId=2&branchName=master) [![Join our Discord](https://img.shields.io/badge/chat%20on-discord-7289DA)](https://discord.gg/DTHHXRt)

# Introduction

Silk.NET is a high-speed, advanced library, providing bindings to popular low-level APIs such as OpenGL and OpenAL. Use Silk.NET to add cross-platform 3D graphics, audio, compute and haptics to your C# application.

Silk.NET works on any .NET Standard 2.0 compliant platform. This includes  .NET Framework 4.6.1+ and .NET Core 2.0+.

# Features
- **Performance**: We use lesser-known techniques for our native interop which makes our bindings blazing fast.
- **Up-to-date**: We've built Silk.NET around the latest versions of the Khronos specifications, and release updates every month to keep up with the ever changing specs.
- **High-level utilities**: We provide high-level abstractions around Windowing and Input APIs, which means your apps can run on any platform without changing a single line.
- **Game-ready**: Making games or game engines with Silk.NET is a breeze as you already have everything a game needs - Graphics, Audio, Input, and Windowing; all in one product!

# Our bindings
| Library | Upstream Version | Silk.NET Version |
|---------|------------------|------------------|
| OpenGL  | 4.6              | 1.0 onwards      |
| OpenGLES| 3.2              | 1.0 onwards      |
| OpenAL  | 1.1              | 1.0 onwards      |
| GLFW    | 3.3              | 1.0 onwards      |
| Vulkan  | 1.2              | 1.0 onwards      |
| OpenCL  | 3.0              | 1.2 onwards      |
| EGL     | 1.5              | 1.0 through 2.0  |
| Assimp  | 5.0              | 2.0 Preview 1 onwards  |
| OpenXR  | 1.0              | 2.0 Preview 1 onwards  |

# Join the conversation

Come chat with us on [Discord](https://discord.gg/DTHHXRt)!

# License
Silk.NET is distributed under the very permissive MIT/X11 license and all dependencies are distributed under MIT-compatible licenses.
