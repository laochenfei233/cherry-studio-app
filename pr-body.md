## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 10
- **Lines Added**: +187
- **Lines Removed**: -94
- **Total Commits**: 7
- **Source Commit**: [`1c6ec3e`](https://github.com/CherryHQ/cherry-studio/commit/1c6ec3eadaecbe2f8a8834ab721adfc84186698c)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`1c6ec3e`](https://github.com/CherryHQ/cherry-studio/commit/1c6ec3eadaecbe2f8a8834ab721adfc84186698c) fix: improve Qwen 3.5 reasoning model detection and thinking param handling (#13235) - *Phantom* (2026-03-05T18:36:15+08:00)
- [`dcf844e`](https://github.com/CherryHQ/cherry-studio/commit/dcf844e05f4168306e37aaa8848eb05c50e86a16) fix: use camelCase reasoningEffort for Gemini 3 models in openai-compatible provider (#13228) - *SuYao* (2026-03-05T13:39:24+08:00)
- [`1392baa`](https://github.com/CherryHQ/cherry-studio/commit/1392baa90ebd55ce29c4f85bb2cf9167ed3c2252) fix: prompt caching crash for OpenRouter and non-Anthropic providers (#13227) - *SuYao* (2026-03-05T13:30:53+08:00)
- [`d71157b`](https://github.com/CherryHQ/cherry-studio/commit/d71157bf025b12ca37bdb0fe0ef4563e588fe6da) fix: duplicate error blocks in aborting (#13224) - *Konv Suu* (2026-03-05T11:58:02+08:00)
- [`bbd3de7`](https://github.com/CherryHQ/cherry-studio/commit/bbd3de7905f5d51790a9e3c833f21246a7def1e2) fix: respect agent allowed_tools in MCP auto-approval check (#12965) - *Luca Moretti* (2026-03-04T11:39:37+02:00)
- [`1fb24f6`](https://github.com/CherryHQ/cherry-studio/commit/1fb24f6dc8f636cea6ecd2e7e92d3fc62625308f) fix: enable thinking for non-Anthropic models using Claude endpoints (#13138) - *SuYao* (2026-03-02T17:51:26+08:00)
- [`c7ac56a`](https://github.com/CherryHQ/cherry-studio/commit/c7ac56af97e7e3abba414683137e9351951675a2) fix(aiCore): extract provider/model from config and fix middleware ordering (#13109) - *SuYao* (2026-03-02T11:56:15+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/712cf1d644ec736d0494ff2cc4f9c0a1cd0c6c84...1c6ec3eadaecbe2f8a8834ab721adfc84186698c)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
