# Requirements
Requirements to be a Nuclear Interactive scripter.

### Skill Requirements
- Experienced in Luau programming
- Knows how to use Visual Studio Code
- Knows how to use Git or/and GitHub
- Knows how to use the required Plugins and Extensions below
### Required Roblox Studio Plugins
- [Rojo](https://www.roblox.com/library/6415005344/Rojo-7)
- [Roblox LSP](https://www.roblox.com/library/5969291145/Roblox-LSP-Plugin)
### Required Visual Studio Code Extensions
- [Rojo](https://marketplace.visualstudio.com/items?itemName=evaera.vscode-rojo)
- [Roblox LSP](https://marketplace.visualstudio.com/items?itemName=Nightrains.robloxlsp)
- [StyLua](https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.stylua)
- [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)
### Required Command Line Tools
- [Wally](https://github.com/UpliftGames/wally)
### Scripting Layout
```lua
--[=[Services]=]--
local Players = game:GetService("Players")
--[=[Directories]=]--
local Packages = game.ReplicatedFirst.Packages
--[=[Packages]=]--
local Promise = require(Packages.Promise)
--[=[Utilities]=]--
local PromiseUtil = require(game.ReplicatedStorage.PromiseUtil)
--[=[Modules]=]--
local Config = require(game.ReplicatedStorage.Config)
--[=[Types]=]--
type Promise = typeof(Promise.new())
--[=[Utility functions]=]--
local function utilFunc()
    print("util func executed")
end
--[=[Main functions]=]--
local function MainFunc()
    utilFunc()
    print("main func executed")
end
--[=[Connections]=]--
workspace.ChildAdded:Connect(MainFunc)
--[=[Code]=]--
MainFunc()
print("Something")
```
This isn't enforced strictly but use this layout to an extent for readability.
