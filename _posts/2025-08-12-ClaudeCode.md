---
layout: post
title: How to use Claude Code
date: 2025-08-10 01:47:00
description: 
tags: Machine-Learning
chart:
  plotly: true
---


## Download
Software download 
Node.js 18+ (https://nodejs.org/en/download)
git 
GitHub or GitLab

Install Claude Code 
```bash
npm install -g @anthropic-ai/claude-code

cd your-project-directory

claude
```


Install github cli `sudo apt install gh`




## Different way to using claude
Chat box mode(headless mode): `claude -p "tell me a joke"` in your terminal

Better install jq, `sudo apt install jq`


yolo mode: ignore premissions issues. `claude yolo - p`




## Claude Code Command
- `/init`: It will help you generate a claude.md file that alow you write instruction for the project and code. 
- `@ + file name`: let claude code to read that file.
- `ESC`: ESC twice will show all the history talk.  
- `Install Github App` 
- `/memory` and `# [Add memory]` for adding memory for your local memory or project memory. 


## Make you own command
Make a commands file `mkdir -p ~/.claude/commands`

Make your own command and you can type and use in claude code `echo "find stock price of $ARGUMENTS right now" > ~/.claude/commands/stockprice.md`


## Claude Code MCP

### Context 7
```bash
claude mcp add --transport http context7 https://mcp.context7.com/mcp --header "CONTEXT7_API_KEY: YOUR_API_KEY"
```




### Modify MCP setting bu youself
`nano .mcp.json`


## Hook
 



## Tips
- Using `Control + R` will help you expend section and show all the context. 



