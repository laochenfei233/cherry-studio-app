## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 10
- **Lines Added**: +455
- **Lines Removed**: -248
- **Total Commits**: 11
- **Source Commit**: [`888c6d7`](https://github.com/CherryHQ/cherry-studio/commit/888c6d7123af60654436c0fe52518b326481c97f)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`888c6d7`](https://github.com/CherryHQ/cherry-studio/commit/888c6d7123af60654436c0fe52518b326481c97f) fix: align hub MCP tools with mcphub (remove search) (#12571) - *LiuVaayne* (2026-02-04T21:30:32+08:00)
- [`2167d96`](https://github.com/CherryHQ/cherry-studio/commit/2167d96e903369e4b5a145cf8747cb8dad41a8dd) fix(bedrock): reorder content blocks for Claude extended thinking (#12713) - *SuYao* (2026-02-04T15:32:20+08:00)
- [`ca46f6b`](https://github.com/CherryHQ/cherry-studio/commit/ca46f6b206cc7783f03aa0e0a8d222cb3274a283) fix: add placeholder text for image-only assistant messages (#12712) - *SuYao* (2026-02-04T14:04:56+08:00)
- [`4fb58f1`](https://github.com/CherryHQ/cherry-studio/commit/4fb58f1c38e523b1426929b52dc91a312b260d4f) fix: handle developer-to-system role conversion for Chat Completions API (#12709) - *SuYao* (2026-02-04T13:35:31+08:00)
- [`c217a88`](https://github.com/CherryHQ/cherry-studio/commit/c217a883ebaca6ed16300c68637d8a3a0c92ba19) feat: add free Qwen3-Next-80B model support - *kangfenmao* (2026-01-29T15:40:03+08:00)
- [`742fbc5`](https://github.com/CherryHQ/cherry-studio/commit/742fbc555ee4222745d329d7a19c6ee1bd4fd611) feat: add Kimi K2.5 model support (#12620) - *Phantom* (2026-01-28T02:30:55+08:00)
- [`0d12da6`](https://github.com/CherryHQ/cherry-studio/commit/0d12da64689df3fdb9a812f4ced95aec175ecf34) fix: Correct reasoning parameters for Aliyun Bailian GLM models and support qwen3-max snapshots (#12614) - *Phantom* (2026-01-27T22:57:34+08:00)
- [`2a3e157`](https://github.com/CherryHQ/cherry-studio/commit/2a3e157ee7fd6121787ab4361b35907e359ca990) refactor(agent): improve tool call render ui/ux (#12540) - *SuYao* (2026-01-27T10:26:02+08:00)
- [`0255cb8`](https://github.com/CherryHQ/cherry-studio/commit/0255cb84435c817d0bc795276ed285abe5bb5079) fix: Improve provider config type safety and ensure required fields (#12589) - *Phantom* (2026-01-26T14:35:46+08:00)
- [`3737c16`](https://github.com/CherryHQ/cherry-studio/commit/3737c1680b6e5bbe0e50e7606345133642b9a035) Revert "fix(header): resolve User-Agent forbidden header in renderer process (#12549)" - *kangfenmao* (2026-01-25T21:17:54+08:00)
- [`56bfa95`](https://github.com/CherryHQ/cherry-studio/commit/56bfa95d08b2d7be144c809c1e426b98ffd293fa) fix(header): resolve User-Agent forbidden header in renderer process (#12549) - *SuYao* (2026-01-23T14:18:28+08:00)

### 🔧 What Was Done

1. ✅ Generated patch from upstream changes
2. ✅ Transformed paths for mobile structure (`src/renderer/src/aiCore` → `src/aiCore`)
3. ✅ Attempted automatic patch application
4. ❌ Automatic application failed

### 📦 Manual Application Required

The patch is available at `.github/port-patches/aicore-changes.patch`

To apply manually:
```bash
git apply .github/port-patches/aicore-changes.patch
# Or with 3-way merge:
git apply --3way .github/port-patches/aicore-changes.patch
```

### ✅ Manual Porting Checklist

- [ ] Review all code changes for mobile compatibility
- [ ] Check for Node.js/Electron-specific APIs (fs, path, etc.)
- [ ] Verify imports work in React Native context
- [ ] Replace desktop APIs with Expo equivalents if needed
- [ ] Test provider functionality on iOS
- [ ] Test provider functionality on Android
- [ ] Verify streaming and SSE handling works on mobile
- [ ] Check error handling in mobile environment
- [ ] Run linting: `yarn lint`
- [ ] Run type checking: `yarn typecheck`
- [ ] Run tests: `yarn test`
- [ ] Test on physical devices (not just emulators)

### ⚠️ Key Differences to Watch

| Desktop (Electron) | Mobile (React Native/Expo) |
|-------------------|---------------------------|
| `fs`, `path` modules | `expo-file-system` |
| Electron IPC | React Native Bridge |
| Synchronous file ops | Async-first with promises |
| Full file system access | Sandboxed directories |
| Node.js crypto | `expo-crypto` or `react-native-crypto` |

### 🔗 Related Links

- [Source Repository](https://github.com/CherryHQ/cherry-studio)
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/ed54bf8810ceef354dd435605ac3359d3b554abb...888c6d7123af60654436c0fe52518b326481c97f)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
