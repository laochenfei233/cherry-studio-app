## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 17
- **Lines Added**: +635
- **Lines Removed**: -104
- **Total Commits**: 6
- **Source Commit**: [`134280a`](https://github.com/CherryHQ/cherry-studio/commit/134280a8627931beffb2c37e1c5e58159392cef5)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`134280a`](https://github.com/CherryHQ/cherry-studio/commit/134280a8627931beffb2c37e1c5e58159392cef5) fix: use i18nKey for error display and add timeout enforcement (#12164) - *Phantom* (2026-03-13T10:06:14+08:00)
- [`5f5ddb2`](https://github.com/CherryHQ/cherry-studio/commit/5f5ddb2b36d2418e2da21f4df6812c1e7a3bc06e) fix: correct Gemini reasoning params for none effort and Gemini 3 thinkingLevel (#13388) - *Phantom* (2026-03-12T15:03:24+08:00)
- [`2bbf09b`](https://github.com/CherryHQ/cherry-studio/commit/2bbf09b546262e4f7489e4a7a5815d5d0e8c0bd4) fix: upgrade xAI web search from deprecated Live Search to Responses API (#12812) - *PhoenixCPH* (2026-03-12T14:07:35+08:00)
- [`bec5ea4`](https://github.com/CherryHQ/cherry-studio/commit/bec5ea4f46cf394ead2c64d5c6a8e73c140521b5) fix: auto-convert reasoning_effort to reasoningEffort for openai-compatible providers (#12831) - *SuYao* (2026-03-11T11:05:30+08:00)
- [`5a2a609`](https://github.com/CherryHQ/cherry-studio/commit/5a2a6092642c9faaf3369d778df8cc76d25993d4) fix: check underlying tool permissions for hub invoke/exec (#13282) - *SuYao* (2026-03-09T20:14:35+08:00)
- [`27ef9b8`](https://github.com/CherryHQ/cherry-studio/commit/27ef9b8123d655c391668a0b232e6082269a0829) fix: remove approval countdown timers and add system notifications (#13281) - *SuYao* (2026-03-09T20:14:22+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/f45874dec15d9a5853617ca698360bb66de9ccae...134280a8627931beffb2c37e1c5e58159392cef5)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
