# [Processing 4.3](https://github.com/benfry/processing4/releases/tag/processing-1293-4.3)

_Revision 1293 – 26 July 2023_

This release incorporates several contributed fixes (see below) and a few additional bug fixes and changes. The icons have been updated a bit so that Processing is less likely to be confused with Visual Studio Code when seen in the dock or taskbar, and the splash screen colors and layout have design tweaks as well.

- Update documentation and process for updating language files for localization [722](https://github.com/processing/processing4/issues/722)
- Inherit dark mode from system settings on macOS [699](https://github.com/processing/processing4/issues/699)
- Use calculated text height instead of OS ascent for better vertical centering. _Note: this may cause some sketches to look slightly different if textAlign(..., CENTER) is being used._ [739](https://github.com/processing/processing4/issues/739)
- Bumped Java to 17.0.8+7.
- Fix `NullPointerException` when `background()` exceeds color range when writing PDF [740](https://github.com/processing/processing4/issues/740)

### Contributions

- Updated icons and splash screen colors from [@fathompaul](https://github.com/fathompaul).
- Register pde:// browser protocol for .pdez and .pdex files on Linux from @lala-lala-lori [674](https://github.com/processing/processing4/issues/674), [696](https://github.com/processing/processing4/pull/696)
- Syntax error highlighting placement / width incorrect from [@sampottinger](https://github.com/sampottinger) [714](https://github.com/processing/processing4/issues/714), [715](https://github.com/processing/processing4/pull/715)
- Better comment/uncomment key shortcut for French systems from @ThinkDumbIndustries [625](https://github.com/processing/processing4/issues/625), [660](https://github.com/processing/processing4/pull/660)
- Fix tweak mode issue with hex codes including transparency from [@sampottinger](https://github.com/sampottinger) [720](https://github.com/processing/processing4/issues/720), [721](https://github.com/processing/processing4/pull/721)
- LSP feature/declaration support from [@Efratror](https://github.com/Efratror) [676](https://github.com/processing/processing4/issues/676), [678](https://github.com/processing/processing4/pull/678)
- Also reference support for Language Server Protocol from [@Efratror](https://github.com/Efratror) [684](https://github.com/processing/processing4/issues/684), [690](https://github.com/processing/processing4/pull/690)
- Updates to the Spanish and Catalan translations from [@trikaphundo](https://github.com/trikaphundo) [744](https://github.com/processing/processing4/issues/744), [746](https://github.com/processing/processing4/pull/746), [743](https://github.com/processing/processing4/issues/743), [745](https://github.com/processing/processing4/pull/745)
- Debugger was listing immediate array dimension last, fix from [@WillRabalais04](https://github.com/WillRabalais04) [606](https://github.com/processing/processing4/issues/606), [729](https://github.com/processing/processing4/pull/729)
- Second `beginDraw()` / `endDraw()` call clears `PGraphics` object when created w/ `P2D` [641](https://github.com/processing/processing4/issues/641), [728](https://github.com/processing/processing4/pull/728)
