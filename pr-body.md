## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 15
- **Lines Added**: +827
- **Lines Removed**: -136
- **Total Commits**: 7
- **Source Commit**: [`5f5ddb2`](https://github.com/CherryHQ/cherry-studio/commit/5f5ddb2b36d2418e2da21f4df6812c1e7a3bc06e)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`5f5ddb2`](https://github.com/CherryHQ/cherry-studio/commit/5f5ddb2b36d2418e2da21f4df6812c1e7a3bc06e) fix: correct Gemini reasoning params for none effort and Gemini 3 thinkingLevel (#13388) - *Phantom* (2026-03-12T15:03:24+08:00)
- [`2bbf09b`](https://github.com/CherryHQ/cherry-studio/commit/2bbf09b546262e4f7489e4a7a5815d5d0e8c0bd4) fix: upgrade xAI web search from deprecated Live Search to Responses API (#12812) - *PhoenixCPH* (2026-03-12T14:07:35+08:00)
- [`bec5ea4`](https://github.com/CherryHQ/cherry-studio/commit/bec5ea4f46cf394ead2c64d5c6a8e73c140521b5) fix: auto-convert reasoning_effort to reasoningEffort for openai-compatible providers (#12831) - *SuYao* (2026-03-11T11:05:30+08:00)
- [`5a2a609`](https://github.com/CherryHQ/cherry-studio/commit/5a2a6092642c9faaf3369d778df8cc76d25993d4) fix: check underlying tool permissions for hub invoke/exec (#13282) - *SuYao* (2026-03-09T20:14:35+08:00)
- [`27ef9b8`](https://github.com/CherryHQ/cherry-studio/commit/27ef9b8123d655c391668a0b232e6082269a0829) fix: remove approval countdown timers and add system notifications (#13281) - *SuYao* (2026-03-09T20:14:22+08:00)
- [`b848580`](https://github.com/CherryHQ/cherry-studio/commit/b8485805296a5843f3d31d9624106b5216169192) feat(gemini): add thought signature persistence for conversation replay (#13100) - *Phantom* (2026-03-07T15:09:17+08:00)
- [`1c6ec3e`](https://github.com/CherryHQ/cherry-studio/commit/1c6ec3eadaecbe2f8a8834ab721adfc84186698c) fix: improve Qwen 3.5 reasoning model detection and thinking param handling (#13235) - *Phantom* (2026-03-05T18:36:15+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/2272f9c25512f91965f4404f2f4570def045aeaa...5f5ddb2b36d2418e2da21f4df6812c1e7a3bc06e)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
