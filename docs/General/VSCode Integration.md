# VSCode Integration

NGT can be integrated into Visual Studio Code using the AngelScriptServer patched extension, which you can find [here](https://github.com/m1maker/NGTVSCodeExtension)

You can use autocomplete, code error checking, etc.
However, note that some features of the NGT preprocessor, such as automatically searching for include files near the NGT executable, or #include "include/*", will not work and VSCode will not include these files in the codebase.
Also, the property keyword is unfortunately not included.

You can try the add-on by downloading it [here](https://github.com/m1maker/NGTVSCodeExtension/releases/download/VPatched/angel-lsp-0.3.12.vsix)

## How to install

Open a command prompt and type:
```
code --install-extension angel-lsp-0.3.12.vsix
```

## Start Coding

First, you need to get a predefined engine configuration.
Run:
```
NGT -p
```

You will get an as.predefined file with NGT executable.
Now, in your projects, put this file in the root of the code base.
