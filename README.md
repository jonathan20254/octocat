
local Test = game.Workspace.Cutscenes.Atoms.sphere.Model.atom.root.Explosion

local test = Test:Clone()
test.Parent = game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart")

for _, child in ipairs(test:GetChildren()) do
    if child:IsA("ParticleEmitter") then
        child:Emit(15)
        child.Enabled = true
    end
end
