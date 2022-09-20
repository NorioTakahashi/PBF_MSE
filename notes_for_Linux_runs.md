## Notes for PBF MSE runs on Linux

### by norio


- R for Linux has "system()" function only (no "shell() function).

- for windows

**error!!**

command_mv = paste("for %%I in (test.txt) do copy %%I ", "D:\\test2", sep ="")

**OK!!**

command_mv = paste("for %I in (test.txt) do copy %I ", "D:\\test2", sep ="")

The syntax as follow though.... (NOT %, BUT %%):

    FOR (オプション) %%変数 IN (セット) DO コマンド

shell(cmd = command_mv)

- for Linux

system("for file in test2.sh test3.sh; do cp $file testdir/; done")

- shebang "#!/bin/bash" is NOT necessary at the first line in a shell script file.

- Linux distinguishes ".PAR" from ".par", so need consistent file names/extensions for read/write.

- Need to give permission to (e.g.)~/PBF_test/PBF_MSE/SS_model/ss by "chmod +x ss"
