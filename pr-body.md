## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 21
- **Lines Added**: +584
- **Lines Removed**: -48
- **Total Commits**: 11
- **Source Commit**: [`d081b05`](https://github.com/CherryHQ/cherry-studio/commit/d081b05c8724294944aaebdb5e7b156ee43997f7)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`d081b05`](https://github.com/CherryHQ/cherry-studio/commit/d081b05c8724294944aaebdb5e7b156ee43997f7) fix: Format provider API hosts in API server & refactor shared utilities (#13198) - *Phantom* (2026-03-19T00:41:20+08:00)
- [`a4cc48a`](https://github.com/CherryHQ/cherry-studio/commit/a4cc48a84621f3217fdb2910497ad9e4d5e4deac) refactor: consolidate qwen model definitions and update related references - *kangfenmao* (2026-03-18T19:09:48+08:00)
- [`21a8c62`](https://github.com/CherryHQ/cherry-studio/commit/21a8c625cb16f9f0d7b9caa293d6350e52a376e7) fix: add budgetTokens fallback for Agent thinking compatibility (#13575) - *Phantom* (2026-03-18T12:21:09+08:00)
- [`3f9cb07`](https://github.com/CherryHQ/cherry-studio/commit/3f9cb07cbef0ab20edf72f1236556de4d14f1099) fix: propagate actual stream errors instead of generic NoTextGeneratedError (#13542) - *Phantom* (2026-03-17T21:49:37+08:00)
- [`af51a27`](https://github.com/CherryHQ/cherry-studio/commit/af51a27b9b006c500449e44a1330f3011bbded82) fix(mcp): resolve hub tool auto-approve to underlying server (#13493) - *SuYao* (2026-03-16T20:57:19+08:00)
- [`83d7575`](https://github.com/CherryHQ/cherry-studio/commit/83d7575695332f9e475891f1b14f22903b45346d) fix(azure): keep dated api versions on chat transport (#13506) - *cherry-ai-bot[bot]* (2026-03-16T16:53:54+08:00)
- [`888ce83`](https://github.com/CherryHQ/cherry-studio/commit/888ce83fc752d6adc1ae4f1dd81cd192b5cb1415) feat(streaming): replace fixed timeout with resettable idle timeout (#13497) - *Phantom* (2026-03-16T15:02:08+08:00)
- [`f3244c3`](https://github.com/CherryHQ/cherry-studio/commit/f3244c3e9eb6d00e1d590f3a7a08be53def61754) fix(aiCore): bypass AI SDK model ID allowlist for reasoning detection (#13463) - *Phantom* (2026-03-14T19:25:14+08:00)
- [`ea694c6`](https://github.com/CherryHQ/cherry-studio/commit/ea694c630c933b1181479dec998390b11152338e) feat(assistant): add configurable max tool calls setting (#13398) - *George·Dong* (2026-03-13T23:39:31+08:00)
- [`4aef249`](https://github.com/CherryHQ/cherry-studio/commit/4aef24915138f75ab7fc743d9557929db4cbfd1b) fix: correctly pass poe web_search via extra_body when built-in search is enabled (#13434) - *Konv Suu* (2026-03-13T17:02:39+08:00)
- [`134280a`](https://github.com/CherryHQ/cherry-studio/commit/134280a8627931beffb2c37e1c5e58159392cef5) fix: use i18nKey for error display and add timeout enforcement (#12164) - *Phantom* (2026-03-13T10:06:14+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/ea6b2f83b9273201a5d25d7c5623b5c8425fdedc...d081b05c8724294944aaebdb5e7b156ee43997f7)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
