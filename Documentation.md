# Ruby Hub Functions
Documentation of Ruby Hub Functions provided to create a user friendly experience.
Running Ruby Hub Functions without the Configs table will use default configs.

## Getting Functions
```lua
local Configs = {
    StartupNotification = true, -- Toast Notification On Startup: default = true
    StartupAnimation = true, -- Loading Animation On Startup: default = true
    ErrorToastNotifications = true -- Toast Notifications For Errors: default = false
}

RubyHubFunctions = loadstring(game:HttpGet("https://raw.githubusercontent.com/RubyScriptsOnTop/RubyHubFunctions/main/source"))(Configs)
```

## Sending A Webhook
```lua
ReturnedData = RubyHubFunctions.SendWebhook({
    WebhookUrl = "https://discord.com/api/webhooks/xxxxxxxxxxxxxxxxxxx/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-xxxxxxxxxxxxxxxxxxxx_xx",
    WebhookBody = {
        ["content"] = "Example",
        ["embeds"] = {
            {
                ["title"] = "Example",
                ["description"] = "Example",
                ["type"] = "rich",
                ["color"] = tonumber(0x7269da),
                ["fields"] = {
                    {
                        ["name"] = "Example",
                        ["value"] = "Example"
                    }
                },
            }
        }
}})

--[[
    WebhookUrl: string - URL to Webhook
    WebhookBody: table - Webhook Contents
]]
```
