## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 12
- **Lines Added**: +325
- **Lines Removed**: -57
- **Total Commits**: 9
- **Source Commit**: [`c1bf6cf`](https://github.com/CherryHQ/cherry-studio/commit/c1bf6cfbb712eeeba81d6ca2876d593c56871bec)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`c1bf6cf`](https://github.com/CherryHQ/cherry-studio/commit/c1bf6cfbb712eeeba81d6ca2876d593c56871bec) fix: add gpustack provider for qwen3 enable think (#11843) - *SuYao* (2025-12-11T18:16:47+08:00)
- [`5f3af64`](https://github.com/CherryHQ/cherry-studio/commit/5f3af646f4307f01b083c9ae78c422eca16a5c53) fix: update CherryIN API URL and add thinking budget parameter - *kangfenmao* (2025-12-11T15:43:28+08:00)
- [`76524d6`](https://github.com/CherryHQ/cherry-studio/commit/76524d68c6ba2e79a1e92f2bb23a60c24bd38702) feat: add CherryIN API host selection settings (#11797) - *亢奋猫* (2025-12-11T11:19:28+08:00)
- [`058a2c7`](https://github.com/CherryHQ/cherry-studio/commit/058a2c763b41ff08720e077d24089c6e97ef268a) fix: restore API version control with trailing # delimiter (addresses #11750) (#11773) - *Phantom* (2025-12-10T13:42:15+08:00)
- [`0861902`](https://github.com/CherryHQ/cherry-studio/commit/086190228a14c96d42165e996f2481461120e8da) fix(aiCore): correct provider adaptation with model parameter (#11758) - *Phantom* (2025-12-09T10:42:18+08:00)
- [`73fc74d`](https://github.com/CherryHQ/cherry-studio/commit/73fc74d875d7652e25fcbf8275498c3b7e835c47) fix: add support for OpenRouter embeddings in listModels method (#11774) - *SuYao* (2025-12-09T10:29:35+08:00)
- [`9f7e473`](https://github.com/CherryHQ/cherry-studio/commit/9f7e47304d7d36684f37ee443ee4e3287d42bc94) refactor: improve temperature and top_p parameter handling (#11663) - *Phantom* (2025-12-08T11:26:44+08:00)
- [`3cedb95`](https://github.com/CherryHQ/cherry-studio/commit/3cedb95db33e570d0f09cbb6376e2ca83e3798ee) fix(stream-options): add user-configurable stream options for OpenAI API (#11693) - *Phantom* (2025-12-05T19:52:37+08:00)
- [`968210f`](https://github.com/CherryHQ/cherry-studio/commit/968210faa71555abcd9e4ca404dd8216e8166eee) fix: correct OVMS API URL path formation (#11701) - *Copilot* (2025-12-05T17:40:29+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/92bb05950d1f65fea084acca644dd43724c395a2...c1bf6cfbb712eeeba81d6ca2876d593c56871bec)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
