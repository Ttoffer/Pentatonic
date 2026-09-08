Pentatonic Scales (guitar)
==========================

A browser app for major and minor pentatonic scales on guitar. You pick a key
from a circle of fifths, see the notes on a six-string fretboard, and work with
the five CAGED boxes so you can start in one position and walk to the next
related pattern up the neck.

Live site (when GitHub Pages is on):
  https://ttoffer.github.io/Pentatonic/

It is a single static page. There is no server, no account, and no tracking.
Open index.html in a browser, or use any static host. Sound needs a tap first
on some phones (the browser only starts audio after you interact).


1. What you see
---------------

Header
  Major / Minor pentatonic
  Pattern overlay, Five CAGED boxes, show-only-pattern, older presets
  Degree labels, string flip (low E at the bottom, like TAB)
  Current key

Five patterns (CAGED)
  Five small diagrams: Pattern 1 to 5 (E, D, C, A, G shapes)
  How many boxes to show: This pattern, This + next, Three in a row,
  Four in a row, Five in a row
  Previous / Next box along the neck
  Example: E minor open → fret 5
  Overlay: Pull-off pairs

Circle (left)
  Twelve keys in fifths order. Tap a key to set the root and hear that pitch
  on the low E string.

Fretboard (right)
  Standard tuning E A D G B E, 22 frets. Tap a labelled note or an empty
  fret to hear that string and fret.

iPhone / iPad
  The phone-shaped button explains Add to Home Screen in Safari.


2. Choosing a key and scale
---------------------------

Major pentatonic notes from the root:  1  2  3  5  6
Minor pentatonic notes from the root:  1  b3  4  5  b7

Colours match those degrees on the circle legend and on the fretboard pills.

The circle is arranged in fifths (C, G, D, A, E, …). The current root is
yellow. Other notes in the pentatonic are highlighted.

Relative major / minor use the same five notes (C major pentatonic = A minor
pentatonic). The app still numbers Pattern 1 from the tonic of the mode you
picked: Pattern 1 always has that tonic on the low E string.


3. The five CAGED boxes
-----------------------

Each key has five connected pentatonic boxes up the neck. They overlap. The
notes at the edge of one box are the start of the next. That is how you move
instead of jumping.

Numbering (for the mode you have selected):

  Pattern 1  E shape   home box (tonic on the low E)
  Pattern 2  D shape
  Pattern 3  C shape
  Pattern 4  A shape
  Pattern 5  G shape   then it wraps back to Pattern 1 an octave higher

Minor example, E minor:
  Pattern 1 sits at the open strings (frets 0–3)
  Pattern 2 continues around frets 2–5
  Shared notes around frets 2–3 are the join

Major example, C major:
  Pattern 1 (tonic C on the low E) sits around frets 7–10
  Pattern 2 follows around frets 9–13

Click a pattern card to start there. The fretboard highlights that box.

How many to show
  This pattern     one box
  This + next      start box plus the next one up the neck (the usual link)
  Three in a row   start plus the next two
  Four in a row    start plus the next three
  Five in a row    all five CAGED boxes (the full series)

  Adding a pattern (This → This + next → Three → Four → Five) pulses the new
  box’s notes brighter for about three seconds, then they settle back.

  The chain always walks up the neck. If a later box would otherwise appear
  nearer the nut (for example C major Pattern 4 at frets 2–5), it is shown
  an octave higher so it joins the previous box (14–17 in that example).

Previous / Next box moves the starting pattern. After Pattern 5 the next
start is Pattern 1 (higher up the neck).

Example button
  Sets E minor, Pattern 1, This + next, so you see the open box linked to
  the box that reaches fret 5.

On the big fretboard
  Coloured bands mark each box in the chain
  Full colour = notes in the chain
  Dashed ring = notes that belong to two boxes (the join)
  Dimmed notes = in the scale but not in the selected boxes
  Soft gold roots remain as hints when they sit outside the chain

Turn off “Five CAGED boxes” if you want the older presets instead
(Low E root, A-string root, or a 3-fret CAGED window).


4. Pull-off pairs
-----------------

Optional overlay on the selected boxes. On each string, a PO mark appears
only when two pentatonic notes sit a whole step apart — one unused (middle)
fret between them. The higher fret pulls off to the lower fret (including
open strings).

There is no pull-off when two frets sit between the notes (the 3-fret
stretch, such as open E or B in E minor Pattern 1: 3 to 0). Those outer
strings are skipped; the middle strings (A, D, G) keep the 2-to-0 pairs.

With This + next, extra whole-step pairs appear where the next box adds a
note two frets from one you already have (for example 5 to 3 on the E
strings).


5. Other fretboard controls
---------------------------

Pattern overlay
  When on, notes in the selected pattern/boxes stand out; others dim.

Show only pattern notes
  Hides the dimmed scale notes. Root hints and gold root guide lines stay.

Show degree labels
  Adds 1, 2, 3, 5, 6 (major) or 1, b3, 4, 5, b7 (minor) on each pill.

Low E at bottom
  Default on, like TAB (high E at the top). Uncheck to put low E at the top.

Older presets (only matter if Five CAGED boxes is off)
  Low E root / A string root were early partial patterns
  CAGED windows were 3-fret slices rather than full 2-notes-per-string boxes


6. Sound
--------

Notes are synthesised in the browser (a short plucked tone). Nothing is
downloaded. Circle taps play the key on the low E at a comfortable fret.
Fretboard taps play the exact string and fret (open E2 up through high E
plus 21).


7. iPhone and iPad
------------------

Use Safari (not Chrome) to add an icon to the Home Screen.

1. Open Safari and go to https://ttoffer.github.io/Pentatonic/
2. Tap Share (square with an arrow)
3. Tap Add to Home Screen
4. Name it if you like, then Add

You get a full-screen icon without the address bar. Repeat on each device.
If an update looks stale, delete the old shortcut and add it again.


8. Files in this folder
-----------------------

  index.html            The whole app (HTML, CSS, and JavaScript)
  README.txt            This guide
  README.md             Short GitHub Pages / Home Screen notes
  manifest.webmanifest  Name, theme, standalone display
  apple-touch-icon.png  Home Screen icon

There is also an iOS wrapper in the parent folder (Swift) that can load the
same web page.


9. Suggested first run
----------------------

1. Open index.html (or the live GitHub Pages URL).
2. Click “Example: E minor open → fret 5”.
3. Leave “This + next” on. Look at Pattern 1 (open) joining Pattern 2
   around fret 5. Dashed rings are the shared notes.
4. Click Five in a row to see the full CAGED series up the neck, then Previous /
   Next to walk the chain.
5. Turn on Pull-off pairs and play the PO links on each string.
6. Switch to Major pentatonic and pick C on the circle to see Pattern 1
   sitting around the 8th fret (C on the low E).


Privacy
-------

Runs only in your browser. No accounts, analytics, or server calls.
