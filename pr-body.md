## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 23
- **Lines Added**: +419
- **Lines Removed**: -605
- **Total Commits**: 3
- **Source Commit**: [`842ccf0`](https://github.com/CherryHQ/cherry-studio/commit/842ccf02727ffd85f4e7221239cad164215ed959)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`842ccf0`](https://github.com/CherryHQ/cherry-studio/commit/842ccf02727ffd85f4e7221239cad164215ed959) refactor: migrate to aisdk v6 Phase 1 (#12078) - *SuYao* (2026-02-27T14:25:40+08:00)
- [`7cca235`](https://github.com/CherryHQ/cherry-studio/commit/7cca23571a7be73e8499d8d6aa138ce9e6b231d2) feat: Add Claude Sonnet 4.6 model support to Anthropic provider (#13016) - *Phantom* (2026-02-24T20:03:10+08:00)
- [`a6cfe6b`](https://github.com/CherryHQ/cherry-studio/commit/a6cfe6ba0f2999c3afcd50b5c7913a911d24bb6d) feat(zhipu): add GLM-5 model support (#12942) - *Wike* (2026-02-17T12:05:53+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/fc7e3742e03836626da6cb038f94547aca51878b...842ccf02727ffd85f4e7221239cad164215ed959)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
