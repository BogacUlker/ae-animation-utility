# AE Animation Utility Extension

After Effects extension for streamlining common animation workflows with keyframe management and easing presets.

## 🎯 Project Goal

Create a minimal prototype extension with 1-2 core features to validate the development workflow, then expand based on testing and feedback.

## 🚀 Phase 1: Minimal Prototype

### Target Features
1. **Easing Preset Applier** - Quick apply common easing curves to selected keyframes
   - Ease In (75% influence)
   - Ease Out (33% influence)
   - Easy Ease (balanced)
   - Linear (remove easing)

2. **Keyframe Offset Tool** - Stagger selected layer animations by time offset
   - Input: offset amount (frames or seconds)
   - Apply to selected layers in sequence

## 📁 Project Structure

```
ae-animation-utility/
├── CSXS/
│   └── manifest.xml          # Extension metadata, AE version compatibility
├── client/
│   ├── index.html           # Panel UI
│   ├── styles/
│   │   └── main.css         # UI styling
│   └── js/
│       ├── main.js          # UI logic & event handlers
│       └── CSInterface.js   # Adobe CEP library (bridge)
└── host/
    └── index.jsx            # ExtendScript - AE API operations
```

## 🔧 Technical Stack

- **CEP Version**: 11+ (After Effects 2021+)
- **UI Layer**: HTML5, CSS3, Vanilla JavaScript
- **Logic Layer**: ExtendScript (Adobe's JavaScript variant)
- **API**: After Effects ExtendScript API

## 📋 Development Roadmap

### Phase 1: Foundation ✅ (Current)
- [x] Project structure setup
- [ ] manifest.xml configuration
- [ ] Basic HTML panel with test button
- [ ] CEP-ExtendScript bridge verification
- [ ] "Hello World" test (create comp from button click)

### Phase 2: Core Features
- [ ] Easing preset buttons (4 types)
- [ ] Keyframe offset tool UI
- [ ] Selected property detection
- [ ] Batch keyframe operations
- [ ] Error handling & user feedback

### Phase 3: Testing & Iteration
- [ ] Install in AE extensions folder
- [ ] Test on various layer types
- [ ] Test on multiple properties simultaneously
- [ ] Edge case handling (no selection, locked layers, etc.)
- [ ] Performance testing with many keyframes

### Phase 4: Polish
- [ ] UI improvements (icons, layout)
- [ ] Keyboard shortcuts
- [ ] Undo support validation
- [ ] Settings persistence
- [ ] User documentation

## 🎨 UI Mockup Concept

```
┌─────────────────────────────┐
│  Animation Utility          │
├─────────────────────────────┤
│  Easing Presets:            │
│  [Ease In] [Ease Out]       │
│  [Easy Ease] [Linear]       │
│                             │
│  Keyframe Tools:            │
│  Offset: [___] frames       │
│  [Apply Stagger]            │
│                             │
│  Status: Ready              │
└─────────────────────────────┘
```

## 🔄 Development Workflow

1. **Development**: Code feature implementation
2. **Installation**: Copy to AE extensions folder
   - **Windows**: `C:\Program Files\Common Files\Adobe\CEP\extensions\`
   - **Mac**: `/Library/Application Support/Adobe/CEP/extensions/`
3. **Testing**: Load in AE via Window → Extensions → Animation Utility
4. **Feedback**: Report bugs, unexpected behavior, feature requests
5. **Iteration**: Fix issues and enhance based on real-world usage

## 📦 Installation Instructions

### For Development
1. Clone this repository
2. Copy entire folder to Adobe CEP extensions directory
3. Enable debugging (if needed):
   - Create `.debug` file in extension folder
   - Or use `PlayerDebugMode` registry key (Windows) / plist (Mac)
4. Restart After Effects
5. Access via Window → Extensions → Animation Utility

### Debug Mode Setup
```xml
<!-- .debug file -->
<?xml version="1.0" encoding="UTF-8"?>
<ExtensionList>
    <Extension Id="com.example.ae-animation-utility">
        <HostList>
            <Host Name="AEFT" Port="8088"/>
        </HostList>
    </Extension>
</ExtensionList>
```

## 🧪 Testing Checklist

### Functional Tests
- [ ] Panel opens without errors
- [ ] Buttons respond to clicks
- [ ] Easing applied correctly to keyframes
- [ ] Offset calculation accurate
- [ ] Works with position/scale/rotation/opacity
- [ ] Multiple layer selection support
- [ ] Undo/redo integration

### Edge Cases
- [ ] No layers selected
- [ ] No keyframes on selected properties
- [ ] Locked layers
- [ ] 3D vs 2D layers
- [ ] Expression-driven properties
- [ ] Very large keyframe counts (100+)

### Error Handling
- [ ] Graceful failure messages
- [ ] No AE crashes
- [ ] Status updates in UI
- [ ] Console error logging

## 🐛 Known Issues

*Will be populated during testing phase*

## 🎯 Future Feature Ideas

### Medium Priority
- Custom easing curve editor
- Animation template save/load
- Batch property operations (animate multiple properties at once)
- Keyframe distribution (evenly space)
- Animation reverser

### Low Priority
- Expression snippet manager
- Motion path utilities
- Advanced expression builder
- Procedural animation generators

## 🤝 Contributing

This is a learning project. Feedback and suggestions welcome!

## 📄 License

MIT License - Free to use, modify, and distribute

## 📚 Resources

- [Adobe CEP Documentation](https://github.com/Adobe-CEP/CEP-Resources)
- [After Effects Scripting Guide](https://ae-scripting.docsforadobe.dev/)
- [ExtendScript Toolkit](https://extendscript.docsforadobe.dev/)

---

**Status**: 🔨 In Development - Phase 1
**Last Updated**: 2025-10-01
