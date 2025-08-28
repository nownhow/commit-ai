# AI commit reviewer
Using **AI** to review your commit message and staged files 

## Implementation
1. Add "commit-ai" file to **your_project_path/.git/hooks/**

2. Run 
```bash 
 chmod +x .git/hooks/commit-ai
```
> make it executable

3. Add API key
```bash
echo "your-real-key-here" > ~/.gemini-key
chmod 600 ~/.gemini-key
```

4. Make this file run every time we commit
```bash 
cd your-project/.git/hooks
nano commit-msg
```

Inside
```bash
#!/bin/bash
.git/hooks/commit-ai "$1" || exit 1
```

Make it executable
```bash
chmod +x commit-msg
```

