---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758257"
---
# Set-AzureRmSqlServerTransparentDataEncryptionProtector

## Sammanfattning
Ställer in skydd mot transparent data kryptering (TDE) för en SQL-Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Set-AzureRmSqlServerTransparentDataEncryptionProtector-cmdleten ställer in TDE-skyddskomponenten för en SQL-Server.
Om du ändrar TDE skydds typ roteras skydds komponenten.

## BESKRIVS

### --------------------------Exempel 1: Ange skydds typen transparent data kryptering (TDE) till ServiceManaged--------------------------
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

Det här kommandot uppdaterar en servers TDE skydds typ till tjänst hanterad.

ResourceGroupName ServerName ServerKeyVaultKeyName
----------------- ----------                   ---- ---------------------
ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged

### --------------------------Exempel 2: Ange den transparenta typen av data krypterings skydd för Azure Key Vault--------------------------
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

Det här kommandot uppdaterar en server för användning av Server Key valv-tangenten med ID ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' som TDE-skydd.

ResourceGroupName ServerName ServerKeyVaultKeyName
----------------- ----------                   ---- ---------------------
ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901

## MALLPARAMETRAR

### -Force
Hoppa över bekräftelse meddelande för att utföra åtgärden

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
KeyId för Azure Key Vault.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen

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

### -ServerName
Namnet på Azure SQL-servern.

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

### – Skriv
TDE skydds typ för Azure SQL Database.

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
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

### Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. EncryptionProtectorType
System. String

## VÄRDEN

### System. Object

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Dokumentation för SQL-databaser](https://docs.microsoft.com/azure/sql-database/)
