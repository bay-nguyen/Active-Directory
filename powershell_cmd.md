# ユーザー一覧
Get-ADObject -LDAPFilter "(objectClass=organizationalPerson)" -Propertie * | Export-Csv output.csv -Encoding Default

# OU一覧
Get-ADObject -LDAPFilter "(objectClass=organizationalUnit)" -Properties * | Export-Csv output-ou.csv -Encoding Default
Get-ADObject -Filter 'ObjectClass -eq "organizationalUnit"' -Properties * | Export-Csv output-ou.csv -Encoding Default

