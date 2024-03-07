---
title: MuseScore Usage Guide
summary: "MuseScore Usage Guide: A Personal Collection of Miscellaneous Tips"
authors: [Ville Langén]
tags: []
categories: []
date: '2024-03-06T00:00:00Z'
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: black
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  highlight_style: dracula
---

# MuseScore Usage Guide: A Personal Collection of Miscellaneous Tips


---

## Getting Started

**First and foremost:** If you've never used MuseScore before, it's advisable to watch a quick tutorial video that demonstrates how to:

- Enter notes
- Delete notes
- Modify notes

For that, I recommend [this video](https://www.youtube.com/watch?v=Pw9X1y_pLko) in the Musician Startup YouTube channel.

---

## Hearing Notes with MIDI

To listen to notes in MuseScore, you will hear played music through sounds called MIDI. However, it's essential to note that on at least MacOS, my experience suggests that MIDI might not function properly without an internet connection. So make sure that your internet connection is running at all times.

---

## Adding Notes

- Ensure you are in note input mode (shortcut: N)
- Move forward with the right arrow key or the number 0
- Press numbers 1-7 to indicate note duration
- Press the desired note (e.g., "D")
- If the note is too high in pitch, press Cmd+down arrow to lower the octave

---

## Adding Chords

- Select the note where you want to add the chord symbol, then Ctrl+K (MacOS: Cmd+K)
- Manually input C, D, E, F, G, A, or B, followed by:
    - Sharp: #
    - Flat: b
    - Double sharp: x or ##
    - Double flat: bb
    - Natural: Ctrl+Shift+H
- Press Esc when you're done

---

## Reducing Measures If the Song Is Too Long

- Select the measures
- Press Cmd+Del

---

## Adding an Instrument

- Press "I"

---

## How to Fit the Entire Score on One Page

- Go to Format → Page Settings
- Choose Scaling: Staff space (sp)

For more essential information on this topic, check out:

[https://www.youtube.com/watch?v=TprrHgmHg6E](https://www.youtube.com/watch?v=TprrHgmHg6E)

---

## Issue with Exporting as MP3

When exporting a song, such as to MP3 format, some instruments may disappear. The reason for this is that certain instruments, such as the Piano channel, cannot contain a Sine Wave Expr. sound type; it must be a plain Sine Wave.

---

## Creating a Hotkey for Rewinding

To enable quick rewinding, it's highly recommended to set up a hotkey.

1. Go to Preferences → Shortcuts ("Player: rewind").
2. Create a custom hotkey for this function.

For further discussion on this topic, visit:

[https://musescore.org/en/node/285182](https://musescore.org/en/node/285182)

---

## Using Wikipedia Images for Reference

If you need to work with bass clef notes on the piano's left hand and haven't memorized which note corresponds to which sound, you can use the image found at the following link from Wikipedia as a reference:

[Wikipedia Bass Clef Image](https://en.wikipedia.org/wiki/Clef#/media/File:Clef_Diagram.png)

---

## Selecting/Extracting Notes for a Single Instrument

1. Go to File → Parts → Single Part
2. Choose the instrument you want to select/extract

---

## Deleting the Bass Clef Section for Piano

1. Press "I" to open the instrument dialog
2. Click on staff 2 in the piano section
3. Click the "Remove" button in the middle of the box
4. Click "OK"

---

## Changing from Alto Saxophone to Tenor Saxophone

Simply change the instrument as follows:

- Right-click on the staff → "Staff Properties"
- Click on "Change Instrument"
- Choose "Tenor Sax"

When necessary, you can easily transpose notes back as follows:

- Select "Notes" → "Transpose"

---

## Selecting All Chord Symbols

To select all chord symbols:

- Place the cursor on a chord symbol
- Right-click
- Choose "Select Similar"

---

## Adjusting Dynamics for Each Note

If importing a MIDI file brings dynamics for each note, and this is bothersome, you can proceed as follows:

- Open the Inspector (F8 or View → Inspector)
- Right-click on any note
- Select → Select All Similar Elements
- In the Inspector view, under the Note section, find "Velocity Type" and "Velocity"
- Reset both "Velocity Type" and "Velocity" to default

---

## Keep Exploring!

I hope these tools give you a little jumpstart as you continue to explore and create in MuseScore. Happy composing!
