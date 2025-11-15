## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 10
- **Lines Added**: +164
- **Lines Removed**: -25
- **Total Commits**: 7
- **Source Commit**: [`2511113`](https://github.com/CherryHQ/cherry-studio/commit/2511113b6244bce20498e2162fd7f9c1409c5140)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`2511113`](https://github.com/CherryHQ/cherry-studio/commit/2511113b6244bce20498e2162fd7f9c1409c5140) feat: support gpt-5.1 (#11294) - *Phantom* (2025-11-15T19:09:43+08:00)
- [`a29b2bb`](https://github.com/CherryHQ/cherry-studio/commit/a29b2bb3d6b762b30cd45dee62f3bd757d8e3331) chore: update @opeoginni/github-copilot-openai-compatible to support gpt5.1 (#11299) - *beyondkmp* (2025-11-15T19:07:16+08:00)
- [`4e699c4`](https://github.com/CherryHQ/cherry-studio/commit/4e699c48bc2fed6b268497bbd57502364d59af69) fix: update Azure OpenAI API version references to v1 in configuration and translations (#10799) - *SuYao* (2025-11-14T13:10:13+08:00)
- [`2b5ac5a`](https://github.com/CherryHQ/cherry-studio/commit/2b5ac5ab51e9191b46b5ddfdfeb358c498e8b929) feat: 添加 AI Gateway  Provider (#11064) - *SuYao* (2025-11-13T16:09:49+08:00)
- [`a6182ea`](https://github.com/CherryHQ/cherry-studio/commit/a6182eaf854a61a8fac21adcfd29fd4ede140774) Refactor/inputbar (#10332) - *SuYao* (2025-11-12T20:04:58+08:00)
- [`649f942`](https://github.com/CherryHQ/cherry-studio/commit/649f9420a4fa4e60276fd6d64335f5aeac9fb422) feat: add @cherrystudio/ai-sdk-provider package and integrate (#10715) - *MyPrototypeWhat* (2025-11-12T18:16:27+08:00)
- [`e2c8eda`](https://github.com/CherryHQ/cherry-studio/commit/e2c8edab61239365530d6d415e517f2ed0831c9f) fix: incorrect spelling caused Gemini endpoint’s thinking budget to fail (#11217) - *Konjac-XZ* (2025-11-10T16:42:34+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/78278ce96d72eaa2bdb62ec115cc872ee25227e4...2511113b6244bce20498e2162fd7f9c1409c5140)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
