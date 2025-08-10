# Deployment Guide

This guide will help you deploy your Study Tracker to GitHub Pages.

## Quick Setup

### 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., "study-tracker" or "checklist")
5. Make sure it's set to "Public"
6. Click "Create repository"

### 2. Upload Your Files

You can upload files in two ways:

#### Option A: Using GitHub Web Interface
1. In your new repository, click "uploading an existing file"
2. Drag and drop all the files from your local folder
3. Add a commit message like "Initial commit"
4. Click "Commit changes"

#### Option B: Using Git Commands
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/your-repo-name.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"

### 4. Access Your Live Site

After a few minutes, your site will be available at:
```
https://yourusername.github.io/your-repo-name
```

## Features Included

✅ **Persistent Storage**: Your progress is saved automatically in your browser
✅ **Progress Statistics**: Visual progress bar and completion counters
✅ **Export/Import**: Backup and restore your progress
✅ **Responsive Design**: Works on desktop, tablet, and mobile
✅ **Reset Functionality**: Clear all progress with confirmation
✅ **Celebration Animation**: Visual feedback when all tasks are completed

## Customization

### Adding New Tasks
1. Open `index.html`
2. Find the section where you want to add tasks
3. Copy an existing task structure:
```html
<label for="task-new" class="flex items-center space-x-3 bg-indigo-50 p-4 rounded-lg cursor-pointer hover:bg-indigo-100 transition-colors duration-200">
    <input type="checkbox" id="task-new" class="form-checkbox h-5 w-5 text-indigo-600 rounded focus:ring-indigo-500 transition duration-150 ease-in-out">
    <span class="text-gray-700 font-medium flex-1">Your new task description</span>
</label>
```
4. Make sure to give each task a unique `id`

### Changing Colors
The tracker uses Tailwind CSS classes. You can modify colors by changing class names:
- `text-indigo-600` → `text-blue-600` (for blue)
- `bg-indigo-50` → `bg-green-50` (for green backgrounds)
- `border-indigo-200` → `border-purple-200` (for purple borders)

### Adding New Sections
1. Copy an existing section structure
2. Update the heading and tasks
3. Make sure all task IDs are unique

## Troubleshooting

### Site Not Loading
- Wait 5-10 minutes after enabling GitHub Pages
- Check that your repository is public
- Ensure `index.html` is in the root directory

### Progress Not Saving
- Make sure JavaScript is enabled in your browser
- Check browser console for errors (F12 → Console tab)
- Try clearing browser cache and reloading

### Mobile Issues
- The site is responsive and should work on all devices
- If you have issues, try refreshing the page

## Support

If you encounter any issues:
1. Check the browser console for error messages
2. Ensure all files are properly uploaded
3. Verify GitHub Pages is enabled correctly
4. Try accessing the site in an incognito/private browser window

## Updates

To update your tracker:
1. Make changes to your local files
2. Upload the updated files to GitHub (overwrite existing ones)
3. Changes will be live within a few minutes

Your progress data is stored locally in your browser, so updates won't affect your saved progress.
