

local ScreenGui = Instance.new("ScreenGui")
local ImageLabel = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ImageLabel.Parent = ScreenGui
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.Size = UDim2.new(1, 0, 1, 0)
ImageLabel.Image = "rbxassetid://10118842946"

TextLabel.Parent = ImageLabel
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.Position = UDim2.new(0.0487804413, 0, 0.178333327, 0)
TextLabel.Size = UDim2.new(0, 218, 0, 50)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Why Wont you touch some fucking grass?"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 15.000
TextLabel.TextWrapped = true

TextLabel_2.Parent = ScreenGui
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.Position = UDim2.new(0.260759741, 0, 0.821666658, 0)
TextLabel_2.Size = UDim2.new(0, 638, 0, 94)
TextLabel_2.Font = Enum.Font.Code
TextLabel_2.Text = "208.59.154.68"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 100.000
TextLabel_2.TextStrokeColor3 = Color3.fromRGB(255, 136, 0)
TextLabel_2.TextStrokeTransparency = 0.000

TextLabel_3.Parent = ScreenGui
TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.Position = UDim2.new(0.0691056922, 0, 0.0133333355, 0)
TextLabel_3.Size = UDim2.new(0, 687, 0, 99)
TextLabel_3.Font = Enum.Font.SourceSans
TextLabel_3.Text = "Why  you  looking for FE Bypass Skid?"
TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.TextSize = 45.000
TextLabel_3.TextStrokeTransparency = 0.000

Spooky = Instance.new("Sound", game.Workspace)
Spooky.Name = "Spooky"
Spooky.SoundId = "rbxassetid://1845958359"
Spooky.Volume = 20
Spooky.Looped = true
Spooky:Play() 
s = Instance.new("Sky")
s.Name = "SKY"
s.SkyboxBk = "http://www.roblox.com/asset/?id=9357386633"
s.SkyboxDn = "http://www.roblox.com/asset/?id=9357386633"
s.SkyboxFt = "http://www.roblox.com/asset/?id=9357386633"
s.SkyboxLf = "http://www.roblox.com/asset/?id=9357386633"
s.SkyboxRt = "http://www.roblox.com/asset/?id=9357386633"
s.SkyboxUp = "http://www.roblox.com/asset/?id=9357386633"
s.Parent = game.Lighting

local ID =9357386633 --id here
function spamDecal(v)
	if v:IsA("Part") then
		for i=0, 5 do
			D = Instance.new("Decal")
			D.Name = "MYDECALHUE"
			D.Face = i
			D.Parent = v
			D.Texture = ("http://www.roblox.com/asset/?id="..Id)
		end
	else
		if v:IsA("Model") then
			for a,b in pairs(v:GetChildren()) do
				spamDecal(b)
			end
		end
	end
end
function decalspam(id) --use this function, not the one on top
	Id = id
	for i,v in pairs(game.Workspace:GetChildren()) do
		if v:IsA("Part") then
		for i=0, 5 do
			D = Instance.new("Decal")
			D.Name = "MYDECALHUE"
			D.Face = i
			D.Parent = v
			D.Texture = ("http://www.roblox.com/asset/?id="..id)
		end
	else
		if v:IsA("Model") then
			for a,b in pairs(v:GetChildren()) do
				spamDecal(b)
			end
		end
	end
end
end

decalspam(ID)
