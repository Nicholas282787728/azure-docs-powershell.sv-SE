---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093356"
---
# Get-AzureRemoteAppVmStaleAdObject

## Sammanfattning
Hämtar objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.

## FRÅGESYNTAXEN

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRemoteAppVmStaleAdObject** hämtar objekt i Azure Active Directory som är associerade med virtuella Azure RemoteApp-datorer som inte längre finns.
Denna cmdlet visar namnet på varje objekt som det får.

## BESKRIVS

### Exempel 1: Hämta gamla objekt för en samling
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Det här andra kommandot får de inaktuella objekten för samlingen contoso.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Strängvärdet

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Clear-AzureRemoteAppVmStaleAdObject](./Clear-AzureRemoteAppVmStaleAdObject.md)


