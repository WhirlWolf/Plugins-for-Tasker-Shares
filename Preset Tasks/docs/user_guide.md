# User guide

## The preset list

Your presets are listed with a coloured initial, the name, a short description, and small tags showing the **priority** (for example `P40`), the number of **params** and the number of **vars**.

| Control | What it does |
|---|---|
| **Sort** (list with a down arrow) | Cycles between your own order, by priority, and by name |
| **Select** (checkbox) | Starts bulk selection (see below) |
| **Backup** (up/down arrows) | Export / import (see below) |
| **Search** (magnifier) | Finds presets by name, ID or author |
| **All / Low / Mid / High** | Filters by priority: Low is 1–17, Mid is 18–34, High is 35–50 |
| **+** | Creates a new preset |

**Open** a preset by tapping it, or by swiping it to the left. **Go back** with the back button, or by swiping in from the left edge of the screen.

## Creating and editing a preset

Tap **+** to create one, or open an existing one. Fill in:

### Basic info
- **Name** – required. A preset without a name can't be saved.
- **ID** – a unique identifier, filled in from the name (you can change it). If it's already taken, a unique one is made when you save.
- **Description** – what the preset does.
- **Author** – set when you create the preset; read-only afterwards.

### Priority
A number from **1 to 50**, set with the slider or by typing. Higher means more important. The colour shows the group: green is Low, amber is Mid, red is High. Tap **?** next to the heading for a reminder.

### Parameters
Two parameters, **par1** and **par2**. For each one you can set a **Value**, a **Description**, a **Hint**, and whether it is **Required**.

### Return value variable
The variable the preset's result goes into, with its own description and hint.

### Pass variables
Extra named variables to hand to the preset. Tap **Add variable** for each one and fill in **Name**, **Value**, **Description**, **Hint** and **Required**. Names need at least three letters; the \`%\` is added for you.

### Saving
Tap **Save**. If you go back with unsaved changes, you're asked **Discard unsaved changes?** so you can't lose work by accident.

At the bottom of an existing preset you can **Duplicate** it (a quick way to start a variant) or **Delete** it. After deleting, an **Undo** button appears for a few seconds.

## Selecting several presets

1. Tap the **Select** icon.
2. Tap presets to select them. **Select all** selects everything that matches your current search and filter.
3. Use the bar at the bottom:
   - **Export selected** – opens the export window with only those presets
   - **Delete selected** – deletes them; **Undo** appears for a few seconds
4. Tap **Cancel** to leave selection mode.

## Backup, export and import

Tap **Backup** in the header.

**Export tab** – shows your presets as text. Tap **Copy all presets** to copy everything. To export only some, use **Export selected** in selection mode instead; the button then reads **Copy N selected presets**.

**Import tab** – paste exported text, then choose:
- **Add to existing** – adds the pasted presets to what you already have
- **Replace all** – deletes your current presets and uses only the pasted ones

> [!WARNING]
> **Replace all** can't be undone. Export your current presets first if you might want them back.

You can paste **one preset or a list of presets**. Presets without a name are skipped, priorities are kept within 1–50, and an imported preset whose ID is already used gets a new unique ID.

### Format

Presets are exchanged as JSON. A single preset looks like this:

```json
{
  "id": "send-notification",
  "name": "Send Notification",
  "desc": "Show a notification with a title and text",
  "author": "Example",
  "priority": 40,
  "returnValueVariable": { "value": "", "desc": "", "hint": "", "required": false },
  "par1": { "value": "%title", "desc": "Notification title", "hint": "", "required": true },
  "par2": { "value": "", "desc": "", "hint": "", "required": false },
  "passVariables": [
    { "name": "%icon", "value": "", "desc": "", "hint": "", "required": false }
  ]
}
```

An export is a list of these. Any extra internal fields you may see (such as `_id`) can be ignored.
