# 🎨 EditorConfig for C#

> Standardized formatting configuration for C# projects using K&R/Stroustrup style

[![EditorConfig](https://img.shields.io/badge/EditorConfig-Compatible-green.svg)](https://editorconfig.org/)
[![C#](https://img.shields.io/badge/Language-C%23-blue.svg)](https://docs.microsoft.com/en-us/dotnet/csharp/)

## 📋 About

This `.editorconfig` file provides consistent code formatting configuration for C# projects, following the K&R/Stroustrup style. It ensures that all project developers maintain the same formatting standards, regardless of the editor or IDE used.

## ✨ Features

### 🔧 Basic Settings
- **Indentation**: 4 spaces
- **Encoding**: UTF-8
- **Line ending**: CRLF (Windows)
- **Trailing whitespace removal**
- **Insert final newline**

### 🎯 Brace Style (K&R/Stroustrup)
```csharp
// ✅ Applied style
if (condition) {
    // code
} else {
    // code
}

try {
    // code
} catch (Exception ex) {
    // handling
} finally {
    // cleanup
}
```

### 📐 Spacing Rules
- **Binary operators**: Spaces before and after (`a + b`)
- **Assignment operators**: Spaces before and after (`x = y`)
- **Conditional operators**: Spaces before and after (`a ? b : c`)
- **Cast**: No space after cast (`(int)value`)
- **Control keywords**: Space after (`if (`, `for (`, `while (`)
- **Parentheses**: No internal spaces

### 🏗️ Indentation
- **Case content**: Indented
- **Switch labels**: Indented
- **Labels**: Left-aligned

## 🚀 How to Use

1. **Copy the `.editorconfig` file** to the root of your C# project
2. **Make sure** your editor supports EditorConfig:
   - ✅ Visual Studio
   - ✅ Visual Studio Code
   - ✅ JetBrains Rider
   - ✅ Vim/Neovim
   - ✅ Emacs
   - ✅ Sublime Text

3. **Restart** your editor if necessary

## 📁 Project Structure

```
project/
├── .editorconfig      # ← This file
├── src/
│   └── *.cs
└── tests/
    └── *.cs
```

## 🎨 Formatting Example

```csharp
using System;
using System.Collections.Generic;

namespace MyProject {
    public class MyClass {
        private readonly List<string> _items;
        
        public MyClass() {
            _items = new List<string>();
        }
        
        public void AddItem(string item) {
            if (string.IsNullOrEmpty(item)) {
                throw new ArgumentException("Item cannot be empty");
            }
            
            _items.Add(item);
        }
        
        public string ProcessItem(string item) {
            return item switch {
                null => "Null",
                "" => "Empty",
                _ => item.ToUpper()
            };
        }
    }
}
```

## ⚙️ Compatibility

|    Editor/IDE   | Native Support | Plugin Required |
|-----------------|----------------|-----------------|
| Visual Studio   |      Yes       |        No       |
| VS Code         |      Yes       |        No       |
| JetBrains Rider |      Yes       |        No       |
| Vim/Neovim      |      No        |        Yes      |
| Emacs           |      No        |        Yes      |
| Sublime Text    |      No        |        Yes      |

## 📚 Additional Resources

- [EditorConfig Official Site](https://editorconfig.org/)
- [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
- [.NET Code Style Rules](https://docs.microsoft.com/en-us/dotnet/fundamentals/code-analysis/style-rules/)

## 🤝 Contributing

Feel free to suggest improvements or adjustments to this configuration through issues or pull requests!

---

<div align="center">

**Written by Murillo Yonamine (Momodev)**

</div>

