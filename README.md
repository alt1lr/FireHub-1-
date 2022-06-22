game:GetService("StarterGui"):SetCore("SendNotification", { 
	Title = "Fire Hub V0.2";
	Text = "By Fire alt1lr#9459";
	Icon = "rbxthumb://type=Asset&id=9950668390&w=150&h=150"})
Duration = 3;
wait(0.1)
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local Window = Library.CreateLib("Fire Hub [1]", "BloodTheme")

local Tab1 = Window:NewTab("Scripts")
local Tab1Section = Tab1:NewSection("Script")

local Tab2 = Window:NewTab("Natural Disaster")
local Tab2Section = Tab2:NewSection("Natural Disaster")

local Tab3 = Window:NewTab("Build The Boat")
local Tab3Section = Tab3:NewSection(" Build The Boat")

local Tab5 = Window:NewTab("Tower Of Misery")
local Tab5Section = Tab5:NewSection(" Tower Of Misery")

Tab1Section:NewToggle("Auto Jump", "ToggleInfo", function(state)
    if state then
        while true do wait(0.000001)
game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping") 
wait(1)
end
    else
        game.Players.LocalPlayer.Character:Destroy()
    end
end)

Tab1Section:NewButton("Fly V3", "", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/RPv4GELs"))()
end)

Tab1Section:NewButton("Yeet Troll Face Edition", "ButtonInfo", function()
-- I DONT OWN THIS SCRIPT

local lp = game:FindService("Players").LocalPlayer

local function gplr(String)
	local Found = {}
	local strl = String:lower()
	if strl == "all" then
		for i,v in pairs(game:FindService("Players"):GetPlayers()) do
			table.insert(Found,v)
		end
	elseif strl == "others" then
		for i,v in pairs(game:FindService("Players"):GetPlayers()) do
			if v.Name ~= lp.Name then
				table.insert(Found,v)
			end
		end 
	elseif strl == "me" then
		for i,v in pairs(game:FindService("Players"):GetPlayers()) do
			if v.Name == lp.Name then
				table.insert(Found,v)
			end
		end 
	else
		for i,v in pairs(game:FindService("Players"):GetPlayers()) do
			if v.Name:lower():sub(1, #String) == String:lower() then
				table.insert(Found,v)
			end
		end 
	end
	return Found 
end

local function notif(str,dur)
	game:FindService("StarterGui"):SetCore("SendNotification", {
		Title = "yeet gui",
		Text = str,
		Icon = "rbxassetid://2005276185",
		Duration = dur or 3
	})
end

--// sds

local h = Instance.new("ScreenGui")
local Main = Instance.new("ImageLabel")
local Top = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local TextBox = Instance.new("TextBox")
local TextButton = Instance.new("TextButton")

h.Name = "h"
h.Parent = game:GetService("CoreGui")
h.ResetOnSpawn = false

Main.Name = "Main"
Main.Parent = h
Main.Active = true
Main.Draggable = true
Main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Main.BorderSizePixel = 0
Main.Position = UDim2.new(0.174545452, 0, 0.459574461, 0)
Main.Size = UDim2.new(0, 454, 0, 218)
Main.Image = "rbxassetid://2005276185"

Top.Name = "Top"
Top.Parent = Main
Top.BackgroundColor3 = Color3.fromRGB(57, 57, 57)
Top.BorderSizePixel = 0
Top.Size = UDim2.new(0, 454, 0, 44)

Title.Name = "Title"
Title.Parent = Top
Title.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
Title.BorderSizePixel = 0
Title.Position = UDim2.new(0, 0, 0.295454562, 0)
Title.Size = UDim2.new(0, 454, 0, 30)
Title.Font = Enum.Font.SourceSans
Title.Text = "FE Yeet Gui (trollface edition)"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true
Title.TextSize = 14.000
Title.TextWrapped = true

TextBox.Parent = Main
TextBox.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
TextBox.BorderSizePixel = 0
TextBox.Position = UDim2.new(0.0704845786, 0, 0.270642221, 0)
TextBox.Size = UDim2.new(0, 388, 0, 62)
TextBox.Font = Enum.Font.SourceSans
TextBox.PlaceholderText = "Who do i destroy(can be shortened)"
TextBox.Text = ""
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.TextScaled = true
TextBox.TextSize = 14.000
TextBox.TextWrapped = true

TextButton.Parent = Main
TextButton.BackgroundColor3 = Color3.fromRGB(49, 49, 49)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0.10352423, 0, 0.596330225, 0)
TextButton.Size = UDim2.new(0, 359, 0, 50)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "Cheese em'"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextWrapped = true

TextButton.MouseButton1Click:Connect(function()
	local Target = gplr(TextBox.Text)
	if Target[1] then
		Target = Target[1]
		
		local Thrust = Instance.new('BodyThrust', lp.Character.HumanoidRootPart)
		Thrust.Force = Vector3.new(9999,9999,9999)
		Thrust.Name = "YeetForce"
		repeat
			lp.Character.HumanoidRootPart.CFrame = Target.Character.HumanoidRootPart.CFrame
			Thrust.Location = Target.Character.HumanoidRootPart.Position
			game:FindService("RunService").Heartbeat:wait()
		until not Target.Character:FindFirstChild("Head")
	else
		notif("Invalid player")
	end
end)
end)

Tab1Section:NewButton("Speed Tool", "ButtonInfo", function()
--Made By Raspyredstoner
mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Speed Tool"
tool.Activated:connect(function()
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)

Tab1Section:NewButton("Infinite Jump", "", function()
    local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
end)

Tab1Section:NewButton("ShiftLock", "", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/WQ9NPeDS'))();
end)

Tab1Section:NewButton("Wall Walking", "", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/zXk4Rq2r"))()
end)

Tab1Section:NewButton("Full Brightness", "", function()
    game:GetService("Lighting").Brightness = 2
game:GetService("Lighting").ClockTime = 14
game:GetService("Lighting").FogEnd = 100000
game:GetService("Lighting").GlobalShadows = false
game:GetService("Lighting").OutdoorAmbient = Color3.fromRGB(128, 128, 128)
end)

Tab1Section:NewButton("Steal Player Inventory", "", function()
    for i,v in pairs (gamePlayers:GetChildren()) do
wait()
for i,b in pairs (vBackpack:GetChildren()) do
bParent = gamePlayersLocalPlayerBackpack
end
end
end)

Tab1Section:NewButton("Chat Translator", "", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/YourLocalNzi/Language-translator-/main/Language%20translator", true))()
end)

Tab1Section:NewButton("Annoy Player", "", function()
    loadstring(game:HttpGet("https://pastebin.com/raw/1cHdCvTF"))()
end)

Tab1Section:NewButton("Keyboard", "", function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/manimcool21/Keyboard-FE/main/Protected%20(3).lua'),true))()
local KeyboardguiWarriorRoberrVersion = Instance.new("ScreenGui")
local Drag = Instance.new("Frame")
local Close = Instance.new("TextButton")


KeyboardguiWarriorRoberrVersion.Name = "Keyboard gui WarriorRoberr Version"
KeyboardguiWarriorRoberrVersion.Parent = game.CoreGui
KeyboardguiWarriorRoberrVersion.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Drag.Name = "Drag"
Drag.Parent = KeyboardguiWarriorRoberrVersion
Drag.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Drag.BorderSizePixel = 0
Drag.Position = UDim2.new(0.147916675, 0, 0.0593749993, 0)
Drag.Size = UDim2.new(0, 270, 0, 30)
Drag.Active = true
Drag.Draggable = true

Close.Name = "Close"
Close.Parent = Drag
Close.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Close.BorderSizePixel = 0
Close.Position = UDim2.new(0.999839723, 0, -0.00729167089, 0)
Close.Size = UDim2.new(0, 30, 0, 30)
Close.Font = Enum.Font.SourceSans
Close.Text = "X"
Close.TextColor3 = Color3.fromRGB(255, 255, 255)
Close.TextSize = 35.000
Close.MouseButton1Click:Connect(function()
	KeyboardguiWarriorRoberrVersion:Destroy()
end)
game.CoreGui["BUNB0yBUN BOARD"].KeyBoard.Parent = Drag
game.CoreGui["BUNB0yBUN BOARD"]:Destroy()
game.CoreGui["Keyboard gui WarriorRoberr Version"].Drag.KeyBoard.Bunb0ybun.Text = "MADE BY WARRIORROBERR BETTER VERSION "
game.CoreGui["Keyboard gui WarriorRoberr Version"].Drag.KeyBoard.Position = UDim2.new(0, 0, 0, 35)
game.CoreGui["Keyboard gui WarriorRoberr Version"].Drag.KeyBoard.Bunb0ybun.TextSize = 10
end)

Tab1Section:NewButton("Teleport Tool", "Hello", function()
    mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Click Teleport"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)

Tab2Section:NewButton("Teleport to Game", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-125, 48, 10)
end)

Tab2Section:NewButton("Teleport to Lobby", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-245, 180, 325)
end)

Tab2Section:NewButton("No Fall Damage", "Hello", function()
game.Players.LocalPlayer.Character.FallDamageScript:Destroy()
end)

Tab2Section:NewButton("Enable Ballon Mode", "Hello", function()
    workspace.Gravity = 60
end)

Tab2Section:NewButton("Disable Ballon Mode", "Hello", function()
    workspace.Gravity = 200
    end)

Tab2Section:NewButton("Auto Farm", "Hello", function()
while true do wait()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-248, 180, 290)
end
end)

Tab2Section:NewButton("UnAuto Farm", "Hello", function()
    game.Players.LocalPlayer.Character:Destroy()
game.Players.LocalPlayer.Character.Script:Destroy()
end)

Tab3Section:NewButton("Teleport to Library", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(180, -11, 1159)
wait(1)
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(240, -11, 1156)
end)

Tab3Section:NewButton("Library Password Books", "Hello", function()
local CoreGui = game:GetService("StarterGui")

CoreGui:SetCore("SendNotification", {
    Title = "Books Password",
    Text = "Yello,Red,Pink,Cyan,LightGreen",
    Duration = 10,
})

end)

Tab3Section:NewButton("Teleport to End", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-55, -360, 9478)
end)

Tab3Section:NewButton("Auto Farm", "Hello", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/nucy5Uw8'))();
end)
    

local Tab3Section = Tab3:NewSection("Teleport to Teams")

Tab3Section:NewButton("White Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-42, -9, -614)
end)

Tab3Section:NewButton("Black Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-576, -9, -122)
end)

Tab3Section:NewButton("Red Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(479, -9, -54)
end)

Tab3Section:NewButton("Green team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-596, -9, 302)
end)

Tab3Section:NewButton("Blue Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(474, -9, 293)
end)

Tab3Section:NewButton("Magenta Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(469, -9, 617)
end)

Tab3Section:NewButton("Yellow Team", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-586, -9, 652)
end)

local Tab4 = Window:NewTab("Lumber Tycoon 2")
local Tab4Section = Tab4:NewSection("RedGhost")

Tab4Section:NewButton("Dupe Axe", "Hello", function()
local plr = game:service'Players'.LocalPlayer

function SafeRespawn()
    plr.Character.Head:Destroy()
end

function Dupe()
    SafeRespawn()
    for i,v in pairs(plr.Backpack:GetChildren()) do
        if v.Name == "Tool" then
            game:GetService("ReplicatedStorage").Interaction.ClientInteracted:FireServer(v,"Drop tool",plr.Character.Torso.CFrame * CFrame.new(0,5,0))
        end
    end
end
Dupe()
end)

Tab4Section:NewButton("Dupe Money", "Hello", function()
    loadstring(game:HttpGet('https://pastebin.com/raw/Duy5Lqyk'))();
end)

Tab4Section:NewButton("Free Land", "Hello", function()
    for a,b in pairs(workspace.Properties:GetChildren()) do 
    if b:FindFirstChild("Owner") and b:FindFirstChild("OriginSquare") and b.Owner.Value == nil then 
        game.ReplicatedStorage.PropertyPurchasing.ClientPurchasedProperty:FireServer(b, b.OriginSquare.OriginCFrame.Value.p + Vector3.new(0,3,0))
 wait(0.5)
        Instance.new('RemoteEvent', game:service'ReplicatedStorage'.Interaction).Name = "Ban"
	for i,v in pairs(game.Workspace.Properties:GetChildren()) do
		if v.Owner.Value == game.Players.LocalPlayer then
    game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.OriginSquare.CFrame + Vector3.new(0,10,0)
    game.Players.LocalPlayer.Character.Humanoid.Jump = true
    wait(0.1)
		end
	end
    end
end
end)

Tab4Section:NewButton("Max Land", "Hello", function()
    for i, v in pairs(game:GetService("Workspace").Properties:GetChildren()) do
        if v:FindFirstChild("Owner") and v.Owner.Value == game.Players.LocalPlayer then
            base = v
            square = v.OriginSquare
            end
        end
    function makebase(pos)
        local Event = game:GetService("ReplicatedStorage").PropertyPurchasing.ClientExpandedProperty
        Event:FireServer(base, pos)
        end
    local spos = square.Position
    makebase(CFrame.new(spos.X + 40, spos.Y, spos.Z))
    makebase(CFrame.new(spos.X - 40, spos.Y, spos.Z))
    makebase(CFrame.new(spos.X, spos.Y, spos.Z + 40))
    makebase(CFrame.new(spos.X, spos.Y, spos.Z - 40))
    makebase(CFrame.new(spos.X + 40, spos.Y, spos.Z + 40))
    makebase(CFrame.new(spos.X + 40, spos.Y, spos.Z - 40))
    makebase(CFrame.new(spos.X - 40, spos.Y, spos.Z + 40))
    makebase(CFrame.new(spos.X - 40, spos.Y, spos.Z - 40))
    makebase(CFrame.new(spos.X + 80, spos.Y, spos.Z))
    makebase(CFrame.new(spos.X - 80, spos.Y, spos.Z))
    makebase(CFrame.new(spos.X, spos.Y, spos.Z + 80))
    makebase(CFrame.new(spos.X, spos.Y, spos.Z - 80))
--Corners--
    makebase(CFrame.new(spos.X + 80, spos.Y, spos.Z + 80))
    makebase(CFrame.new(spos.X + 80, spos.Y, spos.Z - 80))
    makebase(CFrame.new(spos.X - 80, spos.Y, spos.Z + 80))
    makebase(CFrame.new(spos.X - 80, spos.Y, spos.Z - 80))

    makebase(CFrame.new(spos.X + 40, spos.Y, spos.Z + 80))
    makebase(CFrame.new(spos.X - 40, spos.Y, spos.Z + 80))
    makebase(CFrame.new(spos.X + 80, spos.Y, spos.Z + 40))
    makebase(CFrame.new(spos.X + 80, spos.Y, spos.Z - 40))
    makebase(CFrame.new(spos.X - 80, spos.Y, spos.Z + 40))
    makebase(CFrame.new(spos.X - 80, spos.Y, spos.Z - 40))
    makebase(CFrame.new(spos.X + 40, spos.Y, spos.Z - 80))
    makebase(CFrame.new(spos.X - 40, spos.Y, spos.Z - 80))
end)

local Tab4Section = Tab4:NewSection("Teleport to Places")

Tab4Section:NewButton("Spawn", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(153, 3, 61)
end)

Tab4Section:NewButton("Volcano", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-1567, 623, 1085)
end)

Tab4Section:NewButton("Cave", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(3573, -181, 431)
end)

Tab4Section:NewButton("Links Logic", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(4607, 7, -798)
end)

Tab4Section:NewButton("Fancy Furnishings", "Hello", function()
    game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(491, 3, -1720)
end)

Tab4Section:NewButton("Swamp", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-1209, 132, -801)
end)

Tab4Section:NewButton("Palm Island", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(2549, -6, -42)
end)

Tab4Section:NewButton("Bobs Shack", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(237, 8, -2538)
end)

Tab4Section:NewButton("Shrine Of Sight", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-1605, 195, 926)
end)

Tab4Section:NewButton("Boxed Cars", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(509, 3, -1463)
end)

Tab4Section:NewButton("Dock", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(1134, -1, -206)
end)

Tab4Section:NewButton("Bridge", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(113, 11, -977)
end)

Tab4Section:NewButton("Fine Arts Shop", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(5212, -166, 720)
end)

Tab4Section:NewButton("Strange Man", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(1068, 17, 1138)
end)

Tab4Section:NewButton("End Times", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(113, -213, -951)
end)

Tab4Section:NewButton("Snow Island", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(1445, 412, 3202)
end)


Tab5Section:NewButton("Anti Cheat Bypass", "Hello", function()
local CoreGui = game:GetService("StarterGui")

CoreGui:SetCore("SendNotification", {
    Title = "Anti Cheat Bypass",
    Text = "Loading....",
    Duration = 10,
})
wait(3.5)
local CoreGui = game:GetService("StarterGui")

CoreGui:SetCore("SendNotification", {
    Title = "Anti Cheat Bypass",
    Text = "Successful!",
    Duration = 10,
})
wait()
for a,b in pairs(getgc()) do if typeof(b) == 'function' then if debug.getinfo(b).name == 'kick' then
hookfunction(debug.getinfo(b).func,

function()
print'game tried to kick'
end) end end end
print'anticheat bypassed'
end)

Tab5Section:NewButton("Teleport To Top", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-110, 254, 49)
end)

Tab5Section:NewButton("Teleport to Start", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-21, -11, 48)
end)

Tab5Section:NewButton("Auto Win", "Hello", function()
while true do wait()
    game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-118, 255, 49)
end
end)

Tab5Section:NewButton("Disable Auto Win", "Hello", function()
    game.Players.LocalPlayer.Character:Destroy()
game.Players.LocalPlayer.Character.Script:Destroy()
end)

local Tab6 = Window:NewTab("Area51")
local Tab6Section = Tab6:NewSection(" Area 51")

local Tab7 = Window:NewTab("Big Brain Simulator 🤓")
local Tab7Section = Tab7:NewSection(" Big Brain Simulator")

local Tab8 = Window:NewTab("SuperNaturalSimulator")
local Tab8Section = Tab8:NewSection(" Super Natural Simulator ")

local Tab9 = Window:NewTab("Ninja Legends")
local Tab9Section = Tab9:NewSection(" Ninja Legends ")

local Tab10 = Window:NewTab("Other Gui")
local Tab10Section = Tab10:NewSection("Credits In Fire Hub [2]")

Tab6Section:NewButton("Pack A Punch", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(278, 323, 785)
end)

Tab6Section:NewButton("Execution Room [Enside]", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(30.9760799407959, 313.500244140625, 204.16676330566406)
end)

Tab6Section:NewButton("Execution Room [Outside]", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(38.9072265625, 313.4998779296875, 203.27430725097656)
end)

Tab6Section:NewButton("Sewer", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(63.21028137207031, 271.7001953125, 206.32199096679688)
end)

Tab6Section:NewButton("Under Ground", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(279.2727355957031, 259.6999206542969, 356.2850646972656)
end)

Tab6Section:NewButton("Ammo", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(186.50311279296875, 313.5, 395.2683410644531)
end)

Tab6Section:NewButton("Lab", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-48.30491256713867, 303.49969482421875, 573.6751098632812)
end)

Tab6Section:NewButton("Armory", "", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-169.04812622070312, 293.5002136230469, 316.7572937011719)
end)

Tab6Section:NewButton("Gets All Guns", "ButtonInfo", function()
run = not run
--Bring Part
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Hitbox" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait(1)
--tp part ps
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Hitbox" then
         	child.CFrame = CFrame.new(472, 551, 427)
		end
  	end
end)

Tab6Section:NewButton("Become Monster", "", function ()
run = not run
--Bring Part
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "TheButton" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait(1)
--tp part ps
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "TheButton" then
         	child.CFrame = CFrame.new(401, 509.7, 392)
		end
  	end
end)

Tab6Section:NewButton("Get Ammo", "", function()
run = not run
--Bring Part
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Box" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait(0.5)
--tp part ps
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Box" then
         	child.CFrame = CFrame.new(184, 311, 437)
		end
  	end
end)

Tab6Section:NewButton("Get All Papers", "", function()
run = not run
--Bring Part
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Paper" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait(1)
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "Paper" then
         	child.CFrame = CFrame.new(408, 551, 404)
		end
  	end
end)

Tab6Section:NewButton("Remove Fog", "Hello", function ()
    for i,v in pairs(game.Lighting:GetChildren()) do
			if v:IsA("Script") == false and v:IsA("LocalScript") == false then
				v:remove()
		end
	end
while true and wait() do
game.Lighting.FogEnd = math.huge
		game.Lighting.FogStart = 0
		
		game.Lighting.ClockTime=12
	game.Lighting.Brightness = 2
		game.Lighting.Ambient = Color3.fromRGB(167, 167, 167)
		game.Lighting.OutdoorAmbient = Color3.fromRGB(167, 167, 167)
end
end)

Tab7Section:NewButton("Auto Read", "Hello", function()
local range = 1000

local player = game:GetService("Players").LocalPlayer

game:GetService("RunService").RenderStepped:Connect(function()
    local p = game.Players:GetPlayers()
    for i = 2, #p do local v = p[i].Character
        if v and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v:FindFirstChild("HumanoidRootPart") and player:DistanceFromCharacter(v.HumanoidRootPart.Position) <= range then
            local tool = player.Character and player.Character:FindFirstChildOfClass("Tool")
            if tool and tool:FindFirstChild("Handle") then
                tool:Activate()
                for i,v in next, v:GetChildren() do
                    if v:IsA("BasePart") then
                        firetouchinterest(tool.Handle,v,0)
                        firetouchinterest(tool.Handle,v,1)
                    end
                end
            end
        end
    end
end)
end)
    
Tab7Section:NewButton("Teleport to Sell", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-55, 3, -46)
end)

Tab7Section:NewButton("Unlock all Gamepasses", "Hello", function()
game:GetService("Players").LocalPlayer.Gamepasses["2xCoins"].Value = true
game:GetService("Players").LocalPlayer.Gamepasses.Running.Value = true
game:GetService("Players").LocalPlayer.Gamepasses.FastReading.Value = true
game:GetService("Players").LocalPlayer.Gamepasses.Balloon.Value = true
game:GetService("Players").LocalPlayer.Gamepasses.DoubleJump.Value = true
game:GetService("Players").LocalPlayer.Gamepasses.InfiniteBrainCapacity.Value = true
end)

Tab7Section:NewButton("Unlock All Portals", "Hello", function()
game:GetService("Players")["LocalPlayer"].Portals.PeacefulFields.Value = true
game:GetService("Players")["LocalPlayer"].Portals.SnowySnow.Value = true
game:GetService("Players")["LocalPlayer"].Portals.Dunes.Value = true
game:GetService("Players")["LocalPlayer"].Portals.FloatingRock.Value = true
game:GetService("Players")["LocalPlayer"].Portals.SpaceBubble.Value = true
game:GetService("Players")["LocalPlayer"].Portals.Mars.Value = true
game:GetService("Players")["LocalPlayer"].Portals.Moon.Value = true
end)

local Tab7Section = Tab7:NewSection("Teleport Places")

Tab7Section:NewButton("Mars", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-17, 76667, 162)
end)

Tab7Section:NewButton("Moon", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-15, 52667, 186)
end)

Tab7Section:NewButton("Space Bubble", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-16, 34716, 93)
end)

Tab7Section:NewButton("Floating Rock", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-16, 17881, 94)
end)

Tab7Section:NewButton("Dunes", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-16, 8313, 93)
end)

Tab7Section:NewButton("Snowy Snow", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-29, 3503, 96)
end)

Tab7Section:NewButton("Peaceful Fields", "Hello", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-28, 1022, 94)
end)

Tab8Section:NewToggle("Auto Sell", "ToggleInfo", function(state)
    if state then
_G.sell = true
while _G.sell do
    wait(10) -- its good delay didnt change
local args = {
    [1] = {
        [1] = "SellMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
    else
_G.sell = false
while _G.sell do
    wait(9999999999)
     wait(txt)
local args = {
    [1] = {
        [1] = "SellMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
    end
end)

Tab8Section:NewToggle("Auto Gain", "ToggleInfo", function(state)
    if state then
_G.gain = true
while _G.gain do
    wait(0.0000000000000000000001) -- its good delay didnt change
local args = {
    [1] = {
        [1] = "GainMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
    else
_G.gain = false
while _G.gain do
    wait(txt) -- its good delay didnt change
local args = {
    [1] = {
        [1] = "GainMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
    end
end)
Tab8Section:NewTextBox("Auto Sell", "ARE YOU DUMD?! FUCK UR SELF", function(txt)
_G.sell = true
while _G.sell do
    wait(txt) -- its good delay didnt change
local args = {
    [1] = {
        [1] = "SellMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
end)

Tab8Section:NewTextBox("Auto Gain", "ARE YOU DUMD?! FUCK UR SELF", function(txt)
_G.gain = true
while _G.gain do
    wait(txt) -- its good delay didnt change
local args = {
    [1] = {
        [1] = "GainMuscle"
    }
}

game:GetService("ReplicatedStorage").RemoteEvent:FireServer(unpack(args))
end
end)

Tab9Section:NewToggle("Auto Swing", "Auto Swing", function(v)
getgenv().autoswing = v
        while true do
            if not getgenv().autoswing then return end
            for _,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
                if v:FindFirstChild("ninjitsuGain") then
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(v)
                    break
                end
            end
            local A_1 = "swingKatana"
            local Event = game:GetService("Players").LocalPlayer.ninjaEvent
            Event:FireServer(A_1)
            wait(0.1)
    end
end)

Tab9Section:NewToggle("Auto Sell", "Auto Sell", function(state)
getgenv().autosell = v
        while true do
            if getgenv().autoswing == false then return end
            game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
            wait(0.1)
            game:GetService("Workspace").sellAreaCircles["sellAreaCircle16"].circleInner.CFrame = CFrame.new(0,0,0)
            wait(0.1)
    end
end)

local Tab9Section = Tab9:NewSection("Auto Buy")

Tab9Section:NewToggle("Auto Buy Belts", "Auto Buy", function(state)
getgenv().buybelts = v
        while true do
            if not getgenv().buybelts then return end
            local A_1 = "buyAllBelts"
            local A_2 = "Inner Peace Island"
            local Event = game:GetService("Players").LocalPlayer.ninjaEvent
            Event:FireServer(A_1, A_2)
            wait(0.5)
    end
end)

Tab9Section:NewToggle("Auto Buy Katana", "Auto Buy", function(state)
getgenv().buyswords = v
        while true do
            if not getgenv().buyswords then return end
            local A_1 = "buyAllSwords"
            local A_2 = "Inner Peace Island"
            local Event = game:GetService("Players").LocalPlayer.ninjaEvent
            Event:FireServer(A_1, A_2)
            wait(0.5)
    end
end)

local Tab9Section = Tab9:NewSection("Unluck All Island")

Tab9Section:NewButton("Unluck All Island", "Unluck All", function()
local oldcframe = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
        for _,v in pairs(game:GetService("Workspace").islandUnlockParts:GetChildren()) do
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
            wait(0.1)
        end
        wait(0.1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = oldcframe
end)

Tab10Section:NewButton("British Hub V4", "ButtonInfo", function()
local StarterGui = game:GetService("StarterGui")
local bindable1 = Instance.new("BindableFunction")

function bindable1.OnInvoke(response)
setclipboard('https://discord.gg/bK3ruZfwaE')
end

StarterGui:SetCore("SendNotification", {
	Title = "Discord",
	Text = "Join Discord",
	Duration = 3,
	Callback = bindable1,
	Button1 = "Sure",
})
wait(2.1)
loadstring(game:HttpGet(('https://raw.githubusercontent.com/YourLocalNzi/Ye/main/HitBox%20Expand.txt'),true))()
end)

local Tab10Section = Tab10:NewSection("Fire Hub [2]")

Tab10Section:NewButton("Fire Hub [2]", "ButtonInfo", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/alt1lr/FireHubV0.2/main/README.md', true))()
end)
