# Upload System Setup Guide

## Folder Structure Created

```
public/
├── uploads/
│   ├── intro/           # Place intro videos here
│   ├── assignments/     # Place assignment files here
│   └── README.md        # Instructions
└── uploads-metadata.json # Configuration file
```

## How to Use

### Step 1: Add Your Files

1. **For Introduction Video:**
   - Place your video file in: `public/uploads/intro/`
   - Supported formats: MP4, WebM, Ogg, etc.
   - Example: `public/uploads/intro/intro.mp4`

2. **For Assignment:**
   - Place your file in: `public/uploads/assignments/`
   - Supported formats: PDF, DOC, DOCX, etc.
   - Example: `public/uploads/assignments/assignment.pdf`

### Step 2: Enable Files in Metadata

Edit `public/uploads-metadata.json`:

```json
{
  "introVideo": {
    "enabled": true,                    // Change to true
    "filePath": "/uploads/intro/intro.mp4",
    "fileName": "intro.mp4",
    "title": "Introduction Video"
  },
  "assignment": {
    "enabled": true,                    // Change to true
    "filePath": "/uploads/assignments/assignment.pdf",
    "fileName": "assignment.pdf",
    "title": "My Assignment"
  }
}
```

### Step 3: Supported Formats

**Videos:**
- MP4 (.mp4)
- WebM (.webm)
- Ogg (.ogv)
- MOV (.mov)

**Assignments:**
- PDF (.pdf)
- Word Documents (.doc, .docx)
- Text Files (.txt)
- Excel (.xls, .xlsx)
- Images (.jpg, .png, .gif)

### Features

✅ **Upload from Browser** - Use the upload buttons to select files
✅ **Static Files** - Pre-configure files in the public folder
✅ **Dual Support** - Supports both upload methods simultaneously
✅ **Download** - Users can download assignment files
✅ **Video Player** - Built-in video player with controls
✅ **Responsive** - Works on desktop and mobile
✅ **Automatic Loading** - Files load automatically on page load

### Upload Button Status

- **Before upload/configuration:** "Upload Intro Video" / "Upload Assignment"
- **After upload/configuration:** "Video Uploaded ✓" / "Assignment Uploaded ✓"

### Example Workflow

1. Copy `intro.mp4` to `public/uploads/intro/`
2. Copy `assignment.pdf` to `public/uploads/assignments/`
3. Update `public/uploads-metadata.json` with `"enabled": true`
4. Files automatically appear on your portfolio
5. Visitors can view video and download assignment

### Tips

- Keep file sizes reasonable (videos < 100MB recommended)
- Use compression tools if files are too large
- File names should not contain special characters
- Test the metadata JSON for valid syntax
- Use descriptive file names for better UX
