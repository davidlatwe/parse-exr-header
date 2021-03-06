# parse-exr-header
Pure Python (no additional dependencies) helper functions to read metadata from the header of EXR files.

# Reasons
In the VFX world we've got tons of great open source initiatives, like ILM's OpenEXR and Sony's OpenImageIO.
Both are great C++ projects and also provide bindings for Python, so I definitely recommend using them.

BUT maybe your package manager doesn't have a specific version and compiling them from scratch can be a long process that could get you stuck in many, many different & non well documented cmake issues.

If you only need to do something as trivial as reading the metadata of an EXR file and you don't need to do any image manipulation stuff, it's just not worth the hassle.
That's why I've written this very small python module (currently ~360 LOCs) that simply reads the header of an exr file, according to the official EXR documentation available here: https://www.openexr.com/documentation/openexrfilelayout.pdf

# Dependencies
pytest==4.2.0

# Tests
I'm not a TDD guy (yet) - so there are very few tests. I'm planning to write more of them as soon as I can breathe a little.
You can run tests by typing: `pytest` from the root dir of this repo.

# PR & Bugs
Fill free to submit Pull Requests if you notice anything wrong. I'm more than happy to merge them and adapt them to my coding style (which is just PEP8 stuff with some additional things like lowercase functions args in order to distinguish arguments from variables inside the scope of a function - very useful in my opinion and blog post coming soon).
