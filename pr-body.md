## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 16
- **Lines Added**: +319
- **Lines Removed**: -73
- **Total Commits**: 16
- **Source Commit**: [`cccf9bb`](https://github.com/CherryHQ/cherry-studio/commit/cccf9bb7be98469052e076ea00a6a1f596adb059)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`cccf9bb`](https://github.com/CherryHQ/cherry-studio/commit/cccf9bb7be98469052e076ea00a6a1f596adb059) feat: add latest zhipu models (#12169) - *tylinux* (2025-12-28T19:11:08+08:00)
- [`5ff173f`](https://github.com/CherryHQ/cherry-studio/commit/5ff173fcc7ffa39f0c45b84fbdacefe55432320b) fix(ollama): improve reasoningEffort handling in providerOptions (#12089) - *SuYao* (2025-12-28T17:04:45+08:00)
- [`99b431e`](https://github.com/CherryHQ/cherry-studio/commit/99b431ec9299add599e6f74067f058a954f83d02) fix: remove trailing api version in ANTHROPIC_BASE_URL (#12145) - *defi-failure* (2025-12-26T17:37:58+08:00)
- [`d9171e0`](https://github.com/CherryHQ/cherry-studio/commit/d9171e0596aa6956f9cae77b99ff1a4402bac7b1) fix(openrouter): support GPT-5.1/5.2 reasoning effort 'none' for OpenRouter and improve error handling (#12088) - *Phantom* (2025-12-24T14:18:41+08:00)
- [`09e58d3`](https://github.com/CherryHQ/cherry-studio/commit/09e58d37560a6ffd61c819dacd6ae7ac2429a00f) fix: interleaved thinking support (#12084) - *SuYao* (2025-12-23T20:08:53+08:00)
- [`6815ab6`](https://github.com/CherryHQ/cherry-studio/commit/6815ab65d124fb1aabdd674b9d107d346aa082b6) fix(memory): fix retrieval issues and enable database backup (#12073) - *亢奋猫* (2025-12-23T13:21:29+08:00)
- [`7a86297`](https://github.com/CherryHQ/cherry-studio/commit/7a862974c256afeef90d0d8441e6c96489edaaf9) fix(options): add support for persistent server configuration in OpenAI provider options (#12058) - *SuYao* (2025-12-22T16:13:31+08:00)
- [`a35bf4a`](https://github.com/CherryHQ/cherry-studio/commit/a35bf4afa1772ce6e95638c88d0f7cdd0f24bf9e) fix(azure-openai): normalize Azure endpoint (#12055) - *GeekMr* (2025-12-21T17:15:17+08:00)
- [`9f948e1`](https://github.com/CherryHQ/cherry-studio/commit/9f948e1ce7138d659d4cf19c8e3e199b4163ec68) fix(parameterBuilder): enhance urlContext validation for supported providers and models (#12046) - *sxjeru* (2025-12-20T20:14:40+08:00)
- [`4226071`](https://github.com/CherryHQ/cherry-studio/commit/42260710d84c68eb328cc1675185aa3264746643) fix(azure): restore deployment-based URLs for non-v1 apiVersion and add tests (#11966) - *GeekMr* (2025-12-18T18:12:26+08:00)
- [`5e8646c`](https://github.com/CherryHQ/cherry-studio/commit/5e8646c6a59b2206e8d6b7624db0f935fc194755) fix: update API path for image generation requests in OpenAIBaseClient - *kangfenmao* (2025-12-18T14:45:21+08:00)
- [`7e93e8b`](https://github.com/CherryHQ/cherry-studio/commit/7e93e8b9b20502af4e8ce5baa3cac46bbeff74e1) feat(gemini): add support for Gemini 3 Flash and Pro model detection (#11984) - *Phantom* (2025-12-18T14:35:36+08:00)
- [`eb7a2cc`](https://github.com/CherryHQ/cherry-studio/commit/eb7a2cc85ae98daa02b5268c3808297efdf30b93) feat: add support for Xiaomi MiMo model (#11961) - *SuYao* (2025-12-18T13:49:09+08:00)
- [`c04529a`](https://github.com/CherryHQ/cherry-studio/commit/c04529a23c0cd395a214591e6039f091ff7000f1) refactor: improve budget calculation logic (#11973) - *SuYao* (2025-12-18T13:30:41+08:00)
- [`0f1b3af`](https://github.com/CherryHQ/cherry-studio/commit/0f1b3afa72819cf4ce5bb2711ef3c5dd512cb7fd) feat: 添加火山引擎 Doubao-Seed-1.8 模型支持 (#11972) - *George·Dong* (2025-12-18T13:30:23+08:00)
- [`0cf0072`](https://github.com/CherryHQ/cherry-studio/commit/0cf0072b51a37ad638749818e5d2af7fac3c89b9) feat: add default reasoning effort option to resolve confusion between undefined and none (#11942) - *Phantom* (2025-12-18T13:00:23+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/150bb3e3a091618036ed8fbb5a2b295271ca8259...cccf9bb7be98469052e076ea00a6a1f596adb059)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
