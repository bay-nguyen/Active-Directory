## ユーザー一覧
```
Get-ADObject -LDAPFilter "(objectClass=organizationalPerson)" -Propertie * | Export-Csv <出力先.csv> -Encoding Default
```

## OU一覧
```
Get-ADObject -LDAPFilter "(objectClass=organizationalUnit)" -Properties * | Export-Csv  <出力先.csv> -Encoding Default
```

## コンピューター情報
```
Get-ADComputer -Filter "Name -eq 'computerName'" | fl
```
## GPO名一覧
```
Get-GPO -all | select DisplayName
```

## 特定GPOの情報
```
Get-GPOReport -Name <GPOの名前> Html -Path "<出力先>.html"
```

## サイト一覧
```
Get-ADReplicationSite -Filter *
```

## サイトリンク一覧
```
Get-ADReplicationSiteLink -Filter *
```
## サブネット
```
Get-ADReplicationSubnet -Filter *
```




