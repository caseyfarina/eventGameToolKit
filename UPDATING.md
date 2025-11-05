# How to Update Event Game Toolkit

This guide shows students how to safely update the Event Game Toolkit to get new features and bug fixes.

---

## ✅ Will My Work Be Safe?

**Yes!** When you update the toolkit:

✅ **All your GameObjects keep their components**
✅ **All your settings and values are preserved**
✅ **All your UnityEvent connections stay intact**
✅ **All your scenes and prefabs work normally**

The only thing you'll lose is any custom modifications you made to the toolkit scripts themselves.

---

## 📦 Two Installation Methods = Two Update Methods

### If You Installed via Git URL (Package Manager)

**How to Tell:** Look in Unity's Project window. If you see the toolkit under **"Packages"** (not Assets), you used this method.

**How to Update:**

1. Open **Window > Package Manager**
2. Find **"Event Game Toolkit"** in the list
3. If an update is available, click the **Update** button
4. Wait for Unity to re-import
5. Done! ✨

**Easy mode!** Package Manager handles everything automatically.

---

### If You Installed to Assets Folder (Editable)

**How to Tell:** Look in Unity's Project window. If you see **"Assets/eventGameToolKit/"** folder, you used this method.

**How to Update:**

Follow these steps carefully to avoid losing your work:

#### Step 1: Backup Your Project (Recommended)

Before updating, make a backup:

1. Close Unity
2. Copy your entire project folder to a safe location
3. Or commit your work to git if you're using version control

**Why?** Just in case something goes wrong, you can restore your backup.

#### Step 2: Download the New Version

1. Go to the [Event Game Toolkit Releases](https://github.com/caseyfarina/eventGameToolKit/releases)
2. Find the latest version
3. Click **"Source code (zip)"** to download
4. Extract the ZIP file to a temporary location

#### Step 3: Replace the Old Folder

**Option A: Unity Closed (Safest)**

1. **Close Unity completely**
2. Navigate to your project folder on your computer
3. Go to `Assets/eventGameToolKit/`
4. **Delete the old `eventGameToolKit` folder**
5. **Copy the new folder** from the extracted download
6. Make sure it's named `eventGameToolKit` (not `eventGameToolKit-main` or similar)
7. **Open Unity**
8. Unity will re-import everything (may take a minute)
9. Check the Console for any errors

**Option B: Unity Open**

1. In Unity's Project window, **right-click** the `Assets/eventGameToolKit` folder
2. Select **Delete**
3. Confirm deletion
4. Drag the new `eventGameToolKit` folder from Windows Explorer into your `Assets/` folder
5. Unity will re-import automatically
6. Check the Console for any errors

---

## 🔍 Verify the Update Worked

After updating, check these things:

### 1. Check Version Number

Look at the top of the README file in the toolkit folder. It should show the new version number.

### 2. Test Your Scenes

1. Open one of your existing scenes
2. Press **Play**
3. Make sure everything works as expected
4. Check that your UnityEvents still trigger correctly

### 3. Check Console for Errors

Open **Window > Console** and make sure there are no red error messages.

---

## ⚠️ Troubleshooting

### "Missing Script" Warnings

**Problem:** Some GameObjects show "Missing Script" in the Inspector.

**Cause:** A script was renamed or removed in the update.

**Fix:**
1. Check the [CHANGELOG.md](CHANGELOG.md) to see if any scripts were renamed
2. Remove the missing script component
3. Add the new version of the component
4. Reconfigure settings (you may need to redo some work)

---

### "Script Could Not Be Compiled" Errors

**Problem:** Console shows compilation errors.

**Cause:** Update process didn't complete properly.

**Fix:**
1. Close Unity
2. Delete the `Library/` folder in your project (Unity will rebuild it)
3. Open Unity and wait for re-import to complete

---

### Old Version Still Shows After Update

**Problem:** README still shows old version number after updating.

**Cause:** Old files weren't fully deleted.

**Fix:**
1. Close Unity
2. Manually delete `Assets/eventGameToolKit/` completely
3. Re-copy the new version
4. Open Unity

---

## 📋 Update Checklist

Use this checklist when updating:

- [ ] Backup project (copy project folder or commit to git)
- [ ] Download latest release from GitHub
- [ ] Extract ZIP to temporary location
- [ ] Close Unity (if using Option A)
- [ ] Delete old `Assets/eventGameToolKit/` folder
- [ ] Copy new folder into `Assets/`
- [ ] Ensure folder is named `eventGameToolKit` (not `eventGameToolKit-main`)
- [ ] Open Unity (if it was closed)
- [ ] Wait for import to complete
- [ ] Check Console for errors
- [ ] Test one of your scenes in Play mode
- [ ] Verify version number in README

---

## 🆕 What's New?

Always check [CHANGELOG.md](CHANGELOG.md) after updating to see:

- New components added
- Bug fixes
- Improvements to existing components
- Breaking changes (rare, but important to know)

---

## 🆘 Still Having Issues?

If something goes wrong:

1. **Restore your backup** to get back to working state
2. **Check CHANGELOG.md** for breaking changes
3. **Contact your instructor** for help
4. **Report the issue** on GitHub with details about what went wrong

---

## 💡 Pro Tips

### Version Control Users (Git)

If you're using git for your project:

```bash
# Before updating
git add .
git commit -m "Before updating Event Game Toolkit"

# After updating, if it works
git add .
git commit -m "Updated Event Game Toolkit to v1.x.x"

# If something breaks, revert
git reset --hard HEAD~1
```

### Keep Notes

When you update, write down:
- What version you updated from
- What version you updated to
- Any issues you encountered
- How you fixed them

This helps if you need to troubleshoot later!

---

## 📌 When Should I Update?

**Update when:**
- Your instructor announces a new version
- You need a bug fix for an issue you're experiencing
- You want to use a new feature mentioned in the CHANGELOG

**Don't update when:**
- You're in the middle of a critical deadline
- Your project is working perfectly and you don't need new features
- Right before a presentation or submission

**Best time to update:** Start of a new project milestone, after you've backed up your work.

---

## 🎓 Remember

Updating is usually safe and smooth! The toolkit is designed to preserve your work. Just:

1. **Always backup first**
2. **Read the CHANGELOG**
3. **Test after updating**

You've got this! 💪
