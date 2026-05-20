## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 15
- **Lines Added**: +607
- **Lines Removed**: -133
- **Total Commits**: 9
- **Source Commit**: [`0412932`](https://github.com/CherryHQ/cherry-studio/commit/041293233e26a889bb24837c24029179734f5f91)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`0412932`](https://github.com/CherryHQ/cherry-studio/commit/041293233e26a889bb24837c24029179734f5f91) hotfix(model): align Gemini 3.x UI and sampling handling (#15204) - *Asurada* (2026-05-20T18:17:03+08:00)
- [`0b69721`](https://github.com/CherryHQ/cherry-studio/commit/0b697210bdb2180de45f86149cd7e0dbbeea108f) fix: support Grok 4.3 reasoning effort in xAI responses (#15137) - *Asurada* (2026-05-18T16:24:22+08:00)
- [`980d4ed`](https://github.com/CherryHQ/cherry-studio/commit/980d4ed7b703cc4681826aa81a998902be0913a3) fix(aiCore): Qiniu PDF fallback for GPT-5.4 (#15090) - *404-Page-Found* (2026-05-15T21:12:44+10:00)
- [`0bc0b49`](https://github.com/CherryHQ/cherry-studio/commit/0bc0b4980378aad2b3211f636423e8949098aea4) hotfix(aiCore): prevent crash when model.provider not found (#14999) (#15001) - *SuYao* (2026-05-14T15:19:22+08:00)
- [`008f5a8`](https://github.com/CherryHQ/cherry-studio/commit/008f5a8da73ac3cf3efb2feaa895fe94ad64ce5a) fix(ai): thread idle timeout handle to stream chunk adapter (#15056) - *George·Dong* (2026-05-13T20:38:09+08:00)
- [`c5e4409`](https://github.com/CherryHQ/cherry-studio/commit/c5e4409614c778316214c643d29416a0c91d5949) hotfix(models): support hosted Gemma 4 thinking mode (#14793) - *Asurada* (2026-05-08T01:37:28+08:00)
- [`1f86774`](https://github.com/CherryHQ/cherry-studio/commit/1f867749b8b2a3325813b6fac4dbc0d77f93516b) fix(anthropic): support Claude Opus 4.7 (#14349) - *SuYao* (2026-05-07T13:27:56+08:00)
- [`1680243`](https://github.com/CherryHQ/cherry-studio/commit/1680243a537bfb70d9b81b805acaaffd49b1473f) hotfix(gateway): bypass @ai-sdk/gateway schema for Vercel model listing (#14772) - *SuYao* (2026-05-02T20:35:53+08:00)
- [`c2a4ac5`](https://github.com/CherryHQ/cherry-studio/commit/c2a4ac568bbf730f331de5e0574cf04b521ef933) fix(reasoning): use enable_thinking param for SiliconFlow DeepSeek/Zhipu models when reasoning_effort is none (#14782) - *Qin Lingguang* (2026-05-02T09:28:34+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/000c8990a543e974a34997c0263e21352125e6e3...041293233e26a889bb24837c24029179734f5f91)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
