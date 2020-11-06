---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582171"
---
# Get-AzureRmSqlServer

## Sammanfattning
Returnerar information om SQL-databas servrar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmSqlServer** returnerar information om en eller flera Azure SQL Database-servrar.
Ange namnet på en server för att visa information för endast den servern.

## BESKRIVS

### Exempel 1: Hämta alla instanser av SQL Server kopplade till en resurs grupp
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

Med det här kommandot får du information om alla de Azure SQL-databaser som tilldelats resurs gruppen ResourceGroup01.

### Exempel 2: få information om en Azure SQL Database-Server
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

Det här kommandot får information om Azure SQL-databasfilen med namnet Server01.

### Exempel 3: Hämta alla instanser av SQL Server i prenumerationen
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

Med det här kommandot får du information om alla Azure SQL-databas servrar i det aktuella abonnemanget.

## MALLPARAMETRAR

### -ResourceGroupName
Anger namnet på den resurs grupp som servrar är tilldelade till.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Anger namnet på den server som cmdleten får.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmSqlServer](./New-AzureRmSqlServer.md)

[Remove-AzureRmSqlServer](./Remove-AzureRmSqlServer.md)

[Set-AzureRmSqlServer](./Set-AzureRmSqlServer.md)

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)


