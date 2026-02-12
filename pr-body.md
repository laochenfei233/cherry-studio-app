## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 16
- **Lines Added**: +358
- **Lines Removed**: -69
- **Total Commits**: 7
- **Source Commit**: [`26a1f12`](https://github.com/CherryHQ/cherry-studio/commit/26a1f12d325b8346e352497b0ea2f4d2e6264343)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`26a1f12`](https://github.com/CherryHQ/cherry-studio/commit/26a1f12d325b8346e352497b0ea2f4d2e6264343) fix: prevent MCP multimodal tool results from exceeding API message size limits (#12735) - *Nakano Kenji* (2026-02-13T01:27:31+08:00)
- [`40317cd`](https://github.com/CherryHQ/cherry-studio/commit/40317cd3c8f0d8488b6c04239e23723fee468583) refactor: Convert WebSearchSource enum to const object with Zod schema (#12866) - *Phantom* (2026-02-13T00:25:56+08:00)
- [`51fb979`](https://github.com/CherryHQ/cherry-studio/commit/51fb979663ee5b5c40395af2ca2a3e5367ddee59) feat(analytics): track token usage for non-streaming completions (#12875) - *亢奋猫* (2026-02-12T11:11:43+08:00)
- [`095b20a`](https://github.com/CherryHQ/cherry-studio/commit/095b20a8d256a33ec5458df3e8eac2d40f8f279b) refactor: Improve file type naming for clarity and consistency (#12815) - *Phantom* (2026-02-10T12:07:00+08:00)
- [`9a44609`](https://github.com/CherryHQ/cherry-studio/commit/9a44609b7328960ba01ab4345310b3ab9b1067ac) refactor: remove DeepSeek v3.1+ provider whitelist for thinking control (#12824) - *Phantom* (2026-02-09T17:31:37+08:00)
- [`26f37c1`](https://github.com/CherryHQ/cherry-studio/commit/26f37c1c5691a72d0588e32ec7fc2b0ca9d8b0bb) feat: add Claude Opus 4.6 model support (#12777) - *Phantom* (2026-02-08T01:43:00+08:00)
- [`486ed0f`](https://github.com/CherryHQ/cherry-studio/commit/486ed0f148b421d78288f78881c68dcacf9a79fa) fix: handle Gemini OpenAI-compatible thought signatures and missing tool_call index (#12769) - *Phantom* (2026-02-07T23:55:33+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/5e2bdf4591e5df3ac0545b1f04b36317c3c8241b...26a1f12d325b8346e352497b0ea2f4d2e6264343)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
