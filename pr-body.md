## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 9
- **Lines Added**: +204
- **Lines Removed**: -36
- **Total Commits**: 8
- **Source Commit**: [`29d8c4a`](https://github.com/CherryHQ/cherry-studio/commit/29d8c4a7ede6d1521b074482a9689addab31d169)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`29d8c4a`](https://github.com/CherryHQ/cherry-studio/commit/29d8c4a7ede6d1521b074482a9689addab31d169) fix(aiCore): only apply sendReasoning for openai-compatible SDK providers (#12387) - *SuYao* (2026-01-09T15:00:31+08:00)
- [`81ea847`](https://github.com/CherryHQ/cherry-studio/commit/81ea8479890671d0b69807b6ccd8f6a112cc0942) Add Anthropic Cache (#12333) - *花月喵梦* (2026-01-07T23:05:30+08:00)
- [`040f4da`](https://github.com/CherryHQ/cherry-studio/commit/040f4daa98b1577312e84cc27b484621b91690af) fix: enable reasoning cot bug (#12342) - *SuYao* (2026-01-07T17:11:41+08:00)
- [`6d15b0d`](https://github.com/CherryHQ/cherry-studio/commit/6d15b0dfd1a6b4346175dd4cf88a210f81777e45)  feat(mcp): add MCP Hub server for multi-server tool orchestration (#12192) - *LiuVaayne* (2026-01-07T16:35:51+08:00)
- [`6b0bb64`](https://github.com/CherryHQ/cherry-studio/commit/6b0bb64795beb99b5e7a63261132695462d69da4) fix: convert 'developer' role to 'system' for unsupported providers (#12325) - *SuYao* (2026-01-07T01:03:37+08:00)
- [`a5038ac`](https://github.com/CherryHQ/cherry-studio/commit/a5038ac84488ba023957eea1e7289ce498ab14e8) fix: Add reasoning control for Deepseek hybrid inference models when reasoning effort is 'none' (#12314) - *Phantom* (2026-01-06T17:28:34+08:00)
- [`76ee67d`](https://github.com/CherryHQ/cherry-studio/commit/76ee67d4d7c6c8de1efb2ead772028f29991033a) fix: prevent OOM when handling large base64 image data (#12244) - *SuYao* (2026-01-06T00:34:14+08:00)
- [`b4aeced`](https://github.com/CherryHQ/cherry-studio/commit/b4aeced1f984c7bf6936361762728e3cd6a9fae5) fix: thinking time on stop (#11900) - *Calvin Wade* (2026-01-04T19:43:44+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/2012378341cb5960a12a8cd74893fe827482ba82...29d8c4a7ede6d1521b074482a9689addab31d169)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
