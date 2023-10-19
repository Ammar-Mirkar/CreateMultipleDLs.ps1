# CreateMultipleDLs.ps1
#CreateMultipleDLs.ps1
#This script can help create multiple DL's in onprem network
Import-Csv C:\DLs_full.csv | ForEach { New-DistributionGroup -Name $_.Name -Alias $_.Alias -SamAccountName $_.SamAccountName -CopyOwnerToMember -ManagedBy "Test, Mail"-MemberDepartRestriction Closed -MemberJoinRestriction Closed -OrganizationalUnit "conotoso/Address Book/Distribution Lists" -Type "Distribution"}
