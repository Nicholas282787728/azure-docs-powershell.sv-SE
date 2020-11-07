---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922682"
---
# Remove-AzKeyVaultKey

## Sammanfattning
Tar bort en nycklar i ett nyckelord.

## FRÅGESYNTAXEN

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Remove-AzKeyVaultKey cmdlet tar bort en nycklar i ett nyckelord.
Om du av misstag tagit bort tangenten kan du återställa den med hjälp av Undo-AzKeyVaultKeyRemoval av en användare med speciella "Recover"-behörigheter.
Denna cmdlet har värdet High för egenskapen **ConfirmImpact** .

## BESKRIVS

### Exempel 1: ta bort en Key från ett nyckelord
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.

### Exempel 2: ta bort en nycklar utan användar bekräftelse
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

Det här kommandot tar bort den ITSoftware från nyckelordet som heter Contoso.
Kommandot anger *tvingande* och *Bekräfta* parametrar, och därför uppmanas du inte att bekräfta i cmdleten.

### Exempel 3: ta bort en borttagen Key från Key Vault permanent
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Det här kommandot tar bort tangenten med namnet ITSoftware från nyckelordet contoso permanent.
För att köra den här cmdleten krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren för det här nyckelvärdet.

### Exempel 4: ta bort tangenter med pipeline-operatorn
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

Det här kommandot får alla nycklar i nyckel valvet contoso och vidarebefordrar dem till cmdleten **WHERE-objekt** med hjälp av pipeline-operatorn.
Denna cmdlet skickar de nycklar som har värdet $False för det **aktiverade** attributet till den aktuella cmdleten.
Dessa nycklar tas bort med denna cmdlet.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Ta bort den tidigare borttagna knappen permanent.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den som ska tas bort.
Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för en nycklar baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Anger att denna cmdlet returnerar ett **Microsoft. Azure. commands. valv** .-objekt för paket.
Denna cmdlet genererar som standard inga utdata.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Anger namnet på det nyckelord som du vill ta bort.
Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Strängvärdet

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. DeletedKeyBundle
Denna cmdlet returnerar endast ett värde om du anger parametern *Passthru* .

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzKeyVaultKey](./Add-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)

[Ångra-AzKeyVaultKeyRemoval](./Undo-AzKeyVaultKeyRemoval.md)

