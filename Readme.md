AGPM Injector
=============

This is a AGPM (Apple Graphics Power Management) Injector kext generator.

<!-- START shields -->
<div>
    <!-- downloads --><a href="https://github.com/RobyRew/AGPMInjector/releases">
        <img src="https://img.shields.io/github/downloads/RobyRew/AGPMInjector/total" alt="downloads"/>
    </a>
    <!-- version --><a href="https://github.com/RobyRew/AGPMInjector/releases/latest">
        <img src="https://img.shields.io/github/release/RobyRew/AGPMInjector.svg" alt="latest version"/>
    </a>
     <!-- platform --><a href="https://github.com/RobyRew/AGPMInjector">
        <img src="https://img.shields.io/badge/platform-macOS-lightgrey.svg" alt="platform"/>
    </a>
</div>
</br>
<!-- END shields -->

[![Build Status](/Docs/AGPInjectorPreview.png)](https://github.com/RobyRew/AGPMInjector)

><strong>Note:</strong> This is an example,there are much more options for AGPM Kext generation.



#### Installation
- Select the SMBIOS you are currently using.
- Check the box for the dGPU Manufacture you currently have installed.
- Select the dGPU Model from the dropdown menu.
- Click the Generate button to generate the AGPMInjector.kext. This kext will be saved in the your *Downloads* directory.

#### Features
- Nvidia from **GT 710** to **Titan XP**
- AMD from **Duo Pro** to **W 9100**
- Notifies user when there is an update on Github (as of App version 2.3.4).
- Fixes GPU Power Management settings for *desktop* GPUs that are supported (SMBIOS Systems that are in the dropdown menu).
- Automatically parses */System/Library/Extensions/AppleGraphicsPowerManagement.kext* to generate the most up to date injector kext.
- Automatically generates the correct AGPM setting for GPUs that are supported (AMD/Nvidia GPUs that are in the dropdown menu).

#### Known Issues
- Generating the kext on to the user's Desktop when a user has Desktop and Documents enabled for iCloud does not generate the required Info.plist inside the kext file itself. This is because Desktop and Documents enbabled for iCloud turns those directories into containers for iCloud services. This would require my app to enable iCloud APIs which in turn requires me to submit my app to the App Store, which I will not do. So the current generation of the kext to the currently logged in user's Downloads directory is the best solution.

#### Important Information
- X86PlatformPlugin must be loaded in order for this injector to work.

#### Credits
- [toleda](https://github.com/toleda) and others for layout.
- [vidda#7908](https://discord.gg/fSSmfq) for the help with Update Notification feature.
- [Estel#4658](https://discord.gg/fSSmfq) for the help with Encodable CodingKeys.
- [@junzhli](https://github.com/junzhli/AGPMInjector) for version bump and AMD 6000 Support.
