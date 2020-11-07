---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755872"
---
# Get-AzureRmIotHub

## Sammanfattning
Hämtar information om IotHubs i ett abonnemang.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ListIotHubsByResourceGroup (standard)
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetIotHubByName
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Hämtar information om IotHubs i ett abonnemang.
Du kan visa alla IotHub-instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst IotHub-namn.

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzureRmIotHub
```

Hämtar alla IotHubs i prenumerationen.

### Exempel 2
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

Hämtar alla IotHubs i prenumerationen som tillhör resourcegroup med namnet "myresourcegroup".

### Exempel 3
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

Hämtar information om IotHub med namnet "myiothub".

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namn på IotHub

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Namn på ResourceGroup

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub
System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. Management. IotHub. Models. PSIotHub, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null\]\]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

