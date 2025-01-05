# Game-Patches
Games patches I wrote. Currently focused on Burnout Paradise.

## Introduction
I'm still learning Reverse Engineering with IDA Pro, so it might only be small changes for now, and maybe not done in the best way, but this can only improve in the future 😊

## Patches
In the `BURNOUT_ARTIST.XEX` executable of the [Jan 30,2008 prototype](https://hiddenpalace.org/Burnout_Paradise_(Jan_30,_2008_prototype)) of Burnout Paradise
###  Disable Performances Monitors 🟥🟩🟩
Disable the FPS counter as well as the three thread monitors.

<table align="center">
    <tr>
        <td>
            <h2 align="center">Before</h2>
            <img src="https://github.com/user-attachments/assets/e527da13-4540-4cb6-9f3b-e4dc8bc6b0cd">
        </td>
    </tr>
    <tr>
        <td>
            <h2 align="center">After</h2>
            <img src="https://github.com/user-attachments/assets/40fe3199-7a15-41de-b0a2-b4f9cba9dfaf">
        </td>
    </tr>
</table>

### Increased Cars LODs Distance

Increase the LODs distance for the vehicles including traffic. Multiple patch versions are available to balance between performance and visual quality:

- **Ultra:** Maximum quality with 5x increase. May affect game performance on some systems.
- **High:** Significant quality boost with higher LOD distances.
- **Medium:** Balanced option for improved visuals without substantial performance loss.
- **Low:** Lower LOD distances for better performance, suitable for systems struggling to maintain 60 FPS.
- **Potato:** Minimal LOD distances for maximum performance at the cost of visual quality.

⚠️ **Warning**: The `High` and `Ultra` patches can greatly affect the game performance depending on how you run the game without the patch. And higher values than 5x (which is ultra here) can greatly decrease the performance even on high-end hardware: the game is not optimized for this.

<table align= "center">
  <tr>
    <td width="50%">
      <h2 align="center">Before Ultra</h2>
        <img src="https://github.com/user-attachments/assets/09656ff0-828c-4473-8e7f-fcf7c595e91c">
    </td>
    <td width="50%">
      <h2 align="center">After Ultra</h2>
        <img src="https://github.com/user-attachments/assets/1c8c5a4a-7a02-48eb-842f-2f34188808c3">
    </td>
  </tr>
</table>

### Forced Random Soundtrack Play Order
By default, the game plays the soundtrack in the sequential order, and if you change your settings to random and relaunch the game, it default back to sequential. This is a problem with all user settings, not just play order (I plan to fix this). This patch forces the game to play the songs in a **random order** *regardless of the settings*.