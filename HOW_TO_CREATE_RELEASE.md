# How to Create a GitHub Release

Since the `gh` CLI tool isn't installed, here's how to manually create the v1.0.1 release on GitHub:

## Steps

1. **Go to GitHub Repository**
   - Navigate to: https://github.com/caseyfarina/eventGameToolKit

2. **Click "Releases"**
   - On the right sidebar, click "Releases" (or go to https://github.com/caseyfarina/eventGameToolKit/releases)

3. **Click "Draft a new release"**
   - Button in the top right

4. **Fill in Release Information**

   **Tag version:** `v1.0.1`
   - Click "Create new tag: v1.0.1 on publish"

   **Release title:** `Event Game Toolkit v1.0.1`

   **Description:** Copy the entire contents of `RELEASE_NOTES_v1.0.1.md` and paste into the description box

5. **Set as Latest Release**
   - Check the box "Set as the latest release"

6. **Publish Release**
   - Click "Publish release"

## What This Does

- Creates a git tag `v1.0.1` pointing to the current commit
- Creates a downloadable ZIP of the source code at this version
- Makes the release notes visible to students
- Provides a permanent link students can reference

## After Publishing

Students can then:
- Download the ZIP from the releases page
- Install via git URL (will get v1.0.1)
- See changelogs between versions

## Future Releases

For version 1.0.2, 1.1.0, etc:
1. Update version number in `package.json`
2. Update `CHANGELOG.md` with changes
3. Commit and push
4. Create new release following same steps above with new version number
