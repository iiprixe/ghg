--6716188523

local Material = loadstring(game:HttpGet("https://raw.githubusercontent.com/Kinlei/MaterialLua/master/Module.lua"))()

local X = Material.Load({
    Title = "[Stormzzys Scripts] </> Business Tycoon",
    Style = 1,
    SizeX = 370,
    SizeY = 300,
    Theme = "Dark", --light dark aqua mocha jester
    ColorOverrides = {
		NavBarAccent = Color3.fromRGB(130,130,130)
    }
})

local Y = X.New({
    Title = "Main"
})

Y.Button({
    Text = "Collect Cash",
    Callback = function()
local ohNumber1 = _G.cash

game:GetService("ReplicatedStorage").GlobalFunctions.ChangePlayerMoney:FireServer(ohNumber1)
end
})

Y.Slider({
    Text = "Cash",
    Callback = function(value)
    _G.cash = value
    end,
    Min = 50,
    Max = 1000000000000000,
    Def = 50
})
