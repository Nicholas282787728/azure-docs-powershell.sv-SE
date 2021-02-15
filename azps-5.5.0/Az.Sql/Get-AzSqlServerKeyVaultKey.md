---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235566"
---
# Get-AzSqlServerKeyVaultKey

## SYNOPSIS
Hämtar nyckelvalvnycklarna för en SQL-server.

## SYNTAX

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Den Get-AzSqlServerKeyVaultKey cmdleten hämtar information om tangenterna i nyckelvalvet på en SQL-server.
Du kan visa alla tangenter på en server eller visa en specifik nyckel genom att ange KeyId.

## EXEMPEL

### Exempel 1: Hämta alla tangenter i valvet
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Med det här kommandot får du alla tangenter i nyckelvalvet på en SQL-server.
ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Typ: AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 1122334455667788990011223344556677889900 CreationDate : 1/1/2017 12:00:00 AM Resource ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 0099887766554433221100998877665544332211 CreationDate : 1/1/2017 12:00:00 AM

### Exempel 2: Hämta en specifik nyckel för nyckel för nyckel för
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Det här kommandot får nyckeln för nyckelvalv med Id ' ' och lagrar den sedan https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 i den $MyServerKeyVaultKey variabeln.
Du kan granska egenskaperna för $MyServerKeyVaultKey för att få information om nyckelvalvet.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
The Azure Key Vault KeyId.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resursgruppen

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servernamn
Azure Sql Server-namnet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Dokumentation om SQL-databaser](https://docs.microsoft.com/azure/sql-database/)
