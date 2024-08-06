# forensic

## kansa
1. Unblock file
    1. ls -r *.ps1 | Unblock-File
    2. Set-ExecutionPolicy AllSigned | RemoteSigned | Unrestricted
2. Running module standalone (as administrator)
    1. Netstat
    .\Get-Netstat.ps1 | ConvertTo-CSV -Delimiter "`t" -NoTypeInformation | % { $_ -replace "`"" } | Set-Content netstat.tsv
    2. Usb
     .\Modules\Registry\Get-USBForensics.ps1 | ConvertTo-CSV -Delimiter "`t" -NoTypeInformation | % { $_ -replace "`"" } | Set-Content usb.tsv
