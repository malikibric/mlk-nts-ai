# mlk-nts-ai

Get-WinEvent -FilterHashtable @{LogName='Application'; ProviderName='Application Error'} -MaxEvents 2 | Format-List TimeCreated, Message
