# Glass UI Library

Welcome to the official repository for **Glass UI**.
(If you encounter an error please open a ticket in "Support" channel, https://discord.gg/4TsSsKCg6K )

---

## Add this to the top of the script
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Izurishima/GlassUI-Library/refs/heads/main/Glass%20UI%20Library"))()
```

## 1. Create the main window

```lua
local Window = Library:CreateWindow({
    Name = "Glass UI | Version 1.0",
    IntroText = "Loading Glass UI...",
    ConfigFolder = "GlassConfig"
})
```

## 2. Add a Tab

```lua
local MainTab = Window:CreateTab("General")
```

## 3. Add a Section

```lua
local Section = MainTab:CreateSection("Main Features")
```

## 4. Add a Button

```lua
Section:CreateButton({
    Name = "Destroy UI",
    Callback = function()
        Library:Close()
    end,
})
```

## 5. Add a Toggle

```lua
Section:CreateToggle({
    Name = "Toggle Test",
    CurrentValue = false,
    Flag = "Toggle1", -- Unique ID for this toggle
    Callback = function(Value)
        if Value then
            print("Toggle Enabled")
        else
            print("Toggle Disabled")
        end
    end,
})
```

## 6. Send a notification to the user

```lua
Library:Notify({
    Title = "Success",
    Content = "Glass UI has loaded correctly!",
    Duration = 5
})
```
