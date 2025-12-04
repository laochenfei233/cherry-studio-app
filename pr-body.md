## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 21
- **Lines Added**: +426
- **Lines Removed**: -111
- **Total Commits**: 14
- **Source Commit**: [`981bb9f`](https://github.com/CherryHQ/cherry-studio/commit/981bb9f451e0ac54c8cba18d24e5149db0320b3f)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`981bb9f`](https://github.com/CherryHQ/cherry-studio/commit/981bb9f451e0ac54c8cba18d24e5149db0320b3f) fix: update deepseek logic to match deepseek v3.2 (#11648) - *SuYao* (2025-12-04T19:13:51+08:00)
- [`f571dd7`](https://github.com/CherryHQ/cherry-studio/commit/f571dd7af0f98a7616dfd29af52c26695e65703c) fix: ollama url (#11611) - *槑囿脑袋* (2025-12-03T21:03:07+08:00)
- [`6696bca`](https://github.com/CherryHQ/cherry-studio/commit/6696bcacb8bf9df724d8f4394332f89892287c2f) fix(settings): fix wrong type caused by as assertion in OpenAI settings (#11631) - *Phantom* (2025-12-03T18:20:55+08:00)
- [`a1e95b5`](https://github.com/CherryHQ/cherry-studio/commit/a1e95b55f8d67d86e2a575b35aae6a9386053ded) fix: remove stale anthropic-beta header for oauth (#11600) - *Phantom* (2025-12-03T17:20:12+08:00)
- [`3aedf6f`](https://github.com/CherryHQ/cherry-studio/commit/3aedf6f1386f89d1640fa06bec40b1a4578b0919) fix: avoid sending empty anthropic-beta header (#11619) - *f14XuanLv* (2025-12-02T12:53:09+08:00)
- [`3e6dc56`](https://github.com/CherryHQ/cherry-studio/commit/3e6dc5619680ef5b56aa9be52e6beee9d3a1caea) fix(api): add withoutTrailingSharp utility and fix # handling in formatApiHost (#11604) - *Phantom* (2025-12-01T16:27:33+08:00)
- [`50a217a`](https://github.com/CherryHQ/cherry-studio/commit/50a217a6382f02648c863bc72d9de23de6ba785d) fix: separate undefined vs none reasoning effort (#11562) - *Phantom* (2025-11-30T15:37:18+08:00)
- [`444c13e`](https://github.com/CherryHQ/cherry-studio/commit/444c13e1e31fdedadcbab6b56851ec425865bc74) fix: correct trace token usage (#11575) - *Phantom* (2025-11-30T15:35:23+08:00)
- [`c23e88e`](https://github.com/CherryHQ/cherry-studio/commit/c23e88ecd1c073c7f4d0f0de4fc4cba99432437a) fix: handle Gemini API version correctly for Cloudflare Gateway URLs (#11543) - *Phantom* (2025-11-29T14:37:26+08:00)
- [`284d0f9`](https://github.com/CherryHQ/cherry-studio/commit/284d0f99e14918639b99ff1b39e4fe100aaf3523) fix(anthropic): comment out CONTEXT_100M_HEADER to handle via user preferences (#11545) - *Phantom* (2025-11-29T14:33:10+08:00)
- [`13ac5d5`](https://github.com/CherryHQ/cherry-studio/commit/13ac5d564a55f0fc98f1aa94600a2863ffd1d176) fix: match tool-call chunk with tool id (#11533) - *defi-failure* (2025-11-28T20:46:52+08:00)
- [`b18c64b`](https://github.com/CherryHQ/cherry-studio/commit/b18c64b7251c3a3e5e9395b25d6b71fc8567b809) feat: enhance support for AWS Bedrock and Azure OpenAI providers (#11510) - *SuYao* (2025-11-28T11:00:02+08:00)
- [`bf35902`](https://github.com/CherryHQ/cherry-studio/commit/bf35902696ce9f374b9f0a3d299faee8d51efa21) fix(mcp): ensure tool uniqueness by using tool IDs for multiple server instances (#11508) - *SuYao* (2025-11-27T22:35:24+08:00)
- [`0836eef`](https://github.com/CherryHQ/cherry-studio/commit/0836eef1a6a5bf95782315de891e39fa4153c0b3) fix: store JSON custom parameters as strings instead of objects (#11501) (#11503) - *xerxesliu* (2025-11-27T20:22:27+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/97519d96d751438d5ef31fe3d651fd6cf03a4ae0...981bb9f451e0ac54c8cba18d24e5149db0320b3f)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
