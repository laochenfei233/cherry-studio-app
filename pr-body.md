## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 18
- **Lines Added**: +1125
- **Lines Removed**: -205
- **Total Commits**: 13
- **Source Commit**: [`058a2c7`](https://github.com/CherryHQ/cherry-studio/commit/058a2c763b41ff08720e077d24089c6e97ef268a)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`058a2c7`](https://github.com/CherryHQ/cherry-studio/commit/058a2c763b41ff08720e077d24089c6e97ef268a) fix: restore API version control with trailing # delimiter (addresses #11750) (#11773) - *Phantom* (2025-12-10T13:42:15+08:00)
- [`0861902`](https://github.com/CherryHQ/cherry-studio/commit/086190228a14c96d42165e996f2481461120e8da) fix(aiCore): correct provider adaptation with model parameter (#11758) - *Phantom* (2025-12-09T10:42:18+08:00)
- [`73fc74d`](https://github.com/CherryHQ/cherry-studio/commit/73fc74d875d7652e25fcbf8275498c3b7e835c47) fix: add support for OpenRouter embeddings in listModels method (#11774) - *SuYao* (2025-12-09T10:29:35+08:00)
- [`9f7e473`](https://github.com/CherryHQ/cherry-studio/commit/9f7e47304d7d36684f37ee443ee4e3287d42bc94) refactor: improve temperature and top_p parameter handling (#11663) - *Phantom* (2025-12-08T11:26:44+08:00)
- [`3cedb95`](https://github.com/CherryHQ/cherry-studio/commit/3cedb95db33e570d0f09cbb6376e2ca83e3798ee) fix(stream-options): add user-configurable stream options for OpenAI API (#11693) - *Phantom* (2025-12-05T19:52:37+08:00)
- [`968210f`](https://github.com/CherryHQ/cherry-studio/commit/968210faa71555abcd9e4ca404dd8216e8166eee) fix: correct OVMS API URL path formation (#11701) - *Copilot* (2025-12-05T17:40:29+08:00)
- [`92bb059`](https://github.com/CherryHQ/cherry-studio/commit/92bb05950d1f65fea084acca644dd43724c395a2) fix: enhance provider handling and API key rotation logic in AiProvider (#11586) - *SuYao* (2025-12-05T13:25:54+08:00)
- [`a566cd6`](https://github.com/CherryHQ/cherry-studio/commit/a566cd65f4773825c8750f99bbc7ca983053deea) fix: normalize provider model data (#11580) - *Phantom* (2025-12-05T00:29:38+08:00)
- [`a2a6c62`](https://github.com/CherryHQ/cherry-studio/commit/a2a6c62f48585e459f0220e0131488fc0803c637) Fix custom parameters placement for Vercel AI Gateway (#11605) - *Copilot* (2025-12-04T21:19:30+08:00)
- [`981bb9f`](https://github.com/CherryHQ/cherry-studio/commit/981bb9f451e0ac54c8cba18d24e5149db0320b3f) fix: update deepseek logic to match deepseek v3.2 (#11648) - *SuYao* (2025-12-04T19:13:51+08:00)
- [`f571dd7`](https://github.com/CherryHQ/cherry-studio/commit/f571dd7af0f98a7616dfd29af52c26695e65703c) fix: ollama url (#11611) - *槑囿脑袋* (2025-12-03T21:03:07+08:00)
- [`6696bca`](https://github.com/CherryHQ/cherry-studio/commit/6696bcacb8bf9df724d8f4394332f89892287c2f) fix(settings): fix wrong type caused by as assertion in OpenAI settings (#11631) - *Phantom* (2025-12-03T18:20:55+08:00)
- [`a1e95b5`](https://github.com/CherryHQ/cherry-studio/commit/a1e95b55f8d67d86e2a575b35aae6a9386053ded) fix: remove stale anthropic-beta header for oauth (#11600) - *Phantom* (2025-12-03T17:20:12+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/3aedf6f1386f89d1640fa06bec40b1a4578b0919...058a2c763b41ff08720e077d24089c6e97ef268a)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
