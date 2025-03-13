# Rider Dark Theme for Neovim (Based on Mofiqul/vscode.nvim)

This is a customized version of the **[Mofiqul/vscode.nvim](https://github.com/Mofiqul/vscode.nvim)** theme for Neovim.  
The goal is to make it look **closer to JetBrains Rider Dark** while keeping the original **VS Code** style.

## 🎨 Features
- 🔹 **Variables** (`@variable`) in a softer **gray**
- 🔹 **Member variables** (`@variable.member`) in **cyan**
- 🔹 **Function parameters** (`@variable.parameter`) in **pink**
- 🔹 **Methods** (`@function.method`) in **green**
- 🔹 **Control flow keywords** (`if`, `else`, `switch`, `for`, `while`) in **blue**
- 🔹 **Classes** (`@lsp.type.class`) in **purple**
- 🔹 **Numbers** (`@number`) in **pink**
- 🔹 **Comments** in **soft green** and italic

## 📷 Preview

![Rider Dark Theme Preview](https://i.imgur.com/letjTBR.png)

## 📥 Installation

### **Using LazyVim**
Add this to your **`nvim/lua/plugins/colorscheme.lua`**:

```lua
return {
	{
		"Mofiqul/vscode.nvim",
		lazy = false,
		priority = 1000,
		opts = {
			style = "dark",
			group_overrides = {

				-- This re-color is based on Mofiqul/vscode
				-- Just a small recoloring to make it look like JetBrains Rider Dark

				-- Variables
				["@variable"] = { fg = "#bdbdbd" },
				["@variable.c_sharp"] = { link = "@variable" },
				["@variable.member.c_sharp"] = { fg = "#65c3cc" },
				["@variable.parameter"] = { fg = "#ed8796" },
				["@variable.parameter.c_sharp"] = { link = "@variable.parameter" },

				["@keyword.repeat"] = { fg = "#6c95eb", bold = true },
				["@keyword.repeat.c_sharp"] = { link = "@keyword.repeat" },

				-- Boolean
				["@boolean"] = { fg = "#6c95eb", italic = true },
				["@boolean.c_sharp"] = { link = "@boolean" },

				-- Return
				["@keyword.return"] = { fg = "#6c95eb" },
				["@keyword.return.c_sharp"] = { link = "@keyword.return" },

				-- Method
				["@function.method"] = { fg = "#38c596", bold = true },
				["@function.method.call"] = { link = "@function.method" },
				["@function.method.call.c_sharp"] = { link = "@function.method" },

				-- Types (mots clés)
				["@keyword"] = { fg = "#6c95eb", italic = false },
				["@keyword.conditional"] = { fg = "#6c95eb", italic = false },
				["@keyword.conditional.c_sharp"] = { link = "@keyword.conditional" },

				-- Classes
				["@lsp.type.class.cs"] = { fg = "#c191ff", bold = true },

				-- Number
				["@number"] = { fg = "#e791bc", bold = true },
				["@number.c_sharp"] = { link = "@number" },

				-- Comment
				["Comment"] = { fg = "#84c26b", italic = true },
			},
		},
	},
}
```

