## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 37
- **Lines Added**: +4693
- **Lines Removed**: -247
- **Total Commits**: 16
- **Source Commit**: [`0836eef`](https://github.com/CherryHQ/cherry-studio/commit/0836eef1a6a5bf95782315de891e39fa4153c0b3)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`0836eef`](https://github.com/CherryHQ/cherry-studio/commit/0836eef1a6a5bf95782315de891e39fa4153c0b3) fix: store JSON custom parameters as strings instead of objects (#11501) (#11503) - *xerxesliu* (2025-11-27T20:22:27+08:00)
- [`82ef4a3`](https://github.com/CherryHQ/cherry-studio/commit/82ef4a32eb64806678254bc7b02f280689059bdf) Fix Poe API reasoning parameters for GPT-5 and reasoning models (#11379) - *Copilot* (2025-11-26T19:56:31+08:00)
- [`91f0c47`](https://github.com/CherryHQ/cherry-studio/commit/91f0c47b3310e60633d93d7c9b4437ed66278fb0) fix(anthropic): prevent duplicate /v1 in API endpoints (#11467) - *Phantom* (2025-11-26T19:26:39+08:00)
- [`0d69eea`](https://github.com/CherryHQ/cherry-studio/commit/0d69eeaccfcc9d1895122f6b90ccd48737fea591)  fix: improve Gemini reasoning and message handling (#11439) - *SuYao* (2025-11-26T15:46:52+08:00)
- [`a2de7d4`](https://github.com/CherryHQ/cherry-studio/commit/a2de7d48be7c9e662b01f5bd5e7b68b93ec46b67) fix: update Azure provider handling in AI SDK integration (#11465) - *SuYao* (2025-11-26T15:43:32+08:00)
- [`c1f4b5b`](https://github.com/CherryHQ/cherry-studio/commit/c1f4b5b9b9f8171fd8d05efeb5002b171ae65609) Fix: custom parameters for Gemini models (#11456) - *Copilot* (2025-11-26T13:16:58+08:00)
- [`e8de31c`](https://github.com/CherryHQ/cherry-studio/commit/e8de31ca641b5ae9cbbdee52d97b72e608d4ef97) fix: Groq verbosity setting (#11452) - *Phantom* (2025-11-25T23:29:03+08:00)
- [`0004a8c`](https://github.com/CherryHQ/cherry-studio/commit/0004a8cafee6ce86c2a34c6f57b06b14636673bb) fix: respect enableMaxTokens setting when maxTokens is not configured (#11438) - *fullex* (2025-11-25T11:12:50+08:00)
- [`475f718`](https://github.com/CherryHQ/cherry-studio/commit/475f718efb29b64c93171da57f8bf20edf79965e) fix: improve error handling and display in AiSdkToChunkAdapter (#11423) - *SuYao* (2025-11-24T10:57:51+08:00)
- [`2c33389`](https://github.com/CherryHQ/cherry-studio/commit/2c3338939ee974b52a59f4e9861db4d5c6cdfab4) feat: update Google and OpenAI SDKs with new features and fixes (#11395) - *SuYao* (2025-11-23T23:18:57+08:00)
- [`fa36112`](https://github.com/CherryHQ/cherry-studio/commit/fa361126b8d8b755c103f99d083a9f6253a6a1d1) refactor: aisdk config (#11402) - *Phantom* (2025-11-23T21:12:57+08:00)
- [`49903a1`](https://github.com/CherryHQ/cherry-studio/commit/49903a1567963f4bbae2ba221afafcc9fe7db92b) Test/ai-core (#11307) - *SuYao* (2025-11-23T17:33:27+08:00)
- [`c1f1d79`](https://github.com/CherryHQ/cherry-studio/commit/c1f1d7996d56a7a4f1486b3eafc33a07dca8e5a9) test: add thinking budget token test (#11305) - *SuYao* (2025-11-22T21:43:57+08:00)
- [`0a72c61`](https://github.com/CherryHQ/cherry-studio/commit/0a72c613af750a3ed2a4359e76b7a080fe32f7a0) fix(openai): apply verbosity setting with type safety improvements (#10964) - *Phantom* (2025-11-22T21:41:12+08:00)
- [`a1ac320`](https://github.com/CherryHQ/cherry-studio/commit/a1ac3207f1bed6e162e6a054dd3b7fcf02cd70e2) fix/anthropic-vertex (#11397) - *SuYao* (2025-11-22T20:56:05+08:00)
- [`c48f222`](https://github.com/CherryHQ/cherry-studio/commit/c48f222cdb694d0625bdd7596a25c51512b44b08) feat: add endpoint type support for cherryin provider (#11367) - *defi-failure* (2025-11-21T21:42:08+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/852192dce6d5a269c87d6a7daa5d230251db6b33...0836eef1a6a5bf95782315de891e39fa4153c0b3)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
