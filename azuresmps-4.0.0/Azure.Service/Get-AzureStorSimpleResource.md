---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093280"
---
# Get-AzureStorSimpleResource

## Sammanfattning
Hämtar alla resurser som du har skapat.

## FRÅGESYNTAXEN

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleResource** hämtar alla resurser som du har skapat med Azure Portal.
Denna cmdlet hämtar information som du kan använda för att ansluta till resurserna.

## BESKRIVS

### Exempel 1: Hämta alla resurser
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

Det här kommandot får alla resurser du har skapat.
I det här exemplet finns det tre resurser.

### Exempel 2: skaffa en resurs genom att använda dess namn
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

Med det här kommandot får du resursen namnet Contoso63-Tsqa.

### Exempel 3: försök att hämta en resurs som inte finns
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

Det här kommandot försöker hämta resursen med namnet Contoso64-Tsqa.
Det finns ingen resurs med det här namnet.
I det här exemplet returneras ingen resurs.

## MALLPARAMETRAR

### -Profil
Anger en Azure-profil.

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

### -ResourceName
Anger namnet på den resurs som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### IEnumerable \<ResourceCredentials\> , ResourceCredentials
Denna cmdlet returnerar **ResourceCredentials** -objekt som innehåller följande egenskaper: 

- **ResourceName**
- **ResouceId**
- **ResourceState**

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[Select-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


