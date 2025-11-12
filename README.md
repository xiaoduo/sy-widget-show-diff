# Show Diff Widget for SiYuan

A SiYuan note widget that automatically displays the diff between two code blocks in a super block.

[中文](README_zh_CN.md)

## Features

- 🔄 **Auto-refresh**: Automatically updates the diff result every 5 seconds
- 📝 **Template insertion**: One-click button to insert the comparison template structure
- 🎨 **Visual diff display**: Clear visualization with green (additions) and red (deletions)
- 📊 **Statistics**: Shows the number of added and removed lines
- 🖥️ **100% width**: Full-width display by default
- ⚡ **Real-time**: Reads content from super block above and displays diff immediately

## Usage

### Basic Workflow

```
┌────────────────────────────────────────┐
│  Super Block (Side by Side)            │
│  ┌─────────────┐  ┌─────────────┐     │
│  │ ```         │  │ ```         │     │
│  │ Original    │  │ Modified    │     │
│  │ Code        │  │ Code        │     │
│  │ ```         │  │ ```         │     │
│  └─────────────┘  └─────────────┘     │
└────────────────────────────────────────┘
              ↓
┌────────────────────────────────────────┐
│  Widget (Shows diff result only)        │
│  - Deleted lines (red background)       │
│  + Added lines (green background)       │
│    Unchanged lines                      │
└────────────────────────────────────────┘
```

### Step-by-Step Guide

1. **Insert the Widget**: Add the widget to your SiYuan document
2. **Insert Template**: Click the "📝 插入对比模板" button to automatically insert the super block template above the widget
3. **Add Your Code**: Replace the placeholder text with your actual code in both code blocks (left: original, right: modified)
4. **View Diff**: The diff result will automatically appear in the widget below

### Manual Setup

If you prefer to create the structure manually:

1. Create a super block with row layout above the widget
2. Add two code blocks side by side in the super block
3. Put your original code in the left code block
4. Put your modified code in the right code block
5. The widget will automatically detect and display the diff

## Controls

- **📝 插入对比模板**: Insert the comparison template structure above the widget
- **🔄 刷新对比**: Manually refresh the diff (also auto-refreshes every 5 seconds)

## Display Features

- **Line numbers**: Shows line numbers for easy reference
- **Color coding**:
  - 🟢 Green background: Added lines
  - 🔴 Red background: Removed lines
  - ⚪ White background: Unchanged lines
- **Statistics**: Displays total number of additions and deletions
- **Responsive**: Full-width display adapts to container size

## Installation

1. Download the widget from the SiYuan marketplace
2. Or clone this repository to `{workspace}/conf/appearance/widgets/sy-widget-show-diff`
3. Restart SiYuan or refresh the widget list

## Requirements

- SiYuan version: 2.8.8 or higher
- The widget must be placed below a super block containing two code blocks

## Todo
- Add split diff view

## Troubleshooting

**Error: "在挂件上方未找到超级块"**
- Make sure there's a super block directly above the widget
- The super block should contain at least two code blocks

**Empty diff result**
- Check that both code blocks contain content
- Verify the code blocks are properly formatted with ``` markers

**Widget not loading**
- Ensure SiYuan is running
- Check that the API port 6806 is accessible
- Try clicking the "🔄 刷新对比" button manually

## License

MIT License

## Author

xiaoduo

## Links

- GitHub: https://github.com/xiaoduo/sy-widget-show-diff
- Issues: https://github.com/xiaoduo/sy-widget-show-diff/issues
