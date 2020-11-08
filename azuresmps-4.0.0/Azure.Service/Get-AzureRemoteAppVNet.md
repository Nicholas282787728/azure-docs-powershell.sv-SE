---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099800"
---
# Get-AzureRemoteAppVNet

## Sammanfattning
Hämtar information om virtuella Azure RemoteApp-nätverk i Azure.

## FRÅGESYNTAXEN

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRemoteAppVNet** hämtar information om virtuella Azure RemoteApp-nätverk i Microsoft Azure.
Denna cmdlet returnerar ett objekt som innehåller information om ett angivet virtuellt nätverk.
Om inget virtuellt nätverk anges returnerar denna cmdlet information om alla virtuella nätverk i det aktuella abonnemanget.

## BESKRIVS

### Exempel 1: Hämta information om ett virtuellt nätverk
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Med det här kommandot får du information om det virtuella nätverket som heter ContosoVNet.

## MALLPARAMETRAR

### -IncludeSharedKey
Anger att den här cmdleten innehåller värdet för den delade lösningen i den information som hämtas om det virtuella nätverket.

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

### -VNetName
Anger namnet på det virtuella Azure RemoteApp-nätverket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


