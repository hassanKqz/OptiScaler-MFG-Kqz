# XeFG multi-frame generation (MFG) addition

This build is **wilsjo2/OptiScaler-DLSSNR-PreSR-Multipass** at commit `f45ccf3` (v0.8.91)
with the XeFG multi-frame generation unlock from **Hassankqz** (`OptiScaler-MFG-Kqz`) added on top.

What was added (from `OptiScaler-MFG-Kqz`, itself described there as based on `evairx/OptiScaler-MFG`):

- `OptiScaler/proxies/XeFGUnlock.h` - in-memory unlock of MFG in Intel's `libxess_fg.dll`
- `OptiScaler/proxies/XeFGPacing.h` - optional per-frame pacing above 2X
- XeFG interpolation-count handling and pacing hooks in `framegen/xefg/XeFG_Dx12.cpp`
- `[XeFG] UnlockMFG`, `MaxInterpolatedFrames`, `ExtraPacing` settings, the extended MFG menu and the "Extra Pacing" option

Everything else is unchanged from the base fork and upstream OptiScaler (cdozdil and contributors).
OptiScaler is licensed under GPLv3 (see `LICENSE`); this build stays under the same license.
This is unofficial and not supported by upstream OptiScaler, wilsjo2 or NVIDIA. See also `docs/CREDITS.md`.
