## Enable archive mailbox for all mailboxes:
`Get-Mailbox | ForEach-Object {Enable-Mailbox -Identity $_.PrimarySmtpAddress -Archive}`

## Check if the in-place archive is enabled for all mailboxes:
`Get-Mailbox | Select-Object PrimarySmtpAddress,ArchiveStatus | ft -AutoSize`
