## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 16
- **Lines Added**: +868
- **Lines Removed**: -366
- **Total Commits**: 12
- **Source Commit**: [`63be624`](https://github.com/CherryHQ/cherry-studio/commit/63be624f7c0500e2cf8ab8af01f050df6d32c9f8)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`63be624`](https://github.com/CherryHQ/cherry-studio/commit/63be624f7c0500e2cf8ab8af01f050df6d32c9f8) fix(models): add vision and reasoning_effort support for mistral-small-2603 (#14541) - *George·Dong* (2026-04-25T02:22:23+08:00)
- [`4e1e454`](https://github.com/CherryHQ/cherry-studio/commit/4e1e4548bb86ccce752a8ca60a581b37b7bc9b1d) hotfix(deepseek): forward reasoning effort for DeepSeek V4+ via Claude endpoint (#14572) - *SuYao* (2026-04-25T02:12:47+08:00)
- [`774aa67`](https://github.com/CherryHQ/cherry-studio/commit/774aa674d25005ba0cbc70cfa14b36c68d1ac2a9) hotfix(copilot): github copilot model fetch (#14566) - *Asurada* (2026-04-24T23:06:10+08:00)
- [`e17d573`](https://github.com/CherryHQ/cherry-studio/commit/e17d5737555e1bb7d7d6145ea37232c732f79df3) hotfix(models): add DeepSeek V4+ model support with reasoning effort (#14551) - *Siin Xu* (2026-04-23T23:30:23-07:00)
- [`0636b60`](https://github.com/CherryHQ/cherry-studio/commit/0636b601f72ecf41fd253b8c21d95f78cc99cde7) fix: limit builtin web search usage (#14466) - *亢奋猫* (2026-04-23T17:00:23+08:00)
- [`c0b3c88`](https://github.com/CherryHQ/cherry-studio/commit/c0b3c880e3b3846cf457648f3ed826b5e0f4e508) hotfix(ai-sdk/openai): patch @ai-sdk/openai to support gpt-image-2 (#14488) - *SuYao* (2026-04-22T23:29:50+08:00)
- [`5d98273`](https://github.com/CherryHQ/cherry-studio/commit/5d98273d86a9693158ad1a38402e1b0677882fad) fix(ai-core): keep native tool loops going (#14481) - *404-Page-Found* (2026-04-22T23:02:27+10:00)
- [`c4b3a93`](https://github.com/CherryHQ/cherry-studio/commit/c4b3a93ab0499100a0696738803dc7d4d6785c78) fix: prevent empty baseURL/region string in Bedrock provider config (#14425) - *Tsudrat* (2026-04-22T19:08:15+08:00)
- [`01caaf0`](https://github.com/CherryHQ/cherry-studio/commit/01caaf06f79a5cae507a69a6a6c82e3083161488) hotfix: disable native structured output for AiHubMix/NewAPI Anthropic models (#14376) - *SuYao* (2026-04-22T17:35:14+08:00)
- [`c2b3302`](https://github.com/CherryHQ/cherry-studio/commit/c2b3302581aa143ffbfceaeea356aaa5a9f18f11) hotfix: Custom params dropped by CherryIN/NewAPI — respect model.endpoint_type (#14409) - *zhibisora* (2026-04-22T14:39:21+08:00)
- [`da23022`](https://github.com/CherryHQ/cherry-studio/commit/da2302237b52588052f86372b8109b3c0a81c42b) fix: Fix Ollama model list loading when metadata contains null families values (#14364) - *Lance Diarmuid* (2026-04-18T21:58:23+08:00)
- [`fbda0d2`](https://github.com/CherryHQ/cherry-studio/commit/fbda0d213d7f7d589cbdcf90efca37768119dec8) hotfix: Custom params not passed to `Gemini` API when using `NewAPI`/`AiHubMix` (#14352) - *菠蘿包* (2026-04-18T17:32:21+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/0d7e13bd48efce3bd32e5c38d66eeec9a22c9484...63be624f7c0500e2cf8ab8af01f050df6d32c9f8)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
