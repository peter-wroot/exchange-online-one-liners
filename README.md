## Enable archive mailbox for all mailboxes:
`Get-Mailbox | ForEach-Object {Enable-Mailbox -Identity $_.PrimarySmtpAddress -Archive}`

## Check if the in-place archive is enabled for all mailboxes:
`Get-Mailbox | Select-Object PrimarySmtpAddress,ArchiveStatus | ft -AutoSize`

## Get a list of ActiveSync (Mobile) devices and when they last talked to Exchange:
`get-mailbox | ForEach-Object {Get-MobileDeviceStatistics -Mailbox $_.alias} | Select-Object Identity,DeviceModel,LastSuccessSync | ft -AutoSize`
