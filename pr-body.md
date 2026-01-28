## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 8
- **Lines Added**: +560
- **Lines Removed**: -299
- **Total Commits**: 10
- **Source Commit**: [`742fbc5`](https://github.com/CherryHQ/cherry-studio/commit/742fbc555ee4222745d329d7a19c6ee1bd4fd611)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`742fbc5`](https://github.com/CherryHQ/cherry-studio/commit/742fbc555ee4222745d329d7a19c6ee1bd4fd611) feat: add Kimi K2.5 model support (#12620) - *Phantom* (2026-01-28T02:30:55+08:00)
- [`0d12da6`](https://github.com/CherryHQ/cherry-studio/commit/0d12da64689df3fdb9a812f4ced95aec175ecf34) fix: Correct reasoning parameters for Aliyun Bailian GLM models and support qwen3-max snapshots (#12614) - *Phantom* (2026-01-27T22:57:34+08:00)
- [`2a3e157`](https://github.com/CherryHQ/cherry-studio/commit/2a3e157ee7fd6121787ab4361b35907e359ca990) refactor(agent): improve tool call render ui/ux (#12540) - *SuYao* (2026-01-27T10:26:02+08:00)
- [`0255cb8`](https://github.com/CherryHQ/cherry-studio/commit/0255cb84435c817d0bc795276ed285abe5bb5079) fix: Improve provider config type safety and ensure required fields (#12589) - *Phantom* (2026-01-26T14:35:46+08:00)
- [`3737c16`](https://github.com/CherryHQ/cherry-studio/commit/3737c1680b6e5bbe0e50e7606345133642b9a035) Revert "fix(header): resolve User-Agent forbidden header in renderer process (#12549)" - *kangfenmao* (2026-01-25T21:17:54+08:00)
- [`56bfa95`](https://github.com/CherryHQ/cherry-studio/commit/56bfa95d08b2d7be144c809c1e426b98ffd293fa) fix(header): resolve User-Agent forbidden header in renderer process (#12549) - *SuYao* (2026-01-23T14:18:28+08:00)
- [`ac23c7f`](https://github.com/CherryHQ/cherry-studio/commit/ac23c7f30bee65449dc2df66d6ba64d1f093faec) fix(aiCore): preserve conversation history for image enhancement models (#12239) - *SuYao* (2026-01-14T14:23:19+08:00)
- [`9414f13`](https://github.com/CherryHQ/cherry-studio/commit/9414f13f6da5240c56e9e78e2ecaf599383cf88d) fix: 修改请求体字段名 (#12430) - *SuYao* (2026-01-12T16:38:55+08:00)
- [`cbeda03`](https://github.com/CherryHQ/cherry-studio/commit/cbeda03acbe780f72f8bf1aa2dbda6f525e1cdf4) use cumsum in anthropic cache (#12419) - *flt6* (2026-01-12T15:49:33+08:00)
- [`c7c380d`](https://github.com/CherryHQ/cherry-studio/commit/c7c380d706667f2f252438c971adade603f894e3) fix: disable strict JSON schema for OpenRouter to support MCP tools (#12415) - *SuYao* (2026-01-10T21:55:09+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/e8e8f028f38df2bda61cd04ba5369a4212382bf9...742fbc555ee4222745d329d7a19c6ee1bd4fd611)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
