## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 25
- **Lines Added**: +482
- **Lines Removed**: -649
- **Total Commits**: 5
- **Source Commit**: [`bbd3de7`](https://github.com/CherryHQ/cherry-studio/commit/bbd3de7905f5d51790a9e3c833f21246a7def1e2)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`bbd3de7`](https://github.com/CherryHQ/cherry-studio/commit/bbd3de7905f5d51790a9e3c833f21246a7def1e2) fix: respect agent allowed_tools in MCP auto-approval check (#12965) - *Luca Moretti* (2026-03-04T11:39:37+02:00)
- [`1fb24f6`](https://github.com/CherryHQ/cherry-studio/commit/1fb24f6dc8f636cea6ecd2e7e92d3fc62625308f) fix: enable thinking for non-Anthropic models using Claude endpoints (#13138) - *SuYao* (2026-03-02T17:51:26+08:00)
- [`c7ac56a`](https://github.com/CherryHQ/cherry-studio/commit/c7ac56af97e7e3abba414683137e9351951675a2) fix(aiCore): extract provider/model from config and fix middleware ordering (#13109) - *SuYao* (2026-03-02T11:56:15+08:00)
- [`a965667`](https://github.com/CherryHQ/cherry-studio/commit/a9656674ffcb1889041fb503b2ccac3b148b5dbf) fix: upgrade ollama provider to 3.3.1 (#13085) - *Pleasure1234* (2026-02-27T14:52:46Z)
- [`842ccf0`](https://github.com/CherryHQ/cherry-studio/commit/842ccf02727ffd85f4e7221239cad164215ed959) refactor: migrate to aisdk v6 Phase 1 (#12078) - *SuYao* (2026-02-27T14:25:40+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/660c444dc2f7638f9274c62da0f5053eb3feae8e...bbd3de7905f5d51790a9e3c833f21246a7def1e2)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
