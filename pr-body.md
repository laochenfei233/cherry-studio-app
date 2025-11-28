## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 38
- **Lines Added**: +4643
- **Lines Removed**: -266
- **Total Commits**: 15
- **Source Commit**: [`13ac5d5`](https://github.com/CherryHQ/cherry-studio/commit/13ac5d564a55f0fc98f1aa94600a2863ffd1d176)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`13ac5d5`](https://github.com/CherryHQ/cherry-studio/commit/13ac5d564a55f0fc98f1aa94600a2863ffd1d176) fix: match tool-call chunk with tool id (#11533) - *defi-failure* (2025-11-28T20:46:52+08:00)
- [`b18c64b`](https://github.com/CherryHQ/cherry-studio/commit/b18c64b7251c3a3e5e9395b25d6b71fc8567b809) feat: enhance support for AWS Bedrock and Azure OpenAI providers (#11510) - *SuYao* (2025-11-28T11:00:02+08:00)
- [`bf35902`](https://github.com/CherryHQ/cherry-studio/commit/bf35902696ce9f374b9f0a3d299faee8d51efa21) fix(mcp): ensure tool uniqueness by using tool IDs for multiple server instances (#11508) - *SuYao* (2025-11-27T22:35:24+08:00)
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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/c9be949853351b967339eeb4d8041d56a1dbf83b...13ac5d564a55f0fc98f1aa94600a2863ffd1d176)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
