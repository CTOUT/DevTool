# DevTool - Ascension WotLK 3.3.5 Compatibility Fork

## [1.0.11-ascension.1] (2025-11-13)

### WotLK 3.3.5 / Project Ascension Compatibility Changes

This fork adds full compatibility for WotLK 3.3.5 (Project Ascension) while maintaining backward compatibility.

#### Core API Compatibility Fixes

**Color API Shims** - Added missing WoW 8.0+ color functions for WotLK:
- CreateColorFromHexString() shim
- CreateColor() shim  
- ColorMixin with GetRGBA(), GetRGB(), SetRGBA(), WrapTextInColorCode()
- Wraps Ascension's partial implementations to add missing methods

**Frame Resizing** - Fixed window resize corner:
- GetResizeBounds() compatibility (WoW 10.0+)
- Falls back to GetMaxResize()/GetMinResize() for WotLK

**HybridScrollFrame** - Fixed scrolling crashes:
- Set buttonHeight before HybridScrollFrame_CreateButtons
- Wrap OnValueChanged callback to prevent context errors

**Ascension EventTrace** - Fixed /etrace button:
- Loads Ascension_UIDevelopmentTools instead of Blizzard_EventTrace
- Toggles AscensionEventTrace frame properly
- Falls back to Blizzard version for compatibility

#### Testing Status
- ✅ All buttons functional
- ✅ Window resizing works
- ✅ Scrolling works  
- ✅ Color formatting works
- ✅ No Lua errors

#### Copyright Attribution
This fork preserves the original copyright notices "as of fork date" to maintain accurate historical attribution. For current upstream copyright information, please refer to the original repository.

**Upstream:** https://github.com/brittyazel/DevTool  
**This Fork:** https://github.com/CTOUT/DevTool
