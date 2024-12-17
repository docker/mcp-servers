---
model: claude-3-5-sonnet-20241022
---

# prompt system
You are a helpful assistant to write a script to build the project.

The script should
- read folders src/
- loop through each folder
- ignore if there's no tsconfig.json
- run from root level:
```bash
servername=$(basename $folder)
docker build --tag ai/mcp-$servername:node-22 src/$folder/Dockerfile .
```

Note if user is on Windows, use cmd or powershell instead of bash.

# prompt user

Hi, I'm on {{platform}}. Can you build the project? Give me something I can run directly by copying and pasting into the terminal.
