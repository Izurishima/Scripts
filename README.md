# 🌊 Glass UI Script

Welcome to the official repository for **Glass UI**. This script is designed to be lightweight, fast, and easy to use.

---

## Example Script

local Library = loadstring(game:HttpGet("https://pastefy.app/fdr2zeMo"))()

-- 1. Create the main window
local Window = Library:CreateWindow({
    Name = "Glass UI | Version 1.0",
    IntroText = "Loading Glass UI...",
    ConfigFolder = "GlassConfig"
})

-- 2. Add a Tab
local MainTab = Window:CreateTab("General")

-- 3. Add a Section
local Section = MainTab:CreateSection("Main Features")

-- 4. Add a Button
Section:CreateButton({
    Name = "Destroy UI",
    Callback = function()
        Library:Close()
    end,
})

-- 5. Add a Toggle
Section:CreateToggle({
    Name = "Auto-Farm Test",
    CurrentValue = false,
    Flag = "Toggle1", -- Unique ID for this toggle
    Callback = function(Value)
        if Value then
            print("Auto-farm enabled!")
        else
            print("Auto-farm disabled!")
        end
    end,
})

-- 6. Send a notification to the user
Library:Notify({
    Title = "Success",
    Content = "Glass UI has loaded correctly!",
    Duration = 5
})
