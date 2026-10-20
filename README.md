# 📦 Onyx local manifests

```
# Clone local_manifests repository
git clone -b main https://github.com/Onyx-Odyssey/local_manifests .repo/local_manifests
```

Run it from the ROM root, after `repo init`, then `repo sync -c -j8`.

## 📱 Device & Vendor

* 🌳 **Onyx Device Tree** — `device/xiaomi/onyx` → [`android_device_xiaomi_onyx`](https://github.com/Onyx-Odyssey/android_device_xiaomi_onyx) (`lineage-23.2`)
* 🏭 **Onyx Vendor Tree** — `vendor/xiaomi/onyx` → [`proprietary_vendor_xiaomi_onyx`](https://gitlab.com/sachinbarange86/proprietary_vendor_xiaomi_onyx) (`16.2`, GitLab)
* 📷 **Leica Camera** — `vendor/xiaomi/onyx-leicacamera` → [`android_vendor_xiaomi_onyx-leicacamera`](https://gitlab.com/sachinbarange86/android_vendor_xiaomi_onyx-leicacamera) (`lineage-23.2`, GitLab)

## ⚡ Kernel & Hardware

* 🧠 **Onyx Kernel Source** — `kernel/xiaomi/onyx` → [`android_kernel_xiaomi_onyx`](https://github.com/Onyx-Odyssey/android_kernel_xiaomi_onyx) (`lineage-23.2`)
* 🧩 **Onyx Kernel Modules** — `kernel/xiaomi/onyx-modules` → [`android_kernel_xiaomi_onyx-modules`](https://github.com/Onyx-Odyssey/android_kernel_xiaomi_onyx-modules) (`lineage-23.2`)
* 🌲 **Onyx Kernel Devicetrees** — `kernel/xiaomi/onyx-devicetrees` → [`android_kernel_xiaomi_onyx-devicetrees`](https://github.com/Onyx-Odyssey/android_kernel_xiaomi_onyx-devicetrees) (`lineage-23.2`)
* 🔧 **Xiaomi Hardware** — `hardware/xiaomi` → [`android_hardware_xiaomi`](https://github.com/Onyx-Odyssey/android_hardware_xiaomi) (`lineage-23.2`)

## 🎮 Apps

* 🔊 **Lunaris Dolby** — `packages/apps/LunarisDolby` → [`android_packages_apps_LunarisDolby`](https://github.com/Onyx-Odyssey/android_packages_apps_LunarisDolby) (`16.0`)
* 🎮 **Game Bar** — `packages/apps/GameBar` → [`android_packages_apps_GameBar`](https://github.com/Onyx-Odyssey/android_packages_apps_GameBar) (`lineage-23.2`)
* 🚀 **Not Game Turbo** — `packages/apps/NotGameTurbo` → [`android_packages_apps_NotGameTurbo`](https://github.com/Onyx-Odyssey/android_packages_apps_NotGameTurbo) (`lineage-23.2`)

## Notes

* `repo sync` never fetches Git LFS, so the MiuiCamera APK lands as a 134-byte pointer — run `git lfs install` once, then `git -C vendor/xiaomi/onyx-leicacamera lfs pull`.
* If `repo sync` reports a duplicate path (`hardware/xiaomi` and the device/vendor trees are often already declared by the base ROM manifest), keep only one side.
