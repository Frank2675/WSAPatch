# WSA patch for Windows 10

This is a patch for WSA to enable WSA (Windows Subsystem for Android) to run on Windows 10.

Steps:

1. Get WSA appx zip from https://github.com/LSPosed/MagiskOnWSALocal (You need to "build" this yourself with your local WSL2).
2. Get "icu.dll" from Windows 11 22H2. Note that you MUST use icu.dll from Windows 11. The icu.dll from Windows 10 will NOT work.
3. Build WsaPatch.dll with source code in this repo.
4. Patch icu.dll: add WsaPatch.dll as an import DLL as icu.dll.
5. Copy patched icu.dll and WsaPatch.dll to WsaClient dir.
6. Delete all element about "customInstall" in AppxManifest.xml.
7. Run "Run.bat" to register your WSA appx.
8. You should be able to run WSA now.
