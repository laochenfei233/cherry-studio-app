## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 7
- **Lines Added**: +237
- **Lines Removed**: -27
- **Total Commits**: 9
- **Source Commit**: [`9a44609`](https://github.com/CherryHQ/cherry-studio/commit/9a44609b7328960ba01ab4345310b3ab9b1067ac)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`9a44609`](https://github.com/CherryHQ/cherry-studio/commit/9a44609b7328960ba01ab4345310b3ab9b1067ac) refactor: remove DeepSeek v3.1+ provider whitelist for thinking control (#12824) - *Phantom* (2026-02-09T17:31:37+08:00)
- [`26f37c1`](https://github.com/CherryHQ/cherry-studio/commit/26f37c1c5691a72d0588e32ec7fc2b0ca9d8b0bb) feat: add Claude Opus 4.6 model support (#12777) - *Phantom* (2026-02-08T01:43:00+08:00)
- [`486ed0f`](https://github.com/CherryHQ/cherry-studio/commit/486ed0f148b421d78288f78881c68dcacf9a79fa) fix: handle Gemini OpenAI-compatible thought signatures and missing tool_call index (#12769) - *Phantom* (2026-02-07T23:55:33+08:00)
- [`ec3e277`](https://github.com/CherryHQ/cherry-studio/commit/ec3e27784dd8c1175ddcb4d2314ad6d8535ce2ed) fix: refine reasoning controls for Together and DashScope (#12737) - *Phantom* (2026-02-06T15:05:28+08:00)
- [`b8c3c7a`](https://github.com/CherryHQ/cherry-studio/commit/b8c3c7ae198c6cb59ac34e8d73ef5b632c629dc8) fix: resolve Uint8Array type incompatibility with BlobPart for tsgo (#12744) - *亢奋猫* (2026-02-06T13:40:22+08:00)
- [`888c6d7`](https://github.com/CherryHQ/cherry-studio/commit/888c6d7123af60654436c0fe52518b326481c97f) fix: align hub MCP tools with mcphub (remove search) (#12571) - *LiuVaayne* (2026-02-04T21:30:32+08:00)
- [`2167d96`](https://github.com/CherryHQ/cherry-studio/commit/2167d96e903369e4b5a145cf8747cb8dad41a8dd) fix(bedrock): reorder content blocks for Claude extended thinking (#12713) - *SuYao* (2026-02-04T15:32:20+08:00)
- [`ca46f6b`](https://github.com/CherryHQ/cherry-studio/commit/ca46f6b206cc7783f03aa0e0a8d222cb3274a283) fix: add placeholder text for image-only assistant messages (#12712) - *SuYao* (2026-02-04T14:04:56+08:00)
- [`4fb58f1`](https://github.com/CherryHQ/cherry-studio/commit/4fb58f1c38e523b1426929b52dc91a312b260d4f) fix: handle developer-to-system role conversion for Chat Completions API (#12709) - *SuYao* (2026-02-04T13:35:31+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/c53d6f3fd0df3bbf77f18300510f0f5d4ea37ed3...9a44609b7328960ba01ab4345310b3ab9b1067ac)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
