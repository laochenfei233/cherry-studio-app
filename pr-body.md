## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 70
- **Lines Added**: +488
- **Lines Removed**: -400
- **Total Commits**: 8
- **Source Commit**: [`bd94d23`](https://github.com/CherryHQ/cherry-studio/commit/bd94d2334316a66f50ad9e899e822b9f2f6a3374)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`bd94d23`](https://github.com/CherryHQ/cherry-studio/commit/bd94d2334316a66f50ad9e899e822b9f2f6a3374) refactor:Unify the naming of configuration fields in thinking, change to using underscore style. (#11106) - *SuYao* (2025-11-02T19:24:23+08:00)
- [`5f1c14e`](https://github.com/CherryHQ/cherry-studio/commit/5f1c14e2c03af79c1301ac43ade9e220848a959b) fix(aihubmix): fix default rules missing app code (#11100) - *chenxue* (2025-11-02T17:03:05+08:00)
- [`dc06c10`](https://github.com/CherryHQ/cherry-studio/commit/dc06c103e0e1ea93c66fec586df665a6c4a42194) chore[lint]: add import type lint (#11091) - *fullex* (2025-11-01T10:40:02+08:00)
- [`e0a2ed0`](https://github.com/CherryHQ/cherry-studio/commit/e0a2ed04810f424b2606cf3ec32a0abfdcdcac48) Provider Config & anthropic-web-fetch (#10808) - *SuYao* (2025-10-29T14:47:21+08:00)
- [`56d6827`](https://github.com/CherryHQ/cherry-studio/commit/56d68276e15481e6800ae7ae9434ae648e17d7a8) fix(knowledge): force choose knowledge aisdk error (#11006) - *槑囿脑袋* (2025-10-28T16:37:58+08:00)
- [`29c1173`](https://github.com/CherryHQ/cherry-studio/commit/29c11733654da645d3cfc0afea9279a76b3b23d9) Fix Qwen3 thinking mode control for Ollama using aiCore middleware (#10947) - *Copilot* (2025-10-28T14:26:54+08:00)
- [`250f592`](https://github.com/CherryHQ/cherry-studio/commit/250f59234b472ac1c66551e8ad4683a03d663cb2) feat: add isClaude45ReasoningModel function and update getTopP logic (#10988) - *SuYao* (2025-10-27T20:34:11+08:00)
- [`82132d4`](https://github.com/CherryHQ/cherry-studio/commit/82132d479a195f82a62de9521b3491c718e0a6f2) feat: add huggingface provider (#10966) - *SuYao* (2025-10-27T13:30:23+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/f5a1d3f8d0722eef6562eed604f8a1993d2e94d1...bd94d2334316a66f50ad9e899e822b9f2f6a3374)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
