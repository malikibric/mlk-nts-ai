# mlk-nts-ai

Get-WinEvent -FilterHashtable @{LogName='Application'; ProviderName='Application Error'} -MaxEvents 2 | Format-List TimeCreated, Message

(Get-Item C:\Windows\System32\msvcp140.dll).VersionInfo.FileVersion
