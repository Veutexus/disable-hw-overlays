# disable-hw-overlays

A simple **module** that automatically disables hardware overlays (HW overlays) on every boot, so you don't need to toggle it manually in Developer Options every time. Should basically work with/on all common root managers (e.g. Magisk, KernelSU, APatch…).

It uses the following service call to SurfaceFlinger:  
```bash
service call SurfaceFlinger 1008 i32 1
```

Disabling HW overlays may reduce UI stuttering and make your device's interface feel a little smoother. Some users also report improved touch responsiveness and fewer touch interruptions.

## How it works
When enabled (default): Android uses the CPU to composite certain screen elements (e.g., status bar, notifications), which can strain the CPU and cause lag on some older devices.

When disabled: The GPU handles compositing instead, which may improve performance on some devices (results vary).

## Disclaimer
This tweak may cause unknown visual artifacts, weird transparency glitches, other rendering issues, or increased power consumption.

**Flash at your own risk!**
