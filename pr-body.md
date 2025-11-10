## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 9
- **Lines Added**: +338
- **Lines Removed**: -38
- **Total Commits**: 7
- **Source Commit**: [`e2c8eda`](https://github.com/CherryHQ/cherry-studio/commit/e2c8edab61239365530d6d415e517f2ed0831c9f)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`e2c8eda`](https://github.com/CherryHQ/cherry-studio/commit/e2c8edab61239365530d6d415e517f2ed0831c9f) fix: incorrect spelling caused Gemini endpoint’s thinking budget to fail (#11217) - *Konjac-XZ* (2025-11-10T16:42:34+08:00)
- [`83e4d43`](https://github.com/CherryHQ/cherry-studio/commit/83e4d4363fc069e7477ee06feafa0099dfa87630) fix: add Perplexity provider support and update API host formatting (#11162) - *beyondkmp* (2025-11-06T10:43:33+08:00)
- [`346af4d`](https://github.com/CherryHQ/cherry-studio/commit/346af4d338fbd3719a3d0af9f2c3380273fb3e47) fix: add CherryAI provider support and update API host formatting (#11135) - *beyondkmp* (2025-11-04T12:59:14+08:00)
- [`abd5d3b`](https://github.com/CherryHQ/cherry-studio/commit/abd5d3b96ff549aa571938f1b5187a48cb6747ed) feat: amazon bedrock request use bedrock api key (#10727) - *Zephyr* (2025-11-03T21:05:10+08:00)
- [`4186e9c`](https://github.com/CherryHQ/cherry-studio/commit/4186e9c990824d6d0c1f7fbb87df92479e3d0459) feat: add support for TopP in model capabilities and update parameter builder to utilize it - *kangfenmao* (2025-11-03T16:37:12+08:00)
- [`bd94d23`](https://github.com/CherryHQ/cherry-studio/commit/bd94d2334316a66f50ad9e899e822b9f2f6a3374) refactor:Unify the naming of configuration fields in thinking, change to using underscore style. (#11106) - *SuYao* (2025-11-02T19:24:23+08:00)
- [`5f1c14e`](https://github.com/CherryHQ/cherry-studio/commit/5f1c14e2c03af79c1301ac43ade9e220848a959b) fix(aihubmix): fix default rules missing app code (#11100) - *chenxue* (2025-11-02T17:03:05+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/28bc89ac7ccd9acf502f9e564848ed1530a7b373...e2c8edab61239365530d6d415e517f2ed0831c9f)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
