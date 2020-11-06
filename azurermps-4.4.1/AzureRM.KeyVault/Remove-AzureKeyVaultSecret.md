---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583280"
---
# Remove-AzureKeyVaultSecret

## Sammanfattning
Tar bort en hemlighet i ett nyckel valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Remove-AzureKeyVaultSecret-cmdleten tar bort en hemlighet i ett nyckel valv.
Om hemligheten togs bort av misstag kan hemligheten återställas med Undo-AzureKeyVaultSecretRemoval av en användare med särskilda "återställnings behörighet".
Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .

## BESKRIVS

### Exempel 1: ta bort en hemlighet från ett nyckel valv
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.

### Exempel 2: ta bort en hemlighet från ett nyckel valv utan bekräftelse
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

Det här kommandot tar bort hemligheten med namnet FinanceSecret från nyckel valvet contoso.
Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.

### Exempel 3: rensa bort hemliga hemlighet från nyckel valvet permanent
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

Det här kommandot förflyttar den hemliga hemligheten med namnet FinanceSecret från nyckel valvet contoso permanent.
För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.

## MALLPARAMETRAR

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

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

### -InRemovedState
Om den visas tar du bort den hemliga hemligheten permanent.

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

### -Namn
Anger namnet på en hemlighet.
Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) på en hemlighet baserad på namnet som den här parametern anger, namnet på nyckel valvet och din nuvarande miljö.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Anger att den här cmdleten returnerar ett **Microsoft. Azure.-kommandon. nyckel valv.** rebärare-objekt.
Denna cmdlet genererar som standard inga utdata.

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

### -VaultName
Anger namnet på det nyckel valv som hemligheten tillhör.
Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.

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
Cmdleten körs inte. Visar vad som händer om cmdleten körs.
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

### Strängvärdet

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. DeletedSecret
Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureKeyVaultSecret](./Get-AzureKeyVaultSecret.md)

[Set-AzureKeyVaultSecret](./Set-AzureKeyVaultSecret.md)

[Ångra-AzureKeyVaultSecretRemoval](./Undo-AzureKeyVaultSecretRemoval.md)

