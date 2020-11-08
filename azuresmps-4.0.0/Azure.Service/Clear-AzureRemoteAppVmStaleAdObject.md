---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093429"
---
# Clear-AzureRemoteAppVmStaleAdObject

## Sammanfattning
Tar bort objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.

## FRÅGESYNTAXEN

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Clear-AzureRemoteAppVmStaleAdObject** tar bort objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.
Du måste använda autentiseringsuppgifter som har behörighet att ta bort Azure Active Directory-objekt.
Om du anger parametern *verbose* visas namnet på varje objekt som tas bort.

## BESKRIVS

### Exempel 1: ta bort inaktuella objekt för en samling
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

I det första kommandot uppmanas du att ange ett användar namn och lösen ord med hjälp av **Hämta-Credential**.
Kommandot lagrar resultaten i variabeln $AdminCredentials.

Det andra kommandot rensar de inaktuella objekten för samlingen contoso.
Kommandot använder autentiseringsuppgifterna som lagras i $AdminCredentials variabel.
Dessa autentiseringsuppgifter måste ha rätt behörighet för att kommandot ska fungera.

## MALLPARAMETRAR

### -Samlings namn
Anger namnet på Azure RemoteApp-samlingen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Autentiseringsuppgift
Anger en autentiseringsuppgift som har behörighet att utföra den här åtgärden.
Om du vill hämta ett **PSCredential** -objekt använder du cmdleten **Get-Credential** .
Om du inte anger den här parametern används den aktuella användarens autentiseringsuppgifter.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


