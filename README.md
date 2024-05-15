# Intro
This repo is for testing whether symlinks can be created when Developer Mode is enabled on Windows 10 Pro

## Testing
Test that you can create symlinks without admin privileges as per the announcement for [Symlinks in Windows 10](https://blogs.windows.com/windowsdeveloper/2016/12/02/symlinks-windows-10/):
```bash
git clone https://github.com/ayewo/test-symlinks-on-windows10.git

cd test-symlinks-on-windows10\

tree /f

type animals\dog.txt

mklink pet.txt animals\dog.txt

dir

type pet.txt

notepad pet.txt
```

## Further Reading
This excellent wiki article by the [Git for Windows](gitforwindows.org/) project on [Symbolic Links](https://github.com/git-for-windows/git/wiki/Symbolic-Links) contains:
* a [concise history](https://github.com/git-for-windows/git/wiki/Symbolic-Links#background) of which editions of Windows supports symbolic links;
* [the (two) types of symbolic links](https://github.com/git-for-windows/git/wiki/Symbolic-Links#creating-symbolic-links) that can be created (directory and file symbolic links);
* and the (four) ways of granting a user the ability to create symbolic links i.e. via:
  * `gpedit.msc` — _Group Policy Editor_ is used for Windows editions that are centrally administered as part of a domain; 
  * `secpol.msc` — _Local Security Policy_ is used for Windows editions that are not centrally adminsistered;
  * [`polseditx64.exe`](https://www.southsoftware.com/polsedit.html) — _User Policies Editor_ is used for Windows Home editions (that do not have `secpol.msc`);
  * or by enabling [Developer Mode](https://learn.microsoft.com/en-us/windows/apps/get-started/enable-your-device-for-development) — for Windows 10 version 1703 (Creators Update) and later editions.

It also links to a 2016 blog post: *[Symlinks in Windows 10!](https://blogs.windows.com/windowsdeveloper/2016/12/02/symlinks-windows-10/)* explaining what motivated the addition of proper symlinks to Windows.
