## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 25
- **Lines Added**: +702
- **Lines Removed**: -91
- **Total Commits**: 11
- **Source Commit**: [`937c2e8`](https://github.com/CherryHQ/cherry-studio/commit/937c2e883e42ade72bbc51be221a12da38776216)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`937c2e8`](https://github.com/CherryHQ/cherry-studio/commit/937c2e883e42ade72bbc51be221a12da38776216) refactor: add no-unnecessary-type-assertion rule and remove redundant assertions (#13741) - *Phantom* (2026-03-25T19:16:16+08:00)
- [`445208d`](https://github.com/CherryHQ/cherry-studio/commit/445208d3ecaeca105fc43dd699b3b8d581ecb1a3) fix(paintings): fix base64 image handling across providers (#13747) - *Pleasure1234* (2026-03-25T06:04:26Z)
- [`905fab5`](https://github.com/CherryHQ/cherry-studio/commit/905fab56dca7430cc9e5319b094d2520be67342a) fix: prevent CherryAI provider from using native PDF input in middleware (#13777) - *亢奋猫* (2026-03-25T12:11:23+08:00)
- [`f0774b5`](https://github.com/CherryHQ/cherry-studio/commit/f0774b5499f3337af215843574c574eee30b3cdf) fix(aiCore): fix temperature/topP incorrectly disabled when reasoning_effort is default (#13505) - *Phantom* (2026-03-24T15:29:20+08:00)
- [`0a7a2b9`](https://github.com/CherryHQ/cherry-studio/commit/0a7a2b9381f95f322c0a932d594ebf9b0582be8d) refactor: resolve all no-floating-promises lint violations (#13743) - *Phantom* (2026-03-24T14:00:03+08:00)
- [`d03388a`](https://github.com/CherryHQ/cherry-studio/commit/d03388ada0727b599f8dcf48f49df329fd1ddd61) fix(groq): add dedicated @ai-sdk/groq provider to avoid reasoning_content errors (#13735) - *SuYao* (2026-03-24T00:21:34+08:00)
- [`f878c5a`](https://github.com/CherryHQ/cherry-studio/commit/f878c5a39e729ae1bb6a3d64ae00c29dc2f71927) fix(memory): fix agentId filtering and search fallback in vector memory (#13725) - *Pleasure1234* (2026-03-23T13:57:48Z)
- [`3abca4a`](https://github.com/CherryHQ/cherry-studio/commit/3abca4a20922ea0d646eb171c5c86c2729b09b3f) fix: skip thinking budget subtraction for Claude 4.6 adaptive thinking models (#13676) - *lif* (2026-03-22T02:38:24+08:00)
- [`fb42d4d`](https://github.com/CherryHQ/cherry-studio/commit/fb42d4d0b5b40c3b0671d68905cad5322e857ff1) fix(aiCore): improve PDF processing robustness for aggregator providers (#13641) - *Phantom* (2026-03-20T14:29:53+08:00)
- [`65271f3`](https://github.com/CherryHQ/cherry-studio/commit/65271f386e80346637a00a1334ce6e928e1f4687) fix: route copilot gpt-5.4 models to responses (#13632) - *Konv Suu* (2026-03-20T10:05:05+08:00)
- [`62c1eb2`](https://github.com/CherryHQ/cherry-studio/commit/62c1eb28ce93735bbe839b66efd9cd8891ef43b9) fix: correct parameter order in knowledgeSearchTool call (#13635) - *Siin Xu* (2026-03-19T18:07:09+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/f6584848cbde77eb49f962e08763e9dda1340942...937c2e883e42ade72bbc51be221a12da38776216)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
