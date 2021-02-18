## Enable archive mailbox for all mailboxes:
` Get-Mailbox | ForEach-Object {Enable-Mailbox -Identity $_.MicrosoftOnlineServicesID -Archive}`
