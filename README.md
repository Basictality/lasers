was=game.Players.LocalPlayer.Character was.Humanoid.MaxHealth = "9e999" was.Head.Transparency = "1" Head=Instance.new("Part",was) Head.Name = "ExtraHead" Head.Transparency="0" Head.FormFactor = was.Head.FormFactor Head.Size = was.Head.Size Head.Color = was.Head.Color meshhead=Instance.new("SpecialMesh",Head) meshhead.Scale = was.Head.Mesh.Scale

weldHead=Instance.new("Weld",Head) weldHead.Part0=was.Head weldHead.Part1=Head


p=game.Players.LocalPlayer
c=p.Character
m=p:GetMouse()
Player = game:GetService("Players").LocalPlayer
mouse=Player:GetMouse()
Cha = Player.Character
mouse.KeyDown:connect(function(key)
key:lower()
if key == "r" then

x=game.Players.LocalPlayer.Character
local armweld = Instance.new("Weld",x)
armweld.Part0=x.Torso
armweld.Part1=x['Right Arm']
armweld.C0=CFrame.new(1.5,0.5,-0.5) * CFrame.Angles(20.4,0,0)
lightning=Instance.new("Part",x)
lightning.FormFactor = "Custom"
lightning.BrickColor = BrickColor.new'Really red'
lightning.Size = Vector3.new(0,50,0)

function onTouched(hit)
Instance.new("Fire",hit)
local human = hit.Parent:findFirstChild("Humanoid") 
if (human == nil) then return end 
human:TakeDamage(20)
end 
lightning.Touched:connect(onTouched)

local weld = Instance.new("Weld",lightning)
weld.Part0=lightning
weld.Part1=x['Right Arm']
weld.C0=CFrame.new(0,25,0)
local armweld3 = Instance.new("Weld",x)
armweld3.Part0=x.Torso
armweld3.Part1=x['Left Arm']
armweld3.C0=CFrame.new(-1.5,0.5,-0.5) * CFrame.Angles(20.4,0,0)
lightning2=Instance.new("Part",x)
lightning2.FormFactor = "Custom"
lightning2.BrickColor = BrickColor.new'Really red'
lightning2.Size = Vector3.new(0,50,0)

function onTouched(hit)
Instance.new("Fire",hit)
local human = hit.Parent:findFirstChild("Humanoid") 
if (human == nil) then return end 
human:TakeDamage(20)
end 
lightning2.Touched:connect(onTouched)

local weld2 = Instance.new("Weld",lightning2)
weld2.Part0=lightning2
weld2.Part1=x['Left Arm']
weld2.C0=CFrame.new(0,25,0)
wait(1)
lightning:remove()
local armweld = Instance.new("Weld",x)
armweld.Part0=x.Torso
armweld.Part1=x['Right Arm']
armweld.C0=CFrame.new(1.5,-0,-0) * CFrame.Angles(0,0,0)
lightning2:remove()
local armweld2 = Instance.new("Weld",x)
armweld2.Part0=x.Torso
armweld2.Part1=x['Left Arm']
armweld2.C0=CFrame.new(-1.5,-0,-0) * CFrame.Angles(0,0,0)
end
end)
