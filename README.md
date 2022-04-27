local ESP = false

local UserInputService = game:GetService("UserInputService")
wait = task.wait

UserInputService.InputBegan:connect(function(key,typing)
if typing then return end
if key.KeyCode == Enum.KeyCode.H then

if ESP then
    ESP = false
for i,v in pairs(game:GetService("Workspace"):GetDescendants()) do
if v:IsA("BillboardGui") and v.Name == "notesplel" then
    v:remove()
  end
end

 
 else
    ESP = true

    
spawn(function()
while wait() do
    if ESP then
pcall(function()
for i,v in pairs(game:GetService("Players"):GetPlayers()) do 
        if v~=game.Players.LocalPlayer then
        local Char = v.Character or v.CharacterAdded:wait()
    if not Char:FindFirstChild("Head") then return end
    if not Char.Head:FindFirstChild("notesplel") then 
    if not Char:FindFirstChild("Health")  then return end
    if not Char:FindFirstChild("Config") then return end
    if not Char.Config:FindFirstChild("BattlePower") then return end
    local BillboardGui = Instance.new("BillboardGui",Char.Head)

        local Frame = Instance.new("Frame")
        local TextLabel = Instance.new("TextLabel")
        BillboardGui.Adornee = Char.Head
        BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        BillboardGui.Active = true
        BillboardGui.Name = 'notesplel'
        BillboardGui.LightInfluence = 1.000
        BillboardGui.Size = UDim2.new(0, 200, 0, 50)
        BillboardGui.StudsOffset = Vector3.new(0, 3, 0)
        BillboardGui.AlwaysOnTop = true
        Frame.Parent = BillboardGui
        Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Frame.BackgroundTransparency = 10.000
        Frame.Size = UDim2.new(0, 200, 0, 200)

        TextLabel.Parent = Frame
        TextLabel.BackgroundTransparency = 1
        TextLabel.Position = UDim2.new(0, 0, 0, -50)
        TextLabel.Size = UDim2.new(0, 100, 0, 100)
        TextLabel.Font = Enum.Font.SourceSansSemibold
        TextLabel.TextSize = 20
        TextLabel.TextColor3 = Color3.new(1, 1, 1)
        TextLabel.TextStrokeTransparency = 0
        TextLabel.TextYAlignment = Enum.TextYAlignment.Bottom
        TextLabel.Text = ''..v.Name..' | Health: '..Char:FindFirstChild("Health").Value..' | BattlePower: '..Char:FindFirstChild("Config").BattlePower.Value
        TextLabel.ZIndex = 10
        
        wait()
        spawn(function()
        while wait() do
         TextLabel.Text = ''..v.Name..' | Health: '..Char:FindFirstChild("Health").Value..' | BattlePower: '..Char:FindFirstChild("Config").BattlePower.Value
         end
        end)
        
        
        if v:IsFriendsWith(game.Players.LocalPlayer.UserId) then
            TextLabel.TextColor3 = Color3.new(0,255,0)
                                  end
                              end
                          end
                       end
                   end)
                end
             end
         end)
      end
    end
end)

game.Players.PlayerAdded:connect(function()
      if ESP then
pcall(function()
for i,v in pairs(game:GetService("Players"):GetPlayers()) do 
        if v~=game.Players.LocalPlayer then
        local Char = v.Character or v.CharacterAdded:wait()
    if not Char:FindFirstChild("Head") then return end
    if not Char.Head:FindFirstChild("notesplel") then 
    if not Char:FindFirstChild("Health")  then return end
    if not Char:FindFirstChild("Config") then return end
    if not Char.Config:FindFirstChild("BattlePower") then return end
    local BillboardGui = Instance.new("BillboardGui",Char.Head)

        local Frame = Instance.new("Frame")
        local TextLabel = Instance.new("TextLabel")
        BillboardGui.Adornee = Char.Head
        BillboardGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        BillboardGui.Active = true
        BillboardGui.Name = 'notesplel'
        BillboardGui.LightInfluence = 1.000
        BillboardGui.Size = UDim2.new(0, 200, 0, 50)
        BillboardGui.StudsOffset = Vector3.new(0, 3, 0)
        BillboardGui.AlwaysOnTop = true
        Frame.Parent = BillboardGui
        Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Frame.BackgroundTransparency = 10.000
        Frame.Size = UDim2.new(0, 200, 0, 200)

        TextLabel.Parent = Frame
        TextLabel.BackgroundTransparency = 1
        TextLabel.Position = UDim2.new(0, 0, 0, -50)
        TextLabel.Size = UDim2.new(0, 100, 0, 100)
        TextLabel.Font = Enum.Font.SourceSansSemibold
        TextLabel.TextSize = 20
        TextLabel.TextColor3 = Color3.new(1, 1, 1)
        TextLabel.TextStrokeTransparency = 0
        TextLabel.TextYAlignment = Enum.TextYAlignment.Bottom
        TextLabel.Text = ''..v.Name..' | Health: '..Char:FindFirstChild("Health").Value..' | BattlePower: '..Char:FindFirstChild("Config").BattlePower.Value
        TextLabel.ZIndex = 10
        
        wait()
        spawn(function()
        while wait() do
         TextLabel.Text = ''..v.Name..' | Health: '..Char:FindFirstChild("Health").Value..' | BattlePower: '..Char:FindFirstChild("Config").BattlePower.Value
         end
        end)
        
        
        if v:IsFriendsWith(game.Players.LocalPlayer.UserId) then
            TextLabel.TextColor3 = Color3.new(0,255,0)
end
end
end
end
end)
end
end)

