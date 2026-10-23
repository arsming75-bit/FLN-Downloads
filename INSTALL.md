# Install FLN College Football

## Windows warnings and verification

FLN's current installer is **not digitally signed**. Windows cannot show a verified FLN publisher identity. A warning is not proof that a file is malicious, and an unsigned notice is not proof that it is safe.

1. Download only from the release assets at **https://github.com/arsming75-bit/FLN-Downloads/releases**. Check the owner and repository name carefully. Do not use an installer from a direct message or a reupload.
2. Read that release's notes and compare the installer's SHA-256 checksum with the published `SHA256SUMS.txt`.
3. To calculate a checksum, open PowerShell and run the command below, replacing the example path with the exact downloaded filename. This reads the file; it does not run the installer.

```powershell
Get-FileHash -LiteralPath "$env:USERPROFILE\Downloads\FLN-Setup-VERSION-x64.exe" -Algorithm SHA256
```

The entire hash must match (letter case does not matter). A matching hash confirms the file matches the published download; it does not replace a digital signature or guarantee safety. If it differs, do not run the file. Download it again from the official release and report a continued mismatch.

4. If the file matches, you trust the official source, and Windows displays **Windows protected your PC**, select **More info**, check the application filename, and choose **Run anyway** if that option is available. An unsigned package may show **Unknown publisher**; do not expect a verified FLN name.
5. If **Run anyway** is unavailable, or Windows reports malware, Smart App Control, or an administrator policy block, stop and report the exact message. Do not disable Defender, SmartScreen, Smart App Control, or add antivirus exclusions to install FLN. On a managed computer, contact its administrator.

Microsoft explains these distinctions in its [SmartScreen guidance](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation).

## First installation

1. Download the installer and the compatible FLN Assets pack listed in the release notes.
2. Extract the artwork ZIP using **Extract All**. Keep the resulting **FLN Assets** folder in a permanent location outside the application installation folder. Do not select the ZIP itself.
3. Run the verified installer and follow its prompts. Keep **Create a desktop shortcut** and **Open FLN** selected if you want those options.
4. When FLN asks for artwork, select the extracted **FLN Assets** folder. Initial verification can take a little time.
5. In the launcher, select **Open FLN** to open the website in your default browser. Keep the launcher running while using FLN.
6. On the website, select **Open Save** and choose your College Football Dynasty save. FLN reads the game save without modifying it.
7. Register the dynasty when prompted, then check the displayed school, season, and week.

Python and Node are included in the installer. You do not need to install them separately. The application runs locally; installing FLN does not set up remote access or Tailscale sharing.

## Artwork and portraits

Use **Change Artwork** in the launcher to select the standard FLN Assets folder. **Verify Artwork** checks the standard pack when needed.

Updated or custom portraits can be selected separately under **Players & Recruits** and **Coaches**. Compatible packs must preserve the expected portrait filenames/mapping. Use **Refresh** after the selected pack changes, or **Use Standard** to return to standard portraits. Refresh the website after applying changes. Missing custom portraits fall back to standard artwork where available.

## If nothing opens

- Look for the FLN launcher and select **Open FLN**.
- Confirm the artwork ZIP has been extracted and the selected folder still exists.
- If artwork verification fails, extract a fresh compatible pack and select it again.
- If save import reports insufficient available memory, close other large applications and retry.
- Report the FLN version, Windows version, and exact error in a public issue. Remove personal details from screenshots and do not attach saves, API keys, or entire data folders.

Use **Exit FLN** in the launcher to end the app session. Closing only the browser tab does not stop FLN.
