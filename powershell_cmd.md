# ユーザー一覧
```
Get-ADObject -LDAPFilter "(objectClass=organizationalPerson)" -Propertie * | Export-Csv <出力先.csv> -Encoding Default
```

# OU一覧
```
Get-ADObject -LDAPFilter "(objectClass=organizationalUnit)" -Properties * | Export-Csv  <出力先.csv> -Encoding Default
Get-ADObject -Filter 'ObjectClass -eq "organizationalUnit"' -Properties * | Export-Csv <出力先.csv> -Encoding Default
```

# コンピューター情報取得（以下いずれかのコマンドで情報取得できる）
```
Get-ADComputer -Filter * -SearchBase "OU=xxx,OU=Clients,DC=ドメイン,DC=co,DC=jp" | fl
Get-ADComputer -Filter "Name -eq 'computerName'" | fl
Get-ADComputer -Filter "Name -like '*computerName*'" | fl
```
# GPO名を一覧表示する
```
Get-GPO -all | select DisplayName
```

# 特定GPOの情報を取得する
```
Get-GPOReport -Name <GPOの名前> Html -Path "<出力先>.html"
```



