---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: d54314686edafba9e72872411c678905adc55f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758047"
---
# Get-AzureRmMediaService

## Sammanfattning
Hämtar information om en medie tjänst.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ResourceGroupParameterSet
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmMediaService** hämtar information om en medie tjänst.

## BESKRIVS

### Exempel 1: Hämta alla medie tjänster i en resurs grupp
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

Det här kommandot får egenskaper för alla medie tjänster i resurs gruppen som heter ResourceGroup001.

### Exempel 2: Hämta egenskaper för medie tjänster
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

Det här kommandot får egenskaperna för medie tjänsten som heter MediaService1 som tillhör resurs gruppen med namnet ResourceGroup002.

## MALLPARAMETRAR

### -AccountName
Anger namnet på den medie tjänst som cmdleten får.

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
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

### Microsoft. Azure. commands. Media. Models. PSMediaService

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)

[Set-AzureRmMediaService](./Set-AzureRmMediaService.md)


