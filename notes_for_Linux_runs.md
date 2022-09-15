## Notes for PBF MSE runs on Linux

### by norio


R for Linux has "system()" function only (no "shell() function).


*error!!*
command_mv = paste("for %%I in (test.txt) do copy %%I ", "D:\\test2", sep ="")

*OK!!*
command_mv = paste("for %I in (test.txt) do copy %I ", "D:\\test2", sep ="")

The syntax as follow though.... (NOT %, BUT %%):
    FOR (オプション) %%変数 IN (セット) DO コマンド

shell(cmd = command_mv)
