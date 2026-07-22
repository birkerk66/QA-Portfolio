## TC-002: Verify Dynamic CSS Preview Updates and Code Copy Functionality

**Component:** Functional / CSS Generators  
**Preconditions:** 
* User is on the homepage (`https://css-zone.com/`).

### Test Steps:
1. Select and open any generator tool (e.g., *Gradient Generator*).
2. Modify generator input controls (change color pickers, adjust angle sliders, edit numerical inputs).
3. Observe the real-time visual preview canvas.
4. Verify the generated CSS code block output.
5. Click the **"Copy Code"** action button.

### Expected Result:
* Visual preview updates immediately without UI delay or screen flickering upon value change.
* Generated CSS snippet dynamically updates to match the configured parameters.
* Clicking "Copy Code" copies the valid CSS string to the system clipboard.
* No browser performance freezing or UI hanging occurs during interaction.

### Postconditions:
* Valid CSS output resides in the user's clipboard ready for pasting.
