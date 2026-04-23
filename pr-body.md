## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 15
- **Lines Added**: +479
- **Lines Removed**: -364
- **Total Commits**: 9
- **Source Commit**: [`0636b60`](https://github.com/CherryHQ/cherry-studio/commit/0636b601f72ecf41fd253b8c21d95f78cc99cde7)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`0636b60`](https://github.com/CherryHQ/cherry-studio/commit/0636b601f72ecf41fd253b8c21d95f78cc99cde7) fix: limit builtin web search usage (#14466) - *亢奋猫* (2026-04-23T17:00:23+08:00)
- [`c0b3c88`](https://github.com/CherryHQ/cherry-studio/commit/c0b3c880e3b3846cf457648f3ed826b5e0f4e508) hotfix(ai-sdk/openai): patch @ai-sdk/openai to support gpt-image-2 (#14488) - *SuYao* (2026-04-22T23:29:50+08:00)
- [`5d98273`](https://github.com/CherryHQ/cherry-studio/commit/5d98273d86a9693158ad1a38402e1b0677882fad) fix(ai-core): keep native tool loops going (#14481) - *404-Page-Found* (2026-04-22T23:02:27+10:00)
- [`c4b3a93`](https://github.com/CherryHQ/cherry-studio/commit/c4b3a93ab0499100a0696738803dc7d4d6785c78) fix: prevent empty baseURL/region string in Bedrock provider config (#14425) - *Tsudrat* (2026-04-22T19:08:15+08:00)
- [`01caaf0`](https://github.com/CherryHQ/cherry-studio/commit/01caaf06f79a5cae507a69a6a6c82e3083161488) hotfix: disable native structured output for AiHubMix/NewAPI Anthropic models (#14376) - *SuYao* (2026-04-22T17:35:14+08:00)
- [`c2b3302`](https://github.com/CherryHQ/cherry-studio/commit/c2b3302581aa143ffbfceaeea356aaa5a9f18f11) hotfix: Custom params dropped by CherryIN/NewAPI — respect model.endpoint_type (#14409) - *zhibisora* (2026-04-22T14:39:21+08:00)
- [`da23022`](https://github.com/CherryHQ/cherry-studio/commit/da2302237b52588052f86372b8109b3c0a81c42b) fix: Fix Ollama model list loading when metadata contains null families values (#14364) - *Lance Diarmuid* (2026-04-18T21:58:23+08:00)
- [`fbda0d2`](https://github.com/CherryHQ/cherry-studio/commit/fbda0d213d7f7d589cbdcf90efca37768119dec8) hotfix: Custom params not passed to `Gemini` API when using `NewAPI`/`AiHubMix` (#14352) - *菠蘿包* (2026-04-18T17:32:21+08:00)
- [`4c264de`](https://github.com/CherryHQ/cherry-studio/commit/4c264de12f4920c79469272c0d274534141ea8ec) fix(provider): restore /v1 suffix for new-api host formatting (#14156) - *SuYao* (2026-04-10T12:30:37+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/1f72f9890508c6fc0bc95793e286cf61b991c51c...0636b601f72ecf41fd253b8c21d95f78cc99cde7)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
