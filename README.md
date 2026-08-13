# Daniel Schnurbusch

Solo game developer. Unity and C#.

I ship games, then cut the reusable parts out of them and publish those as tools. Everything
below started as a problem in a game I actually finished, not as a product idea.

## Tools on the Unity Asset Store

| | |
|---|---|
| **[ChipForge](https://assetstore.unity.com/packages/tools/audio/chipforge-procedural-retro-sfx-music-zero-audio-files-386476)** | Chiptune SFX and looping music synthesized at runtime. No audio files in the build at all. |
| **[LocLayer](https://assetstore.unity.com/packages/tools/localization/loclayer-localize-without-refactoring-394954)** | Localization as a layer over your existing UI. No keys, no wrapper calls, no rewrite. |
| **[HintOnce](https://assetstore.unity.com/packages/tools/gui/hintonce-first-time-hints-with-one-line-of-code-396738)** | First-time hints in one line of code. No prefab, no canvas, no manager. Free. |
| **PortraitFit** | Portrait WebGL template with a setup window. In review. |

Full C# source in every one of them. No DLLs, no dependencies beyond what Unity ships.

## The game they came from

**[Famechaser](https://schnurbusch.itch.io/famechaser)**, a streaming simulation, playable in
the browser. Portrait, mobile friendly, fully localized, and it does not ship a single authored
audio file.

## A few things I learned doing it

- Never use `??` or `?.` on a `UnityEngine.Object`. A missing component is "fake null", so the
  operator hands you a broken reference and the crash lands far from the cause.
- Generate audio at the device sample rate. At 44100 Hz on a 48000 Hz device you get silence
  rather than a wrong pitch, and only on some hardware.
- Every file in a WebGL template folder is copied into your build, including the README you
  forgot to remove.

## Elsewhere

[schnurbusch.github.io](https://schnurbusch.github.io) · [itch.io](https://schnurbusch.itch.io) · daniel.schnurbusch@web.de
