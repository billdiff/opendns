Umbrella Roaming Client Installation Instructions
--------------------------------------------------------------------------------------

- Silent Provisioning via GPO or command-line -
This package can be provisioned via GPO or command-line silently (Admin rights required) with the following command:

msiexec /i Setup.msi /qn ORG_ID=3385302 ORG_FINGERPRINT=7c8343387c17902b2713096686993644 USER_ID=11244502


- Provisioning without a client User Interface
The Enterprise Roaming Client can be installed without a client-side user interface and remain fully functional:

msiexec /i Setup.msi /qn ORG_ID=3385302 ORG_FINGERPRINT=7c8343387c17902b2713096686993644 USER_ID=11244502 HIDE_UI=1

- Provisioning without a client User Interface AND without displaying Umbrella Roaming Client under Add/Remove Programs
The Enterprise Roaming Client can also be hidden from the Add/Remove Programs dialog with the HIDE_ARP argument:

msiexec /i Setup.msi /qn ORG_ID=3385302 ORG_FINGERPRINT=7c8343387c17902b2713096686993644 USER_ID=11244502 HIDE_UI=1 HIDE_ARP=1

To uninstall the ERC in this state, use the following command from an Administrative Command Prompt:

wmic Product where name='Umbrella Roaming Client' call uninstall

- Installation via GUI installer -
This package can also be provisioned individually via the standard Windows installer.

Double-click the msi file, and when prompted, enter the information below.

Organization Id: 3385302
Fingerprint: 7c8343387c17902b2713096686993644
User Id: 11244502

This information will be auto-filled if the OrgInfo.json file is present in the installer source directory.
