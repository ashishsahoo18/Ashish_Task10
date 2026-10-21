# TuteDude MERN Stack – Task: CSS Laundry Services Adding Animation to the Hero Image

## Files Included
- `index.html` – HTML structure
- `style.css` – CSS with keyframe animations
- `README.md` – This file

## How to Run
1. Unzip the folder.
2. Open `index.html` in Chrome or Firefox.
3. Watch the hero image on the right move in an orbit and get squeezed.

## Animations Used

| Animation | Applied To | Effect |
|-----------|-----------|--------|
| `orbit`   | `.orbit` (wrapper div) | Image travels in a circular path (6s, infinite) |
| `squeeze` | `.orbit img` | Image gets squeezed and stretched at certain points (3s, infinite) |

## How the Orbit Works
```css
@keyframes orbit {
  from { transform: rotate(0deg) translateX(25px) rotate(0deg); }
  to   { transform: rotate(360deg) translateX(25px) rotate(-360deg); }
}
```
The element is rotated, pushed outwards, then rotated back by the same amount.
This makes the image travel in a circle while staying upright.

## How the Squeeze Works
```css
@keyframes squeeze {
  0%   { transform: scale(1, 1); }
  25%  { transform: scale(0.9, 1.1); }
  50%  { transform: scale(1.1, 0.9); }
  75%  { transform: scale(0.92, 1.08); }
  100% { transform: scale(1, 1); }
}
```
`scale(x, y)` changes width and height separately, which creates the squeeze effect.

Two animations are used on two different elements (wrapper and image) so
their `transform` values do not override each other.

## Requirements Completed
- Image moves in an orbit rotation
- Image gets squeezed at certain points
- Animation runs forever (`infinite`)
- Responsive: smaller orbit on tablet and mobile
- Hover effect on button and hamburger menu kept from previous tasks
- No JavaScript, no Bootstrap
- CSS properly linked to HTML

## Submission
1. Put all 3 files in one folder (e.g. `YourName_Task10/`)
2. Compress to `.zip`
3. Rename to `YourName_Task10.zip`
4. Upload the ZIP and deployed link on the TuteDude portal