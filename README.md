# OBSIDIAN: Epoch to Flock - VR Prototype

An Urban Multimedia Opera - WebXR Experience

## Quick Start

### Testing on Desktop (Preview)
1. Open `index.html` in Chrome or Firefox
2. Click "ENTER EXPERIENCE"
3. Use mouse to look around, WASD to move
4. Look at the obsidian rock and click to interact

### Testing on Meta Quest (Full VR)

**Option 1: Local Development Server**
```bash
# Install a simple server (if you have Node.js)
npx serve .

# Or with Python
python -m http.server 8000
```
Then on your Quest:
1. Open the Oculus Browser
2. Navigate to `http://YOUR_COMPUTER_IP:8000`
3. Click "Enter VR" when prompted

**Option 2: Deploy to Web (Recommended for client demo)**
- Upload to GitHub Pages, Netlify, or Vercel
- Share the URL directly - works in Quest browser instantly

**Option 3: Use ngrok for quick sharing**
```bash
npx serve .
# In another terminal:
ngrok http 8000
```
Share the ngrok URL with anyone to test on their Quest.

---

## What This Prototype Demonstrates

### Current Features
- **Immersive Colorado plains environment** - Magic hour atmosphere
- **Rocky Mountain backdrop** - Stylized mountain range with snow caps
- **The Obsidian Rock** - Central interactive element that:
  - Rotates slowly with inner glow
  - Responds to gaze/hover
  - Cycles through 4 time periods on click:
    1. 1864 - The Homestead
    2. 1864 - Native American Settlement  
    3. 1975 - Eastern Plains (Louise finds the rock)
    4. 2025 - Concert Venue Premiere
- **Narrative text** - Story excerpts appear with each era
- **Particle effects** - Mystical energy around the obsidian
- **Dynamic lighting** - Changes color based on selected era

### VR Interactions
- **Gaze cursor** - Look at objects to highlight them
- **Fuse selection** - Stare at rock for 1.5s to activate (hands-free)
- **Click/Trigger** - Direct selection on Quest controllers

---

## Next Steps for Full Development

### Phase 1: Enhanced Prototype (1-2 weeks)
- [ ] Add spatial audio (wind, music cues from screenplay)
- [ ] Create 3D cabin interior for 1864 scene
- [ ] Add character silhouettes
- [ ] Implement scene transitions between eras
- [ ] Add hand tracking support

### Phase 2: Full Scene Development (Unity/Unreal)
For production quality, consider migrating to:

**Unity + XR Interaction Toolkit**
- Better performance on Quest
- Access to Quest features (hand tracking, passthrough)
- Asset store for environments
- C# scripting in VS Code

**Unreal Engine 5**
- Photorealistic environments
- Nanite/Lumen for cinematic quality
- Blueprint visual scripting + C++

### Phase 3: Full Experience
- Multiple complete environments (cabin, Native camp, modern arena)
- Full character models and animations
- Branching narrative choices
- Original soundtrack integration
- Multiplayer/shared viewing option

---

## Technical Notes

### Why WebXR/A-Frame for Prototype?
- **Zero friction** - Runs in browser, no app install
- **Cross-platform** - Works on Quest, desktop, even mobile
- **Fast iteration** - Edit HTML, refresh, see changes
- **Easy sharing** - Just send a URL
- **VS Code friendly** - It's just HTML/JS

### File Structure
```
obsidian-vr/
├── index.html      # Main VR experience
└── README.md       # This file
```

### Dependencies (loaded via CDN)
- A-Frame 1.4.2 - WebXR framework
- A-Frame Environment Component - Procedural environments
- A-Frame Particle System - Visual effects

---

## For the Client Presentation

**Talking Points:**
1. "This is a proof-of-concept to test the VR direction"
2. "The obsidian rock is the anchor - connecting all timelines"
3. "Users can experience key moments from each era"
4. "Full production would include the cabin scene, Native camp, and modern arena"
5. "The music from the screenplay would be spatialized around the viewer"

**Questions to Ask Client:**
- Passive cinematic experience vs. interactive exploration?
- Which scenes are highest priority?
- Solo experience or multiplayer viewing?
- Target release platform (Quest-exclusive or multi-platform)?
- Budget range for full production?

---

## Resources

- [A-Frame Documentation](https://aframe.io/docs/)
- [Meta Quest Developer Hub](https://developer.oculus.com/)
- [WebXR Device API](https://immersiveweb.dev/)
- [Unity XR Interaction Toolkit](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.0/manual/index.html)
