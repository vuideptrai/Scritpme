-- UI Script cho exploit (dùng được trên Deltax, Synapse, KRNL...)
-- Load thư viện UI trước (bạn phải thay bằng link thư viện UI thật)
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/yourUILibraryHere"))()
local Window = Library:MakeWindow({
    Hub = {
        Title = "vuideptrai",
        Animation = "hikaru là nô lệ:"
    }
})

Window:MinimizeButton({
    Image = "http://www.roblox.com/asset/?id=83190276951914",
    Size = {60, 60},
    Color = Color3.fromRGB(10, 10, 10),
    Corner = true,
    Stroke = false,
    StrokeColor = Color3.fromRGB(255, 0, 0)
})

local TabFarm = Window:MakeTab({Name = "Script Farm"})
TabFarm:AddButton({
    Name = "Redz Hub",
    Callback = function()
        local Settings = {
            JoinTeam = "Pirates",
            Translator = true
        }
        loadstring(game:HttpGet("https://raw.githubusercontent.com/realredz/BloxFruits/refs/heads/main/Source.lua"))(Settings)
    end
})

local TabFixLag = Window:MakeTab({Name = "Fix Lag"})
TabFixLag:AddButton({
    Name = "Tối Ưu Game (Fix Lag)",
    Callback = function()
        for _, v in pairs(game:GetDescendants()) do
            if v:IsA("BasePart") then
                v.Material = Enum.Material.SmoothPlastic
                v.Reflectance = 0
            elseif v:IsA("Decal") or v:IsA("Texture") then
                v:Destroy()
            end
        end
        settings().Rendering.QualityLevel = Enum.QualityLevel.Level01
        setfpscap(30)
        print("Đã fix lag thành công!")
    end
})

local TabMaruFree = Window:MakeTab({Name = "Maru Free"})
TabMaruFree:AddButton({
    Name = "Load Maru Script 1",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/yourusername/maruscript1/main/script.lua"))()
        print("Đã tải Maru Script 1")
    end
})
TabMaruFree:AddButton({
    Name = "Load Maru Script 2",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/yourusername/maruscript2/main/script.lua"))()
        print("Đã tải Maru Script 2")
    end
})
TabMaruFree:AddButton({
    Name = "Maru Auto Farm Free",
    Callback = function()
        print("Kích hoạt Auto Farm Maru miễn phí")
        -- Thêm code auto farm hoặc load script ở đây
    end
})
