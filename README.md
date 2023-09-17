local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Monke Gone Gay", "Synapse")

local Tab = Window:NewTab("Auto Play")
local Section = Tab:NewSection("Pro Main")
Section:NewButton("Auto Skip", "Auto Skip wave", function()

local args = {
    [1] = "AutoSkip"
}

game:GetService("ReplicatedStorage"):WaitForChild("Remote"):WaitForChild("Setting"):FireServer(unpack(args))
end)

Section:NewButton("Shielder Monke", "Shielder OFC", function()

local args = {
    [1] = "Shielder",
    [2] = CFrame.new(-420.6040344238281, 179.02679443359375, 1270.0279541015625, 1, 0, 0, 0, 1, 0, 0, 0, 1)
}
game:GetService("ReplicatedStorage"):WaitForChild("Remote"):WaitForChild("SpawnUnit"):InvokeServer(unpack(args))

end)

Section:NewButton("Speed x2", "Nothing", function()

local args = {
    [1] = "x1 Speed"
}
game:GetService("ReplicatedStorage"):WaitForChild("Remote"):WaitForChild("x2Event"):FireServer(unpack(args))

end)

Section:NewButton("AutoUpgrade Shielder", "L", function()

 while true do 
     Wait(2)
local args = {
    [1] = workspace:WaitForChild("Units"):WaitForChild("Shielder")
}
game:GetService("ReplicatedStorage"):WaitForChild("Remote"):WaitForChild("UpgradeUnit"):InvokeServer(unpack(args))
end
end)

Section:NewButton("Start Game","L", function()

game:GetService("ReplicatedStorage"):WaitForChild("Remote"):WaitForChild("SkipEvent"):FireServer()
end)
