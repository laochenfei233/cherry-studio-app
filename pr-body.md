## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 17
- **Lines Added**: +853
- **Lines Removed**: -110
- **Total Commits**: 8
- **Source Commit**: [`83d7575`](https://github.com/CherryHQ/cherry-studio/commit/83d7575695332f9e475891f1b14f22903b45346d)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`83d7575`](https://github.com/CherryHQ/cherry-studio/commit/83d7575695332f9e475891f1b14f22903b45346d) fix(azure): keep dated api versions on chat transport (#13506) - *cherry-ai-bot[bot]* (2026-03-16T16:53:54+08:00)
- [`888ce83`](https://github.com/CherryHQ/cherry-studio/commit/888ce83fc752d6adc1ae4f1dd81cd192b5cb1415) feat(streaming): replace fixed timeout with resettable idle timeout (#13497) - *Phantom* (2026-03-16T15:02:08+08:00)
- [`f3244c3`](https://github.com/CherryHQ/cherry-studio/commit/f3244c3e9eb6d00e1d590f3a7a08be53def61754) fix(aiCore): bypass AI SDK model ID allowlist for reasoning detection (#13463) - *Phantom* (2026-03-14T19:25:14+08:00)
- [`ea694c6`](https://github.com/CherryHQ/cherry-studio/commit/ea694c630c933b1181479dec998390b11152338e) feat(assistant): add configurable max tool calls setting (#13398) - *George·Dong* (2026-03-13T23:39:31+08:00)
- [`4aef249`](https://github.com/CherryHQ/cherry-studio/commit/4aef24915138f75ab7fc743d9557929db4cbfd1b) fix: correctly pass poe web_search via extra_body when built-in search is enabled (#13434) - *Konv Suu* (2026-03-13T17:02:39+08:00)
- [`134280a`](https://github.com/CherryHQ/cherry-studio/commit/134280a8627931beffb2c37e1c5e58159392cef5) fix: use i18nKey for error display and add timeout enforcement (#12164) - *Phantom* (2026-03-13T10:06:14+08:00)
- [`5f5ddb2`](https://github.com/CherryHQ/cherry-studio/commit/5f5ddb2b36d2418e2da21f4df6812c1e7a3bc06e) fix: correct Gemini reasoning params for none effort and Gemini 3 thinkingLevel (#13388) - *Phantom* (2026-03-12T15:03:24+08:00)
- [`2bbf09b`](https://github.com/CherryHQ/cherry-studio/commit/2bbf09b546262e4f7489e4a7a5815d5d0e8c0bd4) fix: upgrade xAI web search from deprecated Live Search to Responses API (#12812) - *PhoenixCPH* (2026-03-12T14:07:35+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/2cd3a81c5fa95f88dab7a0e4feb967766aac2917...83d7575695332f9e475891f1b14f22903b45346d)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
