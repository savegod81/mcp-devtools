## How-To on Windows using Claud apps
1. install: npm install -g @oscarmarin/mcp-devtools
2. in claude_desktop_config.json add mcp server's setting
"mcpServers":
    {
        "devtools":
        {
            "command": "D:\\dev\\nodejs\\node.exe",
            "args":
            [
                "D:\\dev\\nodejs\\node_modules\\@oscarmarin\\mcp-devtools\\dist\\index.js"
            ],
            "env":
            {
                "MCP_DEVTOOLS_CONFIG": "D:\\dev\\nodejs\\mcp-devtools.json"
            }
        }
    }
3. if you need to confine the working folder, create mcp-devtools.json and set the scope
{
    "scope": "D:\\tmp",
    "allowedCommands":
    [
        "npm",
        "node",
        "python",
        "git",
        "make"
    ],
    "databases":
    {},
    "logs":
    {
        "paths":
        [],
        "maxLines": 500
    }
}
4. completely restart Claud App
5. prompt with some local file system operations and verify
