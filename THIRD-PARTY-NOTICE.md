# Third-party notice

`include/Common.hpp`, `include/File/Macros.hpp`, `include/GUI/GUITab.hpp`,
and `include/Mod/CppUserModBase.hpp` are trimmed copies of headers from the
[UE4SS project](https://github.com/UE4SS-RE/RE-UE4SS) (`v3.0.1` tag,
commit `d935b5b`), used here only to compile against UE4SS's C++ mod ABI.

UE4SS is MIT licensed:

```
MIT License

Copyright (c) 2022 Narknon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

`main.cpp` and `main.lua` are original code, not derived from UE4SS.

`UE4SS.def` is a locally generated symbol list (not copied from UE4SS) used
to build an import library against your own installed `UE4SS.dll` -- see
`BUILD.md`.
