---
name: IO Linker
description: Integrates natural language commands with IFTTT Webhooks and Apple Shortcuts.
---

# Instructions
Use this skill when the user wants to automate an action, control a smart home device, or run a workflow on their iPhone.

1. **Analyze the Intent**:
   - If the user mentions "home", "lights", "smart device", or "IFTTT", target the **IFTTT** integration.
   - If the user mentions "shortcut", "workflow", "iOS", or specific app actions (e.g., "add reminder", "play music"), target the **Apple Shortcuts** integration.

2. **Extract Data**:
   - **Event/Shortcut Name**: The specific key or name of the shortcut (e.g., `turn_lights_on`, `MorningRoutine`).
   - **Payload**: A generic string of data to pass (optional).

3. **Action**:
   - Call the `run_js` tool.
   - Pass a JSON object with: `{ "target": "ifttt" | "shortcuts", "name": "<extracted_name>", "payload": "<extracted_data>" }`.

4. **Fallback**:
   - If the user has not provided their IFTTT Key in the chat context previously, ask for it or provide instructions on how to hardcode it in `index.html`.
