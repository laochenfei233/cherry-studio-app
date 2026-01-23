## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 6
- **Lines Added**: +231
- **Lines Removed**: -108
- **Total Commits**: 6
- **Source Commit**: [`56bfa95`](https://github.com/CherryHQ/cherry-studio/commit/56bfa95d08b2d7be144c809c1e426b98ffd293fa)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`56bfa95`](https://github.com/CherryHQ/cherry-studio/commit/56bfa95d08b2d7be144c809c1e426b98ffd293fa) fix(header): resolve User-Agent forbidden header in renderer process (#12549) - *SuYao* (2026-01-23T14:18:28+08:00)
- [`ac23c7f`](https://github.com/CherryHQ/cherry-studio/commit/ac23c7f30bee65449dc2df66d6ba64d1f093faec) fix(aiCore): preserve conversation history for image enhancement models (#12239) - *SuYao* (2026-01-14T14:23:19+08:00)
- [`9414f13`](https://github.com/CherryHQ/cherry-studio/commit/9414f13f6da5240c56e9e78e2ecaf599383cf88d) fix: 修改请求体字段名 (#12430) - *SuYao* (2026-01-12T16:38:55+08:00)
- [`cbeda03`](https://github.com/CherryHQ/cherry-studio/commit/cbeda03acbe780f72f8bf1aa2dbda6f525e1cdf4) use cumsum in anthropic cache (#12419) - *flt6* (2026-01-12T15:49:33+08:00)
- [`c7c380d`](https://github.com/CherryHQ/cherry-studio/commit/c7c380d706667f2f252438c971adade603f894e3) fix: disable strict JSON schema for OpenRouter to support MCP tools (#12415) - *SuYao* (2026-01-10T21:55:09+08:00)
- [`29d8c4a`](https://github.com/CherryHQ/cherry-studio/commit/29d8c4a7ede6d1521b074482a9689addab31d169) fix(aiCore): only apply sendReasoning for openai-compatible SDK providers (#12387) - *SuYao* (2026-01-09T15:00:31+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/0cb3bd831122034d359ae97fca83fb7f5bd87432...56bfa95d08b2d7be144c809c1e426b98ffd293fa)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
