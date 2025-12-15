## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 17
- **Lines Added**: +412
- **Lines Removed**: -100
- **Total Commits**: 15
- **Source Commit**: [`71df9d6`](https://github.com/CherryHQ/cherry-studio/commit/71df9d61fd908abf08889bed824c4cce7dfd5c6f)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`71df9d6`](https://github.com/CherryHQ/cherry-studio/commit/71df9d61fd908abf08889bed824c4cce7dfd5c6f) fix(translate): default to first supported reasoning effort when translating (#11869) - *Phantom* (2025-12-15T15:43:00+08:00)
- [`fd92110`](https://github.com/CherryHQ/cherry-studio/commit/fd921103ddbae1ca57382f87a382ad7b12d270b3) fix: preserve thinking block (#11901) - *SuYao* (2025-12-14T20:05:45+08:00)
- [`ee7eee2`](https://github.com/CherryHQ/cherry-studio/commit/ee7eee24da007f1026e0dc198c63b1ec5a66414a) fix: max search result (#11883) - *SuYao* (2025-12-13T22:58:59+08:00)
- [`5bd550b`](https://github.com/CherryHQ/cherry-studio/commit/5bd550bfb41195b3c19070218767794bbfff167f) Fix/cannot get dimension (#11879) - *SuYao* (2025-12-13T21:09:38+08:00)
- [`dc0c47c`](https://github.com/CherryHQ/cherry-studio/commit/dc0c47c64d5991782560808723e8a27424e071b7) feat: support gpt 5.2 series (#11873) - *SuYao* (2025-12-12T22:53:10+08:00)
- [`66feee7`](https://github.com/CherryHQ/cherry-studio/commit/66feee714b9e9b445e0b6f0990723d2311f6fd5d) fix: use ModernAiProvider for embedding dimensions (#11876) - *defi-failure* (2025-12-12T18:48:38+08:00)
- [`97f6275`](https://github.com/CherryHQ/cherry-studio/commit/97f627510443460670603153f346e252be68cd4a) fix: update Ollama provider options for Qwen model support (#11850) - *Pleasure1234* (2025-12-12T08:48:12Z)
- [`b906849`](https://github.com/CherryHQ/cherry-studio/commit/b906849c177b48644ccf4daf21041fe058b0a793) fix: update anthropicBaseURL and geminiBaseURL for cherryin provider to include versioning - *kangfenmao* (2025-12-12T16:11:20+08:00)
- [`d7b9a6e`](https://github.com/CherryHQ/cherry-studio/commit/d7b9a6e09a87058cba576f0aa51c3c36b6cb25f7) fix: remove cloneDeep to prevent stack overflow with base64 images (#11761) - *Copilot* (2025-12-12T15:16:31+08:00)
- [`c1bf6cf`](https://github.com/CherryHQ/cherry-studio/commit/c1bf6cfbb712eeeba81d6ca2876d593c56871bec) fix: add gpustack provider for qwen3 enable think (#11843) - *SuYao* (2025-12-11T18:16:47+08:00)
- [`5f3af64`](https://github.com/CherryHQ/cherry-studio/commit/5f3af646f4307f01b083c9ae78c422eca16a5c53) fix: update CherryIN API URL and add thinking budget parameter - *kangfenmao* (2025-12-11T15:43:28+08:00)
- [`76524d6`](https://github.com/CherryHQ/cherry-studio/commit/76524d68c6ba2e79a1e92f2bb23a60c24bd38702) feat: add CherryIN API host selection settings (#11797) - *亢奋猫* (2025-12-11T11:19:28+08:00)
- [`058a2c7`](https://github.com/CherryHQ/cherry-studio/commit/058a2c763b41ff08720e077d24089c6e97ef268a) fix: restore API version control with trailing # delimiter (addresses #11750) (#11773) - *Phantom* (2025-12-10T13:42:15+08:00)
- [`0861902`](https://github.com/CherryHQ/cherry-studio/commit/086190228a14c96d42165e996f2481461120e8da) fix(aiCore): correct provider adaptation with model parameter (#11758) - *Phantom* (2025-12-09T10:42:18+08:00)
- [`73fc74d`](https://github.com/CherryHQ/cherry-studio/commit/73fc74d875d7652e25fcbf8275498c3b7e835c47) fix: add support for OpenRouter embeddings in listModels method (#11774) - *SuYao* (2025-12-09T10:29:35+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/e6003463ac240dce491c1e6f230f312c4d65926c...71df9d61fd908abf08889bed824c4cce7dfd5c6f)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
