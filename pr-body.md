## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 7
- **Lines Added**: +48
- **Lines Removed**: -18
- **Total Commits**: 7
- **Source Commit**: [`b4aeced`](https://github.com/CherryHQ/cherry-studio/commit/b4aeced1f984c7bf6936361762728e3cd6a9fae5)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`b4aeced`](https://github.com/CherryHQ/cherry-studio/commit/b4aeced1f984c7bf6936361762728e3cd6a9fae5) fix: thinking time on stop (#11900) - *Calvin Wade* (2026-01-04T19:43:44+08:00)
- [`efbe64e`](https://github.com/CherryHQ/cherry-studio/commit/efbe64e5dab7da2c91305f8ef83232cd4f2d6e54) feat(tokenflux): add Anthropic host support using OpenRouter package (#12188) - *LiuVaayne* (2025-12-29T18:24:57+08:00)
- [`cccf9bb`](https://github.com/CherryHQ/cherry-studio/commit/cccf9bb7be98469052e076ea00a6a1f596adb059) feat: add latest zhipu models (#12169) - *tylinux* (2025-12-28T19:11:08+08:00)
- [`5ff173f`](https://github.com/CherryHQ/cherry-studio/commit/5ff173fcc7ffa39f0c45b84fbdacefe55432320b) fix(ollama): improve reasoningEffort handling in providerOptions (#12089) - *SuYao* (2025-12-28T17:04:45+08:00)
- [`99b431e`](https://github.com/CherryHQ/cherry-studio/commit/99b431ec9299add599e6f74067f058a954f83d02) fix: remove trailing api version in ANTHROPIC_BASE_URL (#12145) - *defi-failure* (2025-12-26T17:37:58+08:00)
- [`d9171e0`](https://github.com/CherryHQ/cherry-studio/commit/d9171e0596aa6956f9cae77b99ff1a4402bac7b1) fix(openrouter): support GPT-5.1/5.2 reasoning effort 'none' for OpenRouter and improve error handling (#12088) - *Phantom* (2025-12-24T14:18:41+08:00)
- [`09e58d3`](https://github.com/CherryHQ/cherry-studio/commit/09e58d37560a6ffd61c819dacd6ae7ac2429a00f) fix: interleaved thinking support (#12084) - *SuYao* (2025-12-23T20:08:53+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/5f0006dcede235cf06bd630864f3afb13ef552bb...b4aeced1f984c7bf6936361762728e3cd6a9fae5)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
