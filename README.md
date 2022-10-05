# file-copy

Tutorial on how to copy/backup files from Windows to a remote server using `rsync`.

1. Activate WSL (Windows Subsystem for Linux) for Windows by typing `wsl --install` into command prompt. Restarting your computer after WSL has install completes.
2. Using Windows Terminal, open an Ubuntu (WSL) Terminal.
3. In Ubuntu terminal, Windows files can be accessed in `/mnt/`. For example `C:\\` is in `/mnt/c/`.
4. run: `rsync -a --progress 10_Gb twsly@colossus.it.mtu.edu:/tmp` to copy a single file, replacing `twsly` with your username
5. 

### Generating test files
- You can easily generate a file of arbitarary size in linux using `truncate -s 5M 5Mb_file.txt` (`5M` means that the file will be 5MB in size).
- To generate multiple files with the same name you cand do `truncate -s 1M my_file{1..5}`. This will generate 5 files of 1MB size that are sequentially named: `my_file1`, `my_file2`, ..., `my_file5`.