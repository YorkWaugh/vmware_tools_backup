# VMware Tools ISO Backup

## Repository Purpose

This repository serves as a backup archive for **all** VMware Tools Guest Operating System ISOs.

VMware Workstation 17.5.2 (build 23775571) and VMware Fusion 13.5.2 (build 23775688) were the last releases known to bundle a complete collection of these ISOs. Newer versions of VMware products, along with the official Broadcom download repositories, appear to **only provide active updates for the `windows` (64-bit) ISO**.

The purpose of this archive is to preserve the legacy and "frozen" versions for all other operating systems (e.g., `darwin`, `linux`, `solaris`, `winPreVista`) that are no longer easily accessible.

## Version Information

The versions archived here correspond to the bundle found in Workstation 17.5.2 and Fusion 13.5.2, cross-referenced with the Broadcom support portal and official package repository. With the exception of `windows.iso` (which is still actively updated), these are believed to be the final "frozen" releases for their respective legacy operating systems.

The `isoimages_manifest.txt` file (from a Workstation 25H2 release) is included in this repository to show which Guest OS settings map to which ISO filename.

| ISO Filename (Archived) | Last Known Version |
| :--- | :--- |
| [`darwin.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/darwin.iso) | 12.1.1-22484250 |
| [`darwinPre15.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/darwinPre15.iso) | 10.0.12-14792880 |
| [`freebsd.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/freebsd.iso) | 10.1.5-5055683 |
| [`linux.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/linux.iso) | 10.3.26-22085142 |
| [`linuxPreGlibc25.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/linuxPreGlibc25.iso) | 10.0.12-14792880 |
| [`netware.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/netware.iso) | 8.1.0-1463223 |
| [`solaris.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/solaris.iso) | 10.3.23-17030940 |
| [`windows.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/windows.iso) | 13.0.5-24915695 |
| [`windows-x86.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/windows-x86.iso) | 12.4.9-24964244 |
| [`winPre2k.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/winPre2k.iso) | 7.7.0-1463223 |
| [`winPreVista.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/winPreVista.iso) | 10.0.12-14792880 |
| [`winVista.iso`](https://github.com/YorkWaugh/vmware_tools_backup/releases/download/Archives/winVista.iso) | 11.0.6-15940789 |

---

## Notes

### Language Support

Starting from VMware Tools 13.0.0, language support is limited to English, French, Japanese, and Spanish.

### Linux Guests

For most modern Linux distributions, it is highly recommended to use **Open VM Tools**. These are open-source and are typically available directly from the distribution's official package repositories (e.g., via `apt`, `yum`, `zypper`).

* **Open VM Tools GitHub:** [https://github.com/vmware/open-vm-tools](https://github.com/vmware/open-vm-tools)
* **Broadcom Installation Guide:** [https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/11-1-0/vmware-tools-administration-11-1-0/installing-vmware-tools/install-open-vm-tools.html](https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/11-1-0/vmware-tools-administration-11-1-0/installing-vmware-tools/install-open-vm-tools.html)

The `linux.iso` package in this archive is a legacy release.

### macOS (darwin.iso) Versioning

VMware Tools 12.1.0 was the last regular release for macOS. An updated darwin.iso (version 12.1.1) was subsequently released to address a reported security vulnerability, which is the version archived here.

* **Sources:** [https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/12-3-0/release-notes/vmware-tools-1235-release-notes.html](https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/12-3-0/release-notes/vmware-tools-1235-release-notes.html)

### Windows Guest OS Compatibility

* **Windows (Arm):** Starting with VMware Tools 12.3.0, support for Windows on Arm was introduced and is being actively updated. **Note: This package is not archived in this repository.**
* **Windows (64-bit):** From VMware Tools 12.5.0 onwards, only 64-bit versions of Windows OS are supported.
* **Windows (32-bit):** The last regular release for 32-bit Windows was 12.4.5. However, due to several CVEs, VMware provided a final update to version 12.4.9, which is the version archived here.
  * **Sources:** [https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/12-5-0/release-notes/vmware-tools-1254-release-notes.html](https://techdocs.broadcom.com/us/en/vmware-cis/vsphere/tools/12-5-0/release-notes/vmware-tools-1254-release-notes.html)
* **Windows 7:**
  * Version 11.1.1 was the last version to support installation on Windows 7 SP1 *without* Microsoft update KB4474419 (SHA-2 code signing support).
  * From version 11.1.5 onwards, installation requires Windows 7 SP1 or Windows Server 2008 R2 SP1 and later.
* **Windows Vista:**
  * **SP2:** The last version to support Windows Vista SP2 is 11.0.6 (this version is archived as `winVista.iso`).
    * **Package Location (SP2):** [https://packages-prod.broadcom.com/tools/frozen/windows/WindowsToolsVista/SP2/](https://packages-prod.broadcom.com/tools/frozen/windows/WindowsToolsVista/SP2/)
  * **SP1:** The last version to support Windows Vista SP1 appears to be 10.2.5.
    * **Package Location (SP1):** [https://packages-prod.broadcom.com/tools/frozen/windows/WindowsToolsVista/SP1/](https://packages-prod.broadcom.com/tools/frozen/windows/WindowsToolsVista/SP1/)
  * **Note on Issues:** For a detailed analysis of issues and compatibility with Windows Vista, see this Gist reference: [https://gist.github.com/akemin-dayo/9f687c91e9e23bb724ac97b4a876a44f](https://gist.github.com/akemin-dayo/9f687c91e9e23bb724ac97b4a876a44f)
* **Windows XP:** The last version to support Windows XP is 10.0.12 (archived here as `winPreVista.iso`).
  * **Note on builds:** The version archived in this repository (from Workstation 17.5.2) is build **10.0.12-14792880** (packaged in 2019). The Broadcom [`frozen`](https://packages-prod.broadcom.com/tools/frozen/) repository holds an older build, **10.0.12-444849614792880** (packaged in 2016).

## Sources & References

* **Version Baseline:** VMware-workstation-full-17.5.2-23775571.exe, VMware-Fusion-13.5.2-23775688_universal.dmg
* **Broadcom Support Download Portal:** [https://support.broadcom.com/group/ecx/productdownloads?subfamily=VMware Tools&freeDownloads=true](https://support.broadcom.com/group/ecx/productdownloads?subfamily=VMware%20Tools&freeDownloads=true)
* **Official Package Repository:** [https://packages-prod.broadcom.com/tools/](https://packages-prod.broadcom.com/tools/)
* **Guest OS Mapping:** [`isoimages_manifest.txt`](isoimages_manifest.txt) (from Workstation 25H2 (25.0.0.24995812), included in this repository)
* **Overview of VMware Tools (KB Article):** [https://knowledge.broadcom.com/external/article/315382/overview-of-vmware-tools.html](https://knowledge.broadcom.com/external/article/315382/overview-of-vmware-tools.html)
* **Internet Archive (VMware):** [https://archive.org/search?query=creator:"VMWare"](https://archive.org/search?query=creator%3A%22VMWare%22)
