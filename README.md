---- script byAegonaChannel


local Material = loadstring(game:HttpGet("https://raw.githubusercontent.com/NiceBBMBThai12/NBTScript/main/Gui%20Th%20Edit%20free%2001"))()

local XX =
    Material.Load(
    {
        Title = "<< AEGONA HUB >>",
        Style = 1,
        SizeX = 400,
        SizeY = 185,
        Theme = "Ben10"
    }
)


local Main =
    XX.New(
    {
        Title = "Auto Farm"
    }
)


local tel =
    XX.New(
    {
        Title = "-- Teleport --"
    }
)

local shop =
    XX.New(
    {
        Title = "-- SHOP --"
    }
)

local raid =
    XX.New(
    {
        Title = "-- RAID --"
    }
)
local setting =
    XX.New(
    {
        Title = "Setting"
    }
)

local D =
    Main.Toggle(
    {
        Text = "-- Auto Farm Box --",
        Callback = function(Value)
            _G.AutoFarm = Value
            while _G.AutoFarm do
             while  wait(0.1) do
    for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
    if v.Name == "TouchInterest" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame
        game.Players.LocalPlayer.Character.Humanoid.Health = 0
        wait(.1)
    end
        Enabled = false
end
end
end
end
    }
)

local blah =
    setting.Button(
    {
        Text = "Joim Maren",
        Callback = function(Value)

local args = {
    [1] = "SetTeam",
    [2] = "Marines"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

        end,
        Enabled = false
    }
)

local blah =
    setting.Button(
    {
        Text = "Joim Pirates",
        Callback = function(Value)

local args = {
    [1] = "SetTeam",
    [2] = "Pirates"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

        end,
        Enabled = false
    }
)

local blah =
    shop.Button(
    {
        Text = "RandomFruit",
        Callback = function(Value)
local args = {
    [1] = "Cousin",
    [2] = "Buy"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
 print("Random_fruit")
        Enabled = false
        end
        }
        )
        
        
        local blah =
    setting.Button(
    {
        Text = "Rejoin",
        Callback = function(Value)
local ts = game:GetService("TeleportService")
      local p = game:GetService("Players").LocalPlayer
ts:Teleport(game.PlaceId, p)
        end,
        Enabled = false
        }
        )
        
        
       local blah =
    raid.Toggle(
    {
        Text = "--> Kill Aura <--",
        Callback = function(Value)
            _G.Autokillaura = Value
            while _G.Autokillaura do
                wait(0.60)
for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
    if v.ClassName == "Model" then
        v.Humanoid.Health = die
    end
    end
        Enabled = false
            end
    end
    }
) 


       local blah =
    raid.Toggle(
    {
        Text = "--> Auto Awakener <--",
        Callback = function(Value)
            _G.Autoawak = Value
            while _G.Autoawak do
                wait(0.60)
local args = {
    [1] = "Awakener",
    [2] = "Check"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        Enabled = false
            end
    end
    }
) 

local blah =
    tel.Button(
    {
        Text = "--> Cafa <--",
        Callback = function(Value)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-385.7210693359375, 73.0458755493164, 299.86419677734375)
wait(.1)
game.Players.LocalPlayer.Character.Humanoid.Health = 0
wait(.1)
local string_1 = "SetSpawnPoint";
								local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
								Target:InvokeServer(string_1);
                    Enabled = false
            end
    }
) 

local blah =
    tel.Button(
    {
        Text = "--> Raid <--",
        Callback = function(Value)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-6450.818359375, 249.55406188964844, -4494.82861328125)
wait(.1)
game.Players.LocalPlayer.Character.Humanoid.Health = 0
wait(.1)
local string_1 = "SetSpawnPoint";
								local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
								Target:InvokeServer(string_1);
                    Enabled = false
            end
    }
) 

local blah =
    setting.Button(
    {
        Text = "--> INVENTORY FRUIT <--",
        Callback = function(Value)
local args = {
    [1] = "getInventoryFruits"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

                    Enabled = false
            end
    }
) 
local blah =
    setting.Button(
    {
        Text = "--> INVENTORY WEAPONS <--",
        Callback = function(Value)
local args = {
    [1] = "getInventoryWeapons"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

                    Enabled = false
            end
    }
) 

local blah =
    setting.Button(
    {
        Text = "--> SHOP FRUIT <--",
        Callback = function(Value)
local args = {
    [1] = "GetFruits",
    [2] = false
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

                    end,
                    Enabled = false
    }
) 

local blah =
    raid.Button(
    {
        Text = "--> Buy Chip Humanbuddha <--",
        Callback = function(Value)
local args = {
    [1] = "RaidsNpc",
    [2] = "Select",
    [3] = "Human: Buddha"
}

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

        end,
        Enabled = false
    }
)

local blah =
    Main.Toggle(
    {
        Text = "Auto Haki Beta",
        Callback = function(Value)
            _G.AutoHaki = Value
            while _G.AutoHaki do
local args = {
    [1] = "Buso"
}
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end
        end,
        Enabled = false
    }
)



    
     
      
     
         
 

						
								

            
  
    

