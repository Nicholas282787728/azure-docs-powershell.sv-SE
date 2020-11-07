---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758045"
---
# Get-AzureRmMediaServiceKeys

## Sammanfattning
Hämtar viktig information för åtkomst till den REST-slutpunkt som är associerad med medie tjänsten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmMediaServiceKeys** hämtar viktig information för att få åtkomst till den ompresentations status överföring (rest) som är associerad med Azure Media-tjänsten.

## BESKRIVS

### Exempel 1: Hämta viktig information för att komma åt medie tjänsten
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

Det här kommandot får viktig information för åtkomst till medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup001.

## MALLPARAMETRAR

### -AccountName
Anger namnet på den medie tjänst som denna cmdlet hämtar medie tjänstens nycklar från.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller medie tjänsten.

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

### Microsoft. Azure. commands. Media. Models. PSServiceKeys

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Set-AzureRmMediaServiceKey](./Set-AzureRmMediaServiceKey.md)


