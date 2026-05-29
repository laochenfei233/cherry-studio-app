## 🤖 Automated Port from CherryHQ/cherry-studio

❌ **Status**: Patch failed to apply (manual porting required)

This PR automatically ports upstream aiCore changes with path transformation:
`src/renderer/src/aiCore` → `src/aiCore`

### 📊 Changes Summary

- **Files Changed**: 67
- **Lines Added**: +0
- **Lines Removed**: -20189
- **Total Commits**: 14
- **Source Commit**: [`53a3577`](https://github.com/CherryHQ/cherry-studio/commit/53a35773898bdd97ae888e849cbaa5f346a4ec0e)
- **Patch Status**: Patch failed to apply (manual porting required)

### 📝 Upstream Commits

- [`53a3577`](https://github.com/CherryHQ/cherry-studio/commit/53a35773898bdd97ae888e849cbaa5f346a4ec0e) refactor(renderer): flatten src/renderer/src to src/renderer - *fullex* (2026-05-28T21:40:20-07:00)
- [`fa5bbb7`](https://github.com/CherryHQ/cherry-studio/commit/fa5bbb760787f9913925689b6a0af1ab43ccf4e3) Merge branch 'main' of github.com:CherryHQ/cherry-studio into v2 - *fullex* (2026-05-28T19:38:52-07:00)
- [`d32cbec`](https://github.com/CherryHQ/cherry-studio/commit/d32cbecfa870af5c2b56a377c97d49e554284233) Fix: change Gemini Safety Settings to BLOCK_NONE - For main (#15303) - *ous fifty* (2026-05-28T10:48:46+08:00)
- [`9b1a658`](https://github.com/CherryHQ/cherry-studio/commit/9b1a65829f547ce29a9f68c93112b47f4a2d2629) fix(aiCore): do not treat Gemini model via non-Gemini provider as native PDF (#14329) - *Octopus* (2026-05-26T13:37:26+08:00)
- [`6a0f4d9`](https://github.com/CherryHQ/cherry-studio/commit/6a0f4d9c17eea87c796c5d4b27e89b94de6d25cc) fix: correct provider ID for AIHubMix reasoning effort (#15283) - *Nicholas-Xiong* (2026-05-24T01:20:55+08:00)
- [`8fe0d64`](https://github.com/CherryHQ/cherry-studio/commit/8fe0d6448a959854026d9f3e4542d1b63729c725) refactor(dead-code): remove orphaned modules and components after v2 migration - *fullex* (2026-05-22T08:45:28-07:00)
- [`0ef3e2b`](https://github.com/CherryHQ/cherry-studio/commit/0ef3e2bb4efc8bfe4d212f9b328b77cdcc69d9bd) refactor(naming): kebab-case to camelCase for non-component files - *fullex* (2026-05-22T06:27:25-07:00)
- [`977b381`](https://github.com/CherryHQ/cherry-studio/commit/977b381e51d04901781a28d43324fb15df6541fe) refactor(naming): normalize acronyms in renderer hooks & utils - *fullex* (2026-05-22T05:58:14-07:00)
- [`70b5c62`](https://github.com/CherryHQ/cherry-studio/commit/70b5c62c7c886f4fc90bf054cebb50046e206ba1) refactor(file-processing): migrate to JobManager (#15214) - *fullex* (2026-05-21T10:54:39+08:00)
- [`0412932`](https://github.com/CherryHQ/cherry-studio/commit/041293233e26a889bb24837c24029179734f5f91) hotfix(model): align Gemini 3.x UI and sampling handling (#15204) - *Asurada* (2026-05-20T18:17:03+08:00)
- [`0b69721`](https://github.com/CherryHQ/cherry-studio/commit/0b697210bdb2180de45f86149cd7e0dbbeea108f) fix: support Grok 4.3 reasoning effort in xAI responses (#15137) - *Asurada* (2026-05-18T16:24:22+08:00)
- [`980d4ed`](https://github.com/CherryHQ/cherry-studio/commit/980d4ed7b703cc4681826aa81a998902be0913a3) fix(aiCore): Qiniu PDF fallback for GPT-5.4 (#15090) - *404-Page-Found* (2026-05-15T21:12:44+10:00)
- [`0bc0b49`](https://github.com/CherryHQ/cherry-studio/commit/0bc0b4980378aad2b3211f636423e8949098aea4) hotfix(aiCore): prevent crash when model.provider not found (#14999) (#15001) - *SuYao* (2026-05-14T15:19:22+08:00)
- [`008f5a8`](https://github.com/CherryHQ/cherry-studio/commit/008f5a8da73ac3cf3efb2feaa895fe94ad64ce5a) fix(ai): thread idle timeout handle to stream chunk adapter (#15056) - *George·Dong* (2026-05-13T20:38:09+08:00)

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
- [Compare Changes](https://github.com/CherryHQ/cherry-studio/compare/73dc3fd3992e22f7294fc6295fee3dddfd541b7b...53a35773898bdd97ae888e849cbaa5f346a4ec0e)
- [Source aiCore Directory](https://github.com/CherryHQ/cherry-studio/tree/main/src/renderer/src/aiCore)
- [Expo FileSystem API](https://docs.expo.dev/versions/latest/sdk/filesystem/)

---

*🤖 This PR was automatically created by Port Bot*
*📅 Generated: $(date -u +"%Y-%m-%d %H:%M:%S UTC")*
