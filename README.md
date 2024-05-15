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

