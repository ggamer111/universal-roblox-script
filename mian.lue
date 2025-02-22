--made my charlie
--most if this code it not mine i just compiled it to make it better for people to use 


local players = game:GetService("Players")
local run_service = game:GetService("RunService")
local user_input_service = game:GetService("UserInputService")
local tween_service = game:GetService("TweenService")
local core_gui = game:GetService("CoreGui")
local loader = Instance.new("ScreenGui") 

local loader = Instance.new("ScreenGui", core_gui)                           

print("😨some of these are very bad i will update when i have time😨")
wait(0.5)
print("😨some script will not work in some games due to the way the game runs😨")
local games = {
    { name = "✔️Full cheat✔️", link = "https://raw.githubusercontent.com/ttwizz/Open-Aimbot/master/source.lua" },
    { name = "👨🏿Charlie ESP👨🏿", link = "https://raw.githubusercontent.com/ggamer111/roblox-esp/refs/heads/main/esp/esp.lua" },
    { name = "🐋Orcs cheats🐋", link = "https://raw.githubusercontent.com/DarkNetworks/Orca/master/public/latest.lua" },
    { name = "💀SkeletonESP💀", link = "https://raw.githubusercontent.com/Blissful4992/ESPs/main/SkeletonESP.lua" },
    { name = "📦2D Box ESP📦", link = "https://raw.githubusercontent.com/Blissful4992/ESPs/main/2D%20Box%20ESP/ESP%20%2B%20Health%20Bars.lua" },
    { name = "📦Corner 2D Box ESP📦", link = "https://raw.githubusercontent.com/Blissful4992/ESPs/main/Corner%202D%20Box%20ESP.lua" },
    { name = "📡PlayerRadar📡", link = "https://raw.githubusercontent.com/Blissful4992/ESPs/main/PlayerRadar.lua" },
    { name = "🤖Aimbot🤖", link = "https://raw.githubusercontent.com/Exunys/Aimbot-V2/main/Resources/Scripts/Raw%20Main.lua" },
    { name = "✈️fly✈️", link = "https://raw.githubusercontent.com/lilmond/roblox_fly_script/refs/heads/main/v4.lua" },    
    { name = "⚠️3D boxes⚠️", link = "https://raw.githubusercontent.com/ggamer111/esp.lua/refs/heads/main/3D%20boxes" },
    { name = "👀Spectate👀", link = "https://raw.githubusercontent.com/ggamer111/esp.lua/refs/heads/main/spectate.lua" },
    { name = "😬CHATGPT AIMBOT😬", link = "https://raw.githubusercontent.com/ggamer111/chatgpt-aimbot.lua/refs/heads/main/chatgpt.lua" },
    { name = "🏃🏿SPEED🏃🏿", link = "https://raw.githubusercontent.com/ggamer111/speed.lua/refs/heads/main/speed.lua" },
    { name = "👮🏿TP SCRIPT👮🏿", link = "https://raw.githubusercontent.com/ggamer111/esp.lua/refs/heads/main/tp.lua" },
}



local custom_callbacks = {}

local holder_stroke = Instance.new("UIStroke")
holder_stroke.Color = Color3.fromRGB(24, 24, 24)
holder_stroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border

-- UI Creation
do
    local dragging = false
    local mouse_start = nil
    local frame_start = nil
    local menu_open = true  -- Track if the menu is open or closed

    -- Create the main frame for the loader
    local main = Instance.new("Frame", loader)
    do
        main.BackgroundColor3 = Color3.fromRGB(12, 12, 12)
        main.BorderColor3 = Color3.fromRGB(0, 0, 0)
        main.BorderSizePixel = 0
        main.Position = UDim2.new(0.427201211, 0, 0.393133998, 0)
        main.Size = UDim2.new(0.145, 0, 0.267, 0)
    end

    -- Title label on top of the loader UI
    local title = Instance.new("TextLabel", main)
    do
        title.BackgroundColor3 = Color3.fromRGB(13, 13, 13)
        title.BorderColor3 = Color3.fromRGB(0, 0, 0)
        title.BorderSizePixel = 0
        title.Position = UDim2.new(0.0361463465, 0, 0.0199999996, 0)
        title.Size = UDim2.new(0.926784515, 0, 0.112490386, 0)
        title.Font = Enum.Font.RobotoMono
        title.Text = "👑Made by Charlie Mitchell👑"
        title.TextColor3 = Color3.fromRGB(255, 255, 255)
        title.TextStrokeTransparency = 0.000
        title.TextWrapped = true
        title.TextSize = 18
    end

    -- UI dragging functionality
    title.InputBegan:Connect(function(input)
        if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then
            dragging = true
            mouse_start = user_input_service:GetMouseLocation()
            frame_start = main.Position
        end
    end)

    user_input_service.InputChanged:Connect(function(input)
        if (dragging and input.UserInputType == Enum.UserInputType.MouseMovement) then
            local delta = user_input_service:GetMouseLocation() - mouse_start
            tween_service:Create(main, TweenInfo.new(0.1), {Position = UDim2.new(frame_start.X.Scale, frame_start.X.Offset + delta.X, frame_start.Y.Scale, frame_start.Y.Offset + delta.Y)}):Play()
        end
    end)

    user_input_service.InputEnded:Connect(function(input)
        if (dragging) then
            dragging = false
        end
    end)

    -- Create the holder frame that will hold all the buttons
    local holder = Instance.new("Frame", main)
    do
        holder.BackgroundColor3 = Color3.fromRGB(13, 13, 13)
        holder.BorderColor3 = Color3.fromRGB(0, 0, 0)
        holder.BorderSizePixel = 0
        holder.Position = UDim2.new(0.0361457169, 0, 0.167407826, 0)
        holder.Size = UDim2.new(0.926784515, 0, 0.781875908, 0)
    end

    -- Add stroke and corner radius to the holder
    local stroke = holder_stroke:Clone()
    stroke.Parent = holder

    local ui_corner_2 = Instance.new("UICorner", holder)
    ui_corner_2.CornerRadius = UDim.new(0, 4)

    -- Create the scrolling frame where the buttons will appear
    local scrolling_frame = Instance.new("ScrollingFrame", holder)
    scrolling_frame.Active = true
    scrolling_frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    scrolling_frame.BackgroundTransparency = 1.000
    scrolling_frame.Position = UDim2.new(0, 0, 3.04931473e-06, 0)
    scrolling_frame.Size = UDim2.new(1, 0, 0.999999821, 0)
    scrolling_frame.CanvasSize = UDim2.new(0, 0, 5, 0)

    -- Padding and layout for the buttons
    local ui_padding = Instance.new("UIPadding", scrolling_frame)
    ui_padding.PaddingTop = UDim.new(0, 10)

    local ui_grid_layout = Instance.new("UIGridLayout", scrolling_frame)
    ui_grid_layout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    ui_grid_layout.SortOrder = Enum.SortOrder.LayoutOrder
    ui_grid_layout.CellPadding = UDim2.new(0, 10, 0, 10)
    ui_grid_layout.CellSize = UDim2.new(0, 165, 0, 25)

    -- Create a button for each game script
    for _, supported_game in pairs(games) do
        local text_button = Instance.new("TextButton", scrolling_frame)
        text_button.Text = "Load " .. supported_game.name
        text_button.BackgroundColor3 = Color3.fromRGB(14, 14, 14)
        text_button.BorderColor3 = Color3.fromRGB(0, 0, 0)
        text_button.BorderSizePixel = 0
        text_button.Size = UDim2.new(0.14958863, 0, 0.0553709865, 0)
        text_button.Font = Enum.Font.RobotoMono
        text_button.TextColor3 = Color3.fromRGB(255, 255, 255)
        text_button.TextSize = 12.000
        text_button.TextWrapped = true

        -- Button click functionality to load the script
        text_button.MouseButton1Click:Connect(function()
            -- Do not destroy the loader UI here; let it remain open
            local success, err = pcall(function()
                loadstring(game:HttpGet(supported_game.link))()  -- Load the script
            end)

            if not success then
                warn("Error loading script: " .. err)  -- Log any errors
            end
        end)

        -- Apply a UI stroke and corner radius to the buttons
        local stroke = holder_stroke:Clone()
        stroke.Parent = text_button

        local ui_corner_3 = Instance.new("UICorner", text_button)
        ui_corner_3.CornerRadius = UDim.new(0, 4)
    end

    -- Toggle the menu when INS key is pressed
    user_input_service.InputBegan:Connect(function(input, gameProcessed)
        if not gameProcessed then
            if input.KeyCode == Enum.KeyCode.Insert then
                menu_open = not menu_open  -- Toggle menu state
                main.Visible = menu_open   -- Set menu visibility
            end
        end
    end)
end
