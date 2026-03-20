## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 19
- **Lines Added**: +543
- **Lines Removed**: -53
- **Total Commits**: 10
- **Source Commit**: [`fb42d4d`](https://github.com/CherryHQ/cherry-studio/commit/fb42d4d0b5b40c3b0671d68905cad5322e857ff1)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`fb42d4d`](https://github.com/CherryHQ/cherry-studio/commit/fb42d4d0b5b40c3b0671d68905cad5322e857ff1) fix(aiCore): improve PDF processing robustness for aggregator providers (#13641) - *Phantom* (2026-03-20T14:29:53+08:00)
- [`65271f3`](https://github.com/CherryHQ/cherry-studio/commit/65271f386e80346637a00a1334ce6e928e1f4687) fix: route copilot gpt-5.4 models to responses (#13632) - *Konv Suu* (2026-03-20T10:05:05+08:00)
- [`62c1eb2`](https://github.com/CherryHQ/cherry-studio/commit/62c1eb28ce93735bbe839b66efd9cd8891ef43b9) fix: correct parameter order in knowledgeSearchTool call (#13635) - *Siin Xu* (2026-03-19T18:07:09+08:00)
- [`d081b05`](https://github.com/CherryHQ/cherry-studio/commit/d081b05c8724294944aaebdb5e7b156ee43997f7) fix: Format provider API hosts in API server & refactor shared utilities (#13198) - *Phantom* (2026-03-19T00:41:20+08:00)
- [`a4cc48a`](https://github.com/CherryHQ/cherry-studio/commit/a4cc48a84621f3217fdb2910497ad9e4d5e4deac) refactor: consolidate qwen model definitions and update related references - *kangfenmao* (2026-03-18T19:09:48+08:00)
- [`21a8c62`](https://github.com/CherryHQ/cherry-studio/commit/21a8c625cb16f9f0d7b9caa293d6350e52a376e7) fix: add budgetTokens fallback for Agent thinking compatibility (#13575) - *Phantom* (2026-03-18T12:21:09+08:00)
- [`3f9cb07`](https://github.com/CherryHQ/cherry-studio/commit/3f9cb07cbef0ab20edf72f1236556de4d14f1099) fix: propagate actual stream errors instead of generic NoTextGeneratedError (#13542) - *Phantom* (2026-03-17T21:49:37+08:00)
- [`af51a27`](https://github.com/CherryHQ/cherry-studio/commit/af51a27b9b006c500449e44a1330f3011bbded82) fix(mcp): resolve hub tool auto-approve to underlying server (#13493) - *SuYao* (2026-03-16T20:57:19+08:00)
- [`83d7575`](https://github.com/CherryHQ/cherry-studio/commit/83d7575695332f9e475891f1b14f22903b45346d) fix(azure): keep dated api versions on chat transport (#13506) - *cherry-ai-bot[bot]* (2026-03-16T16:53:54+08:00)
- [`888ce83`](https://github.com/CherryHQ/cherry-studio/commit/888ce83fc752d6adc1ae4f1dd81cd192b5cb1415) feat(streaming): replace fixed timeout with resettable idle timeout (#13497) - *Phantom* (2026-03-16T15:02:08+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/774cb7a73c5f11091d93cfa1b6b5f7aed912f032...fb42d4d0b5b40c3b0671d68905cad5322e857ff1)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
