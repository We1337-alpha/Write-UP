Boot and Recovery Shortcuts

- **Supr**: Access BIOS settings.
- **F8**: Enter Recovery mode.
- Pressing **Shift** after the Windows banner can bypass autologon.

BAD USB Devices

Devices like **Rubber Ducky** and **Teensyduino** serve as platforms for creating **bad USB** devices, capable of executing predefined payloads when connected to a target computer.

Volume Shadow Copy

Administrator privileges allow for the creation of copies of sensitive files, including the **SAM** file, through PowerShell.

```bash
vssadmin list shadows
```


