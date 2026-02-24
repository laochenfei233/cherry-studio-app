## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 16
- **Lines Added**: +259
- **Lines Removed**: -67
- **Total Commits**: 6
- **Source Commit**: [`7cca235`](https://github.com/CherryHQ/cherry-studio/commit/7cca23571a7be73e8499d8d6aa138ce9e6b231d2)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`7cca235`](https://github.com/CherryHQ/cherry-studio/commit/7cca23571a7be73e8499d8d6aa138ce9e6b231d2) feat: Add Claude Sonnet 4.6 model support to Anthropic provider (#13016) - *Phantom* (2026-02-24T20:03:10+08:00)
- [`a6cfe6b`](https://github.com/CherryHQ/cherry-studio/commit/a6cfe6ba0f2999c3afcd50b5c7913a911d24bb6d) feat(zhipu): add GLM-5 model support (#12942) - *Wike* (2026-02-17T12:05:53+08:00)
- [`26a1f12`](https://github.com/CherryHQ/cherry-studio/commit/26a1f12d325b8346e352497b0ea2f4d2e6264343) fix: prevent MCP multimodal tool results from exceeding API message size limits (#12735) - *Nakano Kenji* (2026-02-13T01:27:31+08:00)
- [`40317cd`](https://github.com/CherryHQ/cherry-studio/commit/40317cd3c8f0d8488b6c04239e23723fee468583) refactor: Convert WebSearchSource enum to const object with Zod schema (#12866) - *Phantom* (2026-02-13T00:25:56+08:00)
- [`51fb979`](https://github.com/CherryHQ/cherry-studio/commit/51fb979663ee5b5c40395af2ca2a3e5367ddee59) feat(analytics): track token usage for non-streaming completions (#12875) - *亢奋猫* (2026-02-12T11:11:43+08:00)
- [`095b20a`](https://github.com/CherryHQ/cherry-studio/commit/095b20a8d256a33ec5458df3e8eac2d40f8f279b) refactor: Improve file type naming for clarity and consistency (#12815) - *Phantom* (2026-02-10T12:07:00+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/81e8bab7941ad165009f48d32021c5f0fcd5544f...7cca23571a7be73e8499d8d6aa138ce9e6b231d2)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
