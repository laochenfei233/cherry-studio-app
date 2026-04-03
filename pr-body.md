## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 91
- **Lines Added**: +4195
- **Lines Removed**: -13416
- **Total Commits**: 8
- **Source Commit**: [`94d38a7`](https://github.com/CherryHQ/cherry-studio/commit/94d38a729d7d247bbf1d65b8519457fc9f0d9ee2)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`94d38a7`](https://github.com/CherryHQ/cherry-studio/commit/94d38a729d7d247bbf1d65b8519457fc9f0d9ee2) fix(models): add model capabilities, loosen schema validation, and support gemma4 (#13996) - *SuYao* (2026-04-03T13:39:00+08:00)
- [`6b14fcd`](https://github.com/CherryHQ/cherry-studio/commit/6b14fcd5ce0ca7e2f03f3ccfc9ce50cf9618d631) refactor: bump AI SDK deps and fix provider API host formatting - *suyao* (2026-04-02T19:19:13+08:00)
- [`9ee9605`](https://github.com/CherryHQ/cherry-studio/commit/9ee9605d772eddae7f91a2fe347ea989531386c6) fix: extend Qwen3.5 model detection to support Qwen3.5–3.9 series (#13979) - *Phantom* (2026-04-02T18:54:22+08:00)
- [`a58bbf5`](https://github.com/CherryHQ/cherry-studio/commit/a58bbf52fd6f404f4cade86be2086868644a70a0) refactor: migrate to ai sdk v6 Phase 3 (#12235) - *SuYao* (2026-04-02T15:38:23+08:00)
- [`18f0197`](https://github.com/CherryHQ/cherry-studio/commit/18f0197aa351a48f7973e3ec793f75de4b57fcd2) fix(aiCore): move stream reading outside try-catch for correct abort flow (#13794) - *SuYao* (2026-04-01T12:47:25+08:00)
- [`88acf2e`](https://github.com/CherryHQ/cherry-studio/commit/88acf2e7b7378fda6cf121d556c209ec0305f524) fix(models): use word boundary matching for GPT model detection (#13927) - *Phantom* (2026-03-31T16:10:55+08:00)
- [`a69243c`](https://github.com/CherryHQ/cherry-studio/commit/a69243ca1360f34d41e12259cdfbbce55bfedda3) fix(poe): fix model loading and update default models (#13726) - *Kamil Jopek* (2026-03-31T01:28:11-05:00)
- [`4f8777b`](https://github.com/CherryHQ/cherry-studio/commit/4f8777bc0d2695f9326bbe68da8862ad048b44f7) fix(aiCore): handle NVIDIA provider reasoning params via chat_template_kwargs (#13846) - *Phantom* (2026-03-29T19:18:51+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/d31652eafbad7655bdf5ea7f92804f5d0d9d87f2...94d38a729d7d247bbf1d65b8519457fc9f0d9ee2)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
