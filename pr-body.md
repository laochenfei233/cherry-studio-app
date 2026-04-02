## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 96
- **Lines Added**: +4281
- **Lines Removed**: -13443
- **Total Commits**: 14
- **Source Commit**: [`3a568dd`](https://github.com/CherryHQ/cherry-studio/commit/3a568dd1add428388817746b41b74ac1c296c249)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`3a568dd`](https://github.com/CherryHQ/cherry-studio/commit/3a568dd1add428388817746b41b74ac1c296c249) fix: resolve CherryIN supported_endpoint_types not being detected - *suyao* (2026-04-02T20:21:36+08:00)
- [`b0d3092`](https://github.com/CherryHQ/cherry-studio/commit/b0d3092982f5d21b96da14e9950fd55e1b42e05f) fix(test): align providerConfig - *suyao* (2026-04-02T19:26:52+08:00)
- [`f990e20`](https://github.com/CherryHQ/cherry-studio/commit/f990e200a72b8e6dbd1e766112f7ef350d20481a) refactor: bump AI SDK deps and fix provider API host formatting - *suyao* (2026-04-02T19:19:13+08:00)
- [`c68cfd1`](https://github.com/CherryHQ/cherry-studio/commit/c68cfd13a232ef3d9139c28927568ec2f66360b5) fix: extend Qwen3.5 model detection to support Qwen3.5–3.9 series (#13979) - *Phantom* (2026-04-02T18:54:22+08:00)
- [`1c0a5a9`](https://github.com/CherryHQ/cherry-studio/commit/1c0a5a95faeea8a9b55e1ae647bc55692d167aec) refactor: migrate to ai sdk v6 Phase 3 (#12235) - *SuYao* (2026-04-02T15:38:23+08:00)
- [`62a27e6`](https://github.com/CherryHQ/cherry-studio/commit/62a27e6c482f2a36d0a10e72c43e3eacddd01766) fix(aiCore): move stream reading outside try-catch for correct abort flow (#13794) - *SuYao* (2026-04-01T12:47:25+08:00)
- [`88acf2e`](https://github.com/CherryHQ/cherry-studio/commit/88acf2e7b7378fda6cf121d556c209ec0305f524) fix(models): use word boundary matching for GPT model detection (#13927) - *Phantom* (2026-03-31T16:10:55+08:00)
- [`a69243c`](https://github.com/CherryHQ/cherry-studio/commit/a69243ca1360f34d41e12259cdfbbce55bfedda3) fix(poe): fix model loading and update default models (#13726) - *Kamil Jopek* (2026-03-31T01:28:11-05:00)
- [`4f8777b`](https://github.com/CherryHQ/cherry-studio/commit/4f8777bc0d2695f9326bbe68da8862ad048b44f7) fix(aiCore): handle NVIDIA provider reasoning params via chat_template_kwargs (#13846) - *Phantom* (2026-03-29T19:18:51+08:00)
- [`a9d3a3f`](https://github.com/CherryHQ/cherry-studio/commit/a9d3a3fe8688b826b2028689015958bf33741835) fix(aiCore): normalize model ID before looking up thinking token limits (#13843) - *Phantom* (2026-03-27T12:53:40+08:00)
- [`1d5bdfb`](https://github.com/CherryHQ/cherry-studio/commit/1d5bdfb5b692b042c5eb3194a50b9a16f99b1db3) fix(aiCore): remove openai-compatible providers from PDF native support list (#13809) - *SuYao* (2026-03-26T17:09:11+08:00)
- [`937c2e8`](https://github.com/CherryHQ/cherry-studio/commit/937c2e883e42ade72bbc51be221a12da38776216) refactor: add no-unnecessary-type-assertion rule and remove redundant assertions (#13741) - *Phantom* (2026-03-25T19:16:16+08:00)
- [`445208d`](https://github.com/CherryHQ/cherry-studio/commit/445208d3ecaeca105fc43dd699b3b8d581ecb1a3) fix(paintings): fix base64 image handling across providers (#13747) - *Pleasure1234* (2026-03-25T06:04:26Z)
- [`905fab5`](https://github.com/CherryHQ/cherry-studio/commit/905fab56dca7430cc9e5319b094d2520be67342a) fix: prevent CherryAI provider from using native PDF input in middleware (#13777) - *亢奋猫* (2026-03-25T12:11:23+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/f9f122a6354a5613ac018e7ad20962310b32ca86...3a568dd1add428388817746b41b74ac1c296c249)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
