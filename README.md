local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
 
local Window = Rayfield:CreateWindow({
   Name = "Alex Universal Hub😎 BETA",
   Icon = 0,
   LoadingTitle = "Alex hub🔥",
   LoadingSubtitle = "by Alex Exploits",
   Theme = "Default",
   ToggleUIKeybind = "K",
   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false,
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil,
      FileName = "Alexhub"
   },
   Discord = {
      Enabled = true,
      Invite = "bteb9aAQ",
      RememberJoins = true
   },
   KeySystem = true,
   KeySettings = {
      Title = "Alex Universal Hub😎 | Key",
      Subtitle = "key in discord",
      Note = "discord: https://discord.gg/bteb9aAQ",
      FileName = "alexkey",
      SaveKey = true,
      GrabKeyFromSite = true,
      Key = {"https://pastebin.com/raw/NQX3GNsJ"}
   }
})
 
local MainTab = Window:CreateTab("🏠 Home", nil)
local MainSection = MainTab:CreateSection("Main")
 
local player = game.Players.LocalPlayer
local userInputService = game:GetService("UserInputService")
local jumpConnection
local jumpDebounce = false
 
local Toggle = MainTab:CreateToggle({
   Name = "Infinite Jump",
   CurrentValue = false,
   Callback = function(value)
      if value then
         jumpConnection = userInputService.JumpRequest:Connect(function()
            if not jumpDebounce then
               jumpDebounce = true
               if player.Character and player.Character:FindFirstChildOfClass("Humanoid") then
                  player.Character:FindFirstChildOfClass("Humanoid"):ChangeState(Enum.HumanoidStateType.Jumping)
               end
               wait()
               jumpDebounce = false
            end
         end)
      else
         if jumpConnection then
            jumpConnection:Disconnect()
            jumpConnection = nil
         end
      end
   end,
})
 
local WalkSpeedSlider = MainTab:CreateSlider({
   Name = "WalkSpeed",
   Range = {16, 200}, -- 16 is default
   Increment = 1,
   Suffix = "Speed",
   CurrentValue = 16,
   Flag = "WalkSpeedSlider",
   Callback = function(Value)
       game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = (Value)
   end,
})
 
local JumpPowerSlider = MainTab:CreateSlider({
   Name = "JumpPower",
   Range = {50, 250},
   Increment = 5,
   Suffix = "Power",
   CurrentValue = 50,
   Flag = "JumpPowerSlider",
   Callback = function(Value)
       game.Players.LocalPlayer.Character.Humanoid.JumpPower = (Value)
   end,
})
 
local MainSection = MainTab:CreateSection("Universal")
 
MainTab:CreateButton({
   Name = "Infinite Yield",
   Callback = function()
       loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source", true))()
   end,
})
 
MainTab:CreateButton({
   Name = "Chat filter bypass",
   Callback = function()
       loadstring(game:HttpGet("https://github.com/Synergy-Networks/products/raw/main/BetterBypasser/loader.lua"))()
   end,
})
 
local MainTab = Window:CreateTab("Fe Animations🕺", nil)
local MainSection = MainTab:CreateSection("Animations")
 
MainTab:CreateButton({
   Name = "Seraphic blade🗡",
   Callback = function()
       loadstring(game:HttpGet("https://pastefy.app/59mJGQGe/raw"))()
   end,
})
 
MainTab:CreateButton({
   Name = "Fe sussy animations🤨",
   Callback = function()
       loadstring(game:HttpGet("https://pastebin.com/raw/FWwdST5Y"))()
   end,
})
 
MainTab:CreateLabel("More Animations Coming Soon")
 
local MainTab = Window:CreateTab("Game scripts🎮")
local MainSection = MainTab:CreateSection("Games")
 
MainTab:CreateButton({
   Name = "Mm2🔪",
   Callback = function()
       loadstring(game:HttpGet('https://raw.githubusercontent.com/zdkjaime/Xhub/refs/heads/main/MainHub'))()
   end,
})
 
MainTab:CreateButton({
   Name = "Natural disasters🌪"
   Callback = function()
       loadstring(game:HttpGet("https://pastebin.com/raw/aZjaAr6F"))()
   end,
})
 
local Button = Tab:CreateButton({
   Name = "Grow a Garden🐝",
   Callback = function()
       
   end,
})
