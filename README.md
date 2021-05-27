# gamepass-helper
Stuff for roblox

Buy gamepass

MPS = game:GetService("MarketplaceService")
id = 978478012 -- put your ID there
local player = game.Players.LocalPlayer

script.Parent.MouseButton1Click:connect(function()
	MPS:PromptProductPurchase(player, id)
end)

-----

Buy item 

--Put Screen GUI in starterGui--
--replace the gamepass id with your id--
--Put gear giver in ServerScriptService--
--Find the item you want--
--Put it in lighting--
--Replace gamepassidhere with your gamepass id--
--Replace itemnamehere
--Delete this--

game.Players.PlayerAdded:connect(function(player)
    if game:GetService("MarketplaceService"):UserOwnsGamePassAsync(player.userId, gamepassidhere) then
        if player.Backpack:FindFirstChild("itemnamehere") == nil then

            local b = game.Lighting:FindFirstChild("itemnamehere"):Clone() -- gives item instantly
            b.Parent = player.Backpack
            local b2 = game.Lighting:FindFirstChild("itemnamehere"):Clone() --gets item when you die
            b2.Parent = player.StarterGear
        end
    end
end)

or you could get my gear https://web.roblox.com/library/5057285344/GamepassHelper
