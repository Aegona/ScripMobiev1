---- script byAegonaChannel

local ToggleAEGONA = Instance.new("ScreenGui")
local ToogleA = Instance.new("TextButton")
local UICorner = Instance.new("UICorner")

ToggleAEGONA.Name = "ToggleAEGONA"
ToggleAEGONA.Parent = game.CoreGui
ToggleAEGONA.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ToogleA.Name = "ToogleA"
ToogleA.Parent = ToggleAEGONA
ToogleA.BackgroundColor3 = Color3.fromRGB(62, 147, 9)
ToogleA.Position = UDim2.new(0.194303796, 0, 0.480566978, 0)
ToogleA.Size = UDim2.new(0, 88, 0, 45)
ToogleA.Font = Enum.Font.Ubuntu
ToogleA.Text = "AEGONAHUB"
ToogleA.TextColor3 = Color3.fromRGB(0, 0, 0)
ToogleA.TextScaled = true
ToogleA.TextSize = 14.000
ToogleA.TextWrapped = true
ToogleA.MouseButton1Click:Connect(function()
	game.CoreGui:FindFirstChild("z AEGONA X HUB z").Enabled = not  game.CoreGui:FindFirstChild("z AEGONA X HUB z").Enabled
end)

UICorner.Parent = ToogleA


function CheckQuest()
   local Lv =  game.Players.LocalPlayer.Data.Level.Value
   if Lv == 1 or Lv <= 9 then
       Ms = "Bandit [Lv. 5]"
       CQ = CFrame.new(1059.838623046875, 16.516624450683594, 1545.941162109375)
       CM = CFrame.new(1177.2108154296875, 16.43285369873047, 1616.587646484375)
       NQ = "BanditQuest1"
       NM = "Bandit"
       LQ = 1
   elseif Lv == 10 or Lv <= 14 then
       Ms = "Monkey [Lv. 14]"
       CQ = CFrame.new(-1601.58642578125, 36.852134704589844, 153.4748077392578)
       CM = CFrame.new(-1447.85400390625, 22.852529525756836, 224.74119567871094)
       NQ = "JungleQuest"
       NM = "Monkey"
       LQ = 1
            elseif Lv == 15 or Lv <= 29 then
       Ms = "Gorilla [Lv. 20]"
       CQ = CFrame.new(-1601.58642578125, 36.852134704589844, 153.4748077392578)
       CM = CFrame.new(-1226.2562255859375, 6.279374599456787, -490.89447021484375)
       NQ = "JungleQuest"
       NM = "Gorilla"
       LQ = 2
        elseif Lv == 30 or Lv <= 2298 then
       Ms = "Pirate [Lv. 35]"
       CQ = CFrame.new(-1139.8831787109375, 4.752061367034912, 3824.586181640625)
       CM = CFrame.new(-1210.2435302734375, 4.752061367034912, 3918.926513671875)
       NQ = "BuggyQuest1"
       NM = "Pirate"
       LQ = 1
               elseif Lv == 2299 or Lv <= 2300 then
       Ms = "Head Baker [Lv. 2275]"
       CQ = CFrame.new(-1924.693115234375, 37.82392501831055, -12850.0869140625)
       CM = CFrame.new(-2217.271484375, 53.528297424316406, -12865.2177734375)
       NQ = "CakeQuest2"
       NM = "Head Baker"
       LQ = 2
    end
end
















local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/zxciaz/VenyxUI/main/Reuploaded"))() --someone reuploaded it so I put it in place of the original back up so guy can get free credit.
local venyx = library.new("z AEGONA X HUB z", 5013109572)

-- themes
local themes = {
Background = Color3.fromRGB(24, 24, 24),
Glow = Color3.fromRGB(0, 0, 0),
Accent = Color3.fromRGB(10, 10, 10),
LightContrast = Color3.fromRGB(20, 20, 20),
DarkContrast = Color3.fromRGB(14, 14, 14),  
TextColor = Color3.fromRGB(255, 255, 255)
}


local page = venyx:addPage("Main", 5012544693)
local point = venyx:addPage("POINT", 5012544693)
local section1 = page:addSection("Section 1")
local section2 = page:addSection("Section 2")
local point2 = point:addSection("-- POINT --")

section1:addToggle("AutoFarm", nil, function(value)
_G.Farm = true
wait(.1)
if focusLost then
venyx:Notify("AutoFarm = True ", value)
end
end)

section1:addButton("FIX Delete AutoFarm", function()
_G.Farm = false
wait(.1)
game.Players.LocalPlayer.Character.Humanoid.Health = die
end)

section1:addToggle("BringMob", nil, function(value)
_G.BringMob = true
wait(.1)
if focusLost then
venyx:Notify("BringMob = True ", value)
end
end)

section1:addToggle("FastAttck", nil, function(value)
local CombatFramework = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
Camera:Stop()
coroutine.wrap(function()
    game:GetService("RunService").Stepped:Connect(function()
        if getupvalues(CombatFramework)[2]['activeController'].timeToNextAttack then
            getupvalues(CombatFramework)[2]['activeController'].timeToNextAttack = 0
            getupvalues(CombatFramework)[2]['activeController'].hitboxMagnitude = 60
            getupvalues(CombatFramework)[2]['activeController']:attack()
        end
    end)
end)()
end)


point2:addToggle("MELEE", nil, function(value)
    while true do wait()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee",1)
end
end)

point2:addToggle("DEFENSE", nil, function(value)
    while true do wait()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",1)
end
end)

point2:addToggle("Sword", nil, function(value)
    while true do wait()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword",1)
end
end)


section2:addToggle("AutoSetSpawn", nil, function(value)
    while wait(3) do
local string_1 = "SetSpawnPoint";
								local Target = game:GetService("ReplicatedStorage").Remotes["CommF_"];
								Target:InvokeServer(string_1);
end
end)












CheckQuest()

function TP(P)
    NoClip = true
    Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 10 then
        Speed = 1000
    elseif Distance < 170 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = P
        Speed = 400
    elseif Distance < 1000 then
        Speed = 400
    elseif Distance >= 1000 then
        Speed = 300
    end
    game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P}
    ):Play()
    NoClip = false
end

spawn(function()
    while task.wait() do
        if _G.Farm then
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                TP(CQ)
                wait(3)
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NQ,LQ)
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if v.Name == Ms then
                        repeat task.wait()
                        TP(v.HumanoidRootPart.CFrame * CFrame.new(0,20,0))
                        until not _G.Farm
                        end
                    end
                end
            end    
        end
    end
end)

spawn(function()
    pcall(function()
        while task.wait() do
            if _G.Farm then
                if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000,100000,100000)
                    Noclip.Velocity = Vector3.new(0,0,0)
                end
            else
                if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                end
            end
        end
    end)
end)



spawn(function()
    while task.wait() do
        if _G.Farm then
        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
            if v.Name == Ms then
                v.HumanoidRootPart.CFrame = CM
                v.HumanoidRootPart.CanCollide = false
                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                end
            end
        end
    end
end)



             while _G.BringMob do wait()
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                 for i2,v2 in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                    if v.Name == MON and v2.Name == MON then
                        v2.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
                        v2.HumanoidRootPart.CanCollide = false
                           game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * Method
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                    end
                 end
            end
             end
