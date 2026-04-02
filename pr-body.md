## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 91
- **Lines Added**: +3987
- **Lines Removed**: -13419
- **Total Commits**: 7
- **Source Commit**: [`c68cfd1`](https://github.com/CherryHQ/cherry-studio/commit/c68cfd13a232ef3d9139c28927568ec2f66360b5)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`c68cfd1`](https://github.com/CherryHQ/cherry-studio/commit/c68cfd13a232ef3d9139c28927568ec2f66360b5) fix: extend Qwen3.5 model detection to support Qwen3.5–3.9 series (#13979) - *Phantom* (2026-04-02T18:54:22+08:00)
- [`1c0a5a9`](https://github.com/CherryHQ/cherry-studio/commit/1c0a5a95faeea8a9b55e1ae647bc55692d167aec) refactor: migrate to ai sdk v6 Phase 3 (#12235) - *SuYao* (2026-04-02T15:38:23+08:00)
- [`62a27e6`](https://github.com/CherryHQ/cherry-studio/commit/62a27e6c482f2a36d0a10e72c43e3eacddd01766) fix(aiCore): move stream reading outside try-catch for correct abort flow (#13794) - *SuYao* (2026-04-01T12:47:25+08:00)
- [`88acf2e`](https://github.com/CherryHQ/cherry-studio/commit/88acf2e7b7378fda6cf121d556c209ec0305f524) fix(models): use word boundary matching for GPT model detection (#13927) - *Phantom* (2026-03-31T16:10:55+08:00)
- [`a69243c`](https://github.com/CherryHQ/cherry-studio/commit/a69243ca1360f34d41e12259cdfbbce55bfedda3) fix(poe): fix model loading and update default models (#13726) - *Kamil Jopek* (2026-03-31T01:28:11-05:00)
- [`4f8777b`](https://github.com/CherryHQ/cherry-studio/commit/4f8777bc0d2695f9326bbe68da8862ad048b44f7) fix(aiCore): handle NVIDIA provider reasoning params via chat_template_kwargs (#13846) - *Phantom* (2026-03-29T19:18:51+08:00)
- [`a9d3a3f`](https://github.com/CherryHQ/cherry-studio/commit/a9d3a3fe8688b826b2028689015958bf33741835) fix(aiCore): normalize model ID before looking up thinking token limits (#13843) - *Phantom* (2026-03-27T12:53:40+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/1d5bdfb5b692b042c5eb3194a50b9a16f99b1db3...c68cfd13a232ef3d9139c28927568ec2f66360b5)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
