# CSS Generators Testing

## Project Description
I tested a web platform that provides different CSS/UI generators. 

The goal was to check how the application behaves in real user scenarios, including navigation, generator functionality, and UI behavior.

---

## What I tested
- Navigation between pages and generators  
- Generator inputs and outputs  
- UI elements and layout  
- Responsive behavior (desktop and mobile)  
- Edge cases (large input values)

---

## Testing approach
I mainly used exploratory testing, focusing on how a real user would interact with the product.

Also checked:
- UI consistency  
- Basic functionality  
- Behavior under unusual inputs  

---

## Environment
- Chrome (desktop)  
- Mobile browser  
- DevTools  

---

## Bugs I found
During testing I found several issues:

- Navigation issue (page didn’t always switch after using some generators)  
- Intermittent 502 Bad Gateway error  
- UI bug (arrow / element misalignment)  
- Text overflow on mobile  
- Animation disappearing on extreme values  

Detailed reports are in the /bug-reports folder.

---

## Test artifacts
- Bug reports → /bug-reports  
- Test cases → /test-cases  
- Checklist → /checklists  

---

## Notes
- Some behaviors looked strange but were confirmed as “by design”  
- Most core features worked stable under normal usage  
- Issues mainly appeared in edge cases and UI  

---

## Result
Overall, the application works stable for typical usage, but there are some UI issues and edge-case behaviors that can be improved.

---

## About me
Junior QA Engineer focused on manual testing and real user scenarios.
