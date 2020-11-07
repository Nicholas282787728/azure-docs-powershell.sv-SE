---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758118"
---
# Test-AzureRmContainerRegistryNameAvailability

## Sammanfattning
Kontrollerar tillgänglighet för ett namn på en behållare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **test-AzureRmContainerRegistryNameAvailability** kontrollerar om ett namn på en behållare är giltig och tillgänglig för användning.

## BESKRIVS

### Exempel 1: kontrol lera tillgänglighet för ett namn på en behållares register
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

Det här kommandot kontrollerar tillgängligheten för behållar registrerings namnet `SomeRegistryName` .

## MALLPARAMETRAR

### -Namn
Namn på behållarens register.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

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

### Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmContainerRegistry](./New-AzureRmContainerRegistry.md)

