# FAQ

### Where are my presets stored?
On your device, in the Tasker global variable `%PresetTasks`, as JSON. Nothing is sent anywhere.

### How do I back up my presets?
Open **Backup** → **Export** → **Copy all presets**, then paste the text somewhere safe (a note, a file, a message to yourself).

### How do I move my presets to another device?
Export on the old device. On the new one, open **Backup** → **Import**, paste, and choose **Add to existing**.

### I only want to share a few presets.
Tap the **Select** icon, pick the presets, and tap **Export selected**. Whoever receives the text can paste it into **Backup → Import**.

### Import says the text isn't valid.
Make sure you copied the **whole** export, from the first `[` (or `{`) to the last `]` (or `}`). Messaging apps sometimes cut long text or change quotation marks.

### Some presets were skipped when I imported.
Presets need a **name**. Any without one are skipped.

### What's the difference between "Add to existing" and "Replace all"?
**Add to existing** keeps your current presets and adds the pasted ones. **Replace all** deletes your current presets and uses only the pasted ones, so export a backup first.

### I deleted a preset by mistake.
Tap **Undo** right after deleting. If it's gone, restore it from a backup with **Backup → Import**.

### What does priority do?
It is a number from 1 to 50 used to prioritize tasks by tasker, shown as Low (1–17), Mid (18–34) or High (35–50). Tap the **?** next to **Priority** in the editor for a reminder, and use the priority filter and sort to find presets by importance.

### Why can't I change the Author?
The author is set when a preset is created and is read-only afterwards.

### Something doesn't work.
[Open an issue](../../../../issues) and include your Tasker version, Project version, Plugin version and what you did.
