## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 17
- **Lines Added**: +373
- **Lines Removed**: -133
- **Total Commits**: 16
- **Source Commit**: [`a35bf4a`](https://github.com/CherryHQ/cherry-studio/commit/a35bf4afa1772ce6e95638c88d0f7cdd0f24bf9e)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`a35bf4a`](https://github.com/CherryHQ/cherry-studio/commit/a35bf4afa1772ce6e95638c88d0f7cdd0f24bf9e) fix(azure-openai): normalize Azure endpoint (#12055) - *GeekMr* (2025-12-21T17:15:17+08:00)
- [`9f948e1`](https://github.com/CherryHQ/cherry-studio/commit/9f948e1ce7138d659d4cf19c8e3e199b4163ec68) fix(parameterBuilder): enhance urlContext validation for supported providers and models (#12046) - *sxjeru* (2025-12-20T20:14:40+08:00)
- [`4226071`](https://github.com/CherryHQ/cherry-studio/commit/42260710d84c68eb328cc1675185aa3264746643) fix(azure): restore deployment-based URLs for non-v1 apiVersion and add tests (#11966) - *GeekMr* (2025-12-18T18:12:26+08:00)
- [`5e8646c`](https://github.com/CherryHQ/cherry-studio/commit/5e8646c6a59b2206e8d6b7624db0f935fc194755) fix: update API path for image generation requests in OpenAIBaseClient - *kangfenmao* (2025-12-18T14:45:21+08:00)
- [`7e93e8b`](https://github.com/CherryHQ/cherry-studio/commit/7e93e8b9b20502af4e8ce5baa3cac46bbeff74e1) feat(gemini): add support for Gemini 3 Flash and Pro model detection (#11984) - *Phantom* (2025-12-18T14:35:36+08:00)
- [`eb7a2cc`](https://github.com/CherryHQ/cherry-studio/commit/eb7a2cc85ae98daa02b5268c3808297efdf30b93) feat: add support for Xiaomi MiMo model (#11961) - *SuYao* (2025-12-18T13:49:09+08:00)
- [`c04529a`](https://github.com/CherryHQ/cherry-studio/commit/c04529a23c0cd395a214591e6039f091ff7000f1) refactor: improve budget calculation logic (#11973) - *SuYao* (2025-12-18T13:30:41+08:00)
- [`0f1b3af`](https://github.com/CherryHQ/cherry-studio/commit/0f1b3afa72819cf4ce5bb2711ef3c5dd512cb7fd) feat: 添加火山引擎 Doubao-Seed-1.8 模型支持 (#11972) - *George·Dong* (2025-12-18T13:30:23+08:00)
- [`0cf0072`](https://github.com/CherryHQ/cherry-studio/commit/0cf0072b51a37ad638749818e5d2af7fac3c89b9) feat: add default reasoning effort option to resolve confusion between undefined and none (#11942) - *Phantom* (2025-12-18T13:00:23+08:00)
- [`ef25eef`](https://github.com/CherryHQ/cherry-studio/commit/ef25eef0ebc6d3dbb754780669593a7a9f3c1d7d) feat(knowledge): use prompt injection for forced knowledge base search - *kangfenmao* (2025-12-16T12:18:11+08:00)
- [`bfeef7e`](https://github.com/CherryHQ/cherry-studio/commit/bfeef7ef911698af77f7f853bec03c239233e7e8) fix: refactor provider headers logic in providerConfig (#11849) - *Pleasure1234* (2025-12-17T07:21:06Z)
- [`71df9d6`](https://github.com/CherryHQ/cherry-studio/commit/71df9d61fd908abf08889bed824c4cce7dfd5c6f) fix(translate): default to first supported reasoning effort when translating (#11869) - *Phantom* (2025-12-15T15:43:00+08:00)
- [`fd92110`](https://github.com/CherryHQ/cherry-studio/commit/fd921103ddbae1ca57382f87a382ad7b12d270b3) fix: preserve thinking block (#11901) - *SuYao* (2025-12-14T20:05:45+08:00)
- [`ee7eee2`](https://github.com/CherryHQ/cherry-studio/commit/ee7eee24da007f1026e0dc198c63b1ec5a66414a) fix: max search result (#11883) - *SuYao* (2025-12-13T22:58:59+08:00)
- [`5bd550b`](https://github.com/CherryHQ/cherry-studio/commit/5bd550bfb41195b3c19070218767794bbfff167f) Fix/cannot get dimension (#11879) - *SuYao* (2025-12-13T21:09:38+08:00)
- [`dc0c47c`](https://github.com/CherryHQ/cherry-studio/commit/dc0c47c64d5991782560808723e8a27424e071b7) feat: support gpt 5.2 series (#11873) - *SuYao* (2025-12-12T22:53:10+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/66feee714b9e9b445e0b6f0990723d2311f6fd5d...a35bf4afa1772ce6e95638c88d0f7cdd0f24bf9e)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
