-- AutoFarm con menú y logo de rayo
-- StarterPlayerScripts

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

local autoFarm = false
local range = 50 -- rango máximo para atacar

-- GUI principal
local ScreenGui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
ScreenGui.ResetOnSpawn = false

-- Botón del logo (ícono de rayo)
local LogoButton = Instance.new("ImageButton", ScreenGui)
LogoButton.Size = UDim2.new(0, 60, 0, 60)
LogoButton.Position = UDim2.new(0, 20, 0.8, 0) -- esquina izquierda abajo
LogoButton.Image = "rbxassetid://5107182114" -- ⚡ ID de un rayo (puedes cambiarlo por otro decal)

-- Panel oculto
local Panel = Instance.new("Frame", ScreenGui)
Panel.Size = UDim2.new(0, 220, 0, 120)
Panel.Position = UDim2.new(0, 90, 0.7, 0)
Panel.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Panel.Visible = false
Panel.Active = true
Panel.Draggable = true -- para mover el panel
