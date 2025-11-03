## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 69
- **Lines Added**: +509
- **Lines Removed**: -401
- **Total Commits**: 6
- **Source Commit**: [`abd5d3b`](https://github.com/CherryHQ/cherry-studio/commit/abd5d3b96ff549aa571938f1b5187a48cb6747ed)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`abd5d3b`](https://github.com/CherryHQ/cherry-studio/commit/abd5d3b96ff549aa571938f1b5187a48cb6747ed) feat: amazon bedrock request use bedrock api key (#10727) - *Zephyr* (2025-11-03T21:05:10+08:00)
- [`4186e9c`](https://github.com/CherryHQ/cherry-studio/commit/4186e9c990824d6d0c1f7fbb87df92479e3d0459) feat: add support for TopP in model capabilities and update parameter builder to utilize it - *kangfenmao* (2025-11-03T16:37:12+08:00)
- [`bd94d23`](https://github.com/CherryHQ/cherry-studio/commit/bd94d2334316a66f50ad9e899e822b9f2f6a3374) refactor:Unify the naming of configuration fields in thinking, change to using underscore style. (#11106) - *SuYao* (2025-11-02T19:24:23+08:00)
- [`5f1c14e`](https://github.com/CherryHQ/cherry-studio/commit/5f1c14e2c03af79c1301ac43ade9e220848a959b) fix(aihubmix): fix default rules missing app code (#11100) - *chenxue* (2025-11-02T17:03:05+08:00)
- [`dc06c10`](https://github.com/CherryHQ/cherry-studio/commit/dc06c103e0e1ea93c66fec586df665a6c4a42194) chore[lint]: add import type lint (#11091) - *fullex* (2025-11-01T10:40:02+08:00)
- [`e0a2ed0`](https://github.com/CherryHQ/cherry-studio/commit/e0a2ed04810f424b2606cf3ec32a0abfdcdcac48) Provider Config & anthropic-web-fetch (#10808) - *SuYao* (2025-10-29T14:47:21+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/5986800c9d820cad76eb57c62e7f3a1e06c34704...abd5d3b96ff549aa571938f1b5187a48cb6747ed)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
