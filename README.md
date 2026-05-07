# The Daily Growth Journal

A simple daily journal to help you track progress, record good moments, and keep a habit streak.

## Purpose

This journal keeps your entries on your own device. You can write your tasks, wins, appreciation notes, and reflections without sending your data anywhere else.

## Saving Data

- Your entries are saved automatically while you use the journal.
- The journal saves one entry for each date.
- It also keeps track of your streak and any manual streak adjustments.

## Backup and Restore

You can save a copy of your data and restore it later.

### Backup

Click `Backup Data` to download a file with your journal entries. The file name looks like:

- `Daily-Growth-Journal-Backup-YYYY-MM-DD.json`

### Restore

Click `Restore Data` and upload a backup file from this journal. Only files created by this app will be accepted.

## File Format

- Backup files use the `.json` extension.
- This is the format the app uses to save and restore your journal data.

## How to Use

1. Open `index.html` in your browser.
2. Fill in your tasks, wins, gratitude items, and reflection.
3. Use `Backup Data` to save a copy of your journal.
4. Use `Restore Data` to bring your saved entries back.

## Notes

- Your journal stays on your device unless you choose to back it up.
- Keep your backup file in a safe place so you can restore it later.# 🌟 Kaizen Daily Journal

A complete, production-ready digital Kaizen journal with a clean paper-like interface, built using vanilla HTML, CSS, and JavaScript.

## ✨ Features

### 📝 Core Journaling
- **Daily workflow**: Morning → Throughout day → End of day
- **Priorities section**: Spiritual, Physical, and Mental wins
- **6-task checklist**: Track daily goals with checkboxes
- **Gratitude entries**: Two items for daily appreciation
- **Daily reflection**: Lined textarea for thoughts and insights
- **Random motivational quotes**: 50+ inspiring quotes with author attribution

### 💾 Data Management
- **Auto-save**: All entries save automatically
- **Persistent storage**: Uses localStorage for data persistence
- **Date navigation**: Access any previous or future journal entry
- **Data backup**: All entries stored locally with date-based keys

### 📊 Progress Tracking
- **Streak calculation**: Automatic tracking of consecutive completed days
- **Manual streak adjustment**: Ability to manually update streak with audit logging
- **Visual streak display**: Shows current streak count in real-time

### 📄 PDF Export
- **Clean PDF export**: Export journal pages without UI controls
- **Smart filename format**: `Kaizen-Journal-YYYY-MM-DD-Day-X-Streak.pdf`
- **Print-optimized**: Black and white, clean margins, professional layout

### 📤 Backup Features
- **PDF upload**: Upload previously exported journal PDFs
- **Filename validation**: Enforces proper Kaizen naming conventions
- **Security measures**: File type validation, size limits, filename sanitization
- **Upload history**: Tracks all uploaded backups with metadata

### 🌐 Network Access
- **Multi-device access**: Access from phones, tablets, other computers
- **Local network sharing**: Custom server with automatic IP detection
- **Easy setup**: One-command server startup with clear instructions

## 🚀 Quick Start

### Method 1: Enhanced Server (Recommended)
```bash
# Start the server with network IP display
python3 start_server.py

# Or specify a custom port
python3 start_server.py 3000
```

### Method 2: Basic Server
```bash
# Basic Python HTTP server
python3 -m http.server 8000

# Then find your IP manually:
# Windows: ipconfig
# Mac/Linux: ifconfig or ip addr show
```

## 📱 Multi-Device Access

1. **Start the server** using Method 1 above
2. **Note the network IP** displayed in the terminal
3. **On other devices**: Connect to the same WiFi network
4. **Open browser** and go to `http://YOUR_IP:8000`
5. **Bookmark the URL** for easy access

Example: `http://192.168.1.100:8000`

## 🎯 Daily Workflow

### Morning (5 minutes)
1. **Set date** to today (auto-loaded)
2. **Read daily quote** for inspiration
3. **Define priorities**: Set your spiritual, physical, and mental wins
4. **Plan tasks**: Fill in your 6 daily tasks in the checklist

### Throughout the Day
1. **Check off tasks** as you complete them
2. **Track progress**: Watch your completion rate
3. **Stay motivated**: Refer back to your priorities

### Evening (10 minutes)
1. **Complete gratitude**: List 2 things you're grateful for
2. **Write reflection**: Capture thoughts, lessons, insights
3. **Review completion**: Ensure all 6 tasks are checked for streak credit
4. **Export PDF** (optional): Save a permanent record

## 📊 Streak System

### Automatic Calculation
- **Streak counts** consecutive days with all 6 tasks completed
- **Updates in real-time** as you check off tasks
- **Includes today** if all tasks are complete

### Manual Adjustment
1. Click **"Adjust Streak"** button
2. Enter new streak count (0-365)
3. Confirm adjustment
4. Change is **logged for audit purposes**

### Reset Manual Override
- Delete the `manual-streak` key from localStorage to return to automatic calculation
- Or set manual streak to match calculated streak

## 📤 PDF Backup System

### Upload Requirements
- **File type**: Must be PDF
- **File size**: Maximum 10MB
- **Filename format**: Must match one of these patterns:
  - `Kaizen-Journal-YYYY-MM-DD-Day-X-Streak.pdf`
  - `Kaizen-Journal-YYYY-MM-DD.pdf`
  - `Kaizen-YYYY-MM-DD.pdf`

### Security Features
- **Type validation**: Checks file extension and MIME type
- **Filename sanitization**: Removes dangerous characters
- **Size limits**: Prevents oversized uploads
- **Upload logging**: Tracks all uploads with metadata

## 🛠️ Technical Details

### File Structure
```
Kaizen Journal/
├── index.html          # Main application structure
├── style.css          # Paper-like styling and responsive design
├── script.js          # Core functionality and data management
├── start_server.py    # Enhanced server with network IP display
└── README.md          # This documentation
```

### Browser Compatibility
- **Modern browsers**: Chrome, Firefox, Safari, Edge
- **Mobile browsers**: Works on iOS Safari, Android Chrome
- **JavaScript required**: Application won't work with JS disabled
- **localStorage support**: Required for data persistence

### Data Storage
- **Format**: JSON objects stored in browser localStorage
- **Keys**: `kaizen-YYYY-MM-DD` for daily entries
- **Special keys**:
  - `manual-streak`: Manual streak override
  - `streak-audit-log`: Audit trail for streak changes
  - `pdf-uploads`: Upload history metadata

### Security Considerations
- **Client-side only**: No data leaves your device unless you explicitly export
- **No tracking**: No analytics, no external requests (except CDN for PDF library)
- **Local network only**: Server only binds to local network, not internet
- **File validation**: Strict checks on uploaded PDFs

## 🎨 Design Philosophy

### Paper Journal Aesthetic
- **Black and white**: Clean, minimal color scheme
- **Serif fonts**: Times New Roman for authentic feel
- **Lined paper**: Background lines in reflection section
- **Clean spacing**: Lots of whitespace for readability

### User Experience
- **No learning curve**: Immediate intuitive use
- **Auto-save**: Never lose your work
- **Fast loading**: No external dependencies (except PDF library)
- **Offline capable**: Works without internet connection

## 🔧 Customization

### Quotes
- Edit the `quotes` array in `script.js` to add your own motivational quotes
- Each quote object needs `text` and `author` properties

### Styling
- Modify `style.css` to change colors, fonts, or layout
- The design uses CSS custom properties for easy theming

### Functionality
- All functions are well-documented and modular
- Core functions available via `window.debugFunctions` for console access

## 🐛 Troubleshooting

### Server Won't Start
- **Port in use**: Try a different port number
- **Permission denied**: On some systems, use `sudo python3 start_server.py`
- **Python not found**: Ensure Python 3 is installed

### Can't Access from Other Devices
- **Same network**: Ensure all devices on same WiFi
- **Firewall**: Check if firewall is blocking the port
- **IP address**: Verify the IP address is correct

### Data Not Saving
- **localStorage disabled**: Check browser privacy settings
- **Private/incognito mode**: Data won't persist in private browsing
- **Storage full**: Clear other website data if localStorage is full

### PDF Upload Issues
- **File format**: Ensure file is actually a PDF
- **Filename**: Check filename matches expected patterns
- **File size**: Files must be under 10MB

## 📋 Keyboard Shortcuts

- **Tab**: Navigate between form fields
- **Enter**: In text inputs moves to next field
- **Space**: Toggle checkboxes when focused
- **Escape**: Close modal dialogs

## 🔮 Future Enhancements

Potential features for future versions:
- **Data export**: JSON backup/restore functionality
- **Theme options**: Dark mode, color themes
- **Calendar view**: Monthly overview of streaks
- **Goal tracking**: Long-term goal progress
- **Habit tracking**: Additional recurring tasks
- **Cloud sync**: Optional cloud storage integration

---

## 📄 License

This project is open source. Feel free to modify and adapt for your needs.

## 🙏 Acknowledgments

Built with inspiration from the Kaizen philosophy of continuous improvement. 

**"A journey of a thousand miles begins with a single step."** - Lao Tzu