---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755370"
---
# Remove-AzureRmServerManagementNode

## Sammanfattning
Tar bort en nod för Server hantering.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ByName
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmServerManagementNode** tar bort en Azure Server Management-nod.

## BESKRIVS

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Nod
Anger den nod som denna cmdlet ska tas bort för.

Den här parametern kan användas i stället för parametrarna *ResourceGroupName* och *nodnamn* .

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nodnamn
Anger namnet på den nod som denna cmdlet ska tas bort för.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som noden tillhör.

```yaml
Type: String
Parameter Sets: ByName
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

### Nodnamnet
Parametern ' Node ' godkänner värdet för typen nod från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmServerManagementNode](./Get-AzureRmServerManagementNode.md)

[New-AzureRmServerManagementNode](./New-AzureRmServerManagementNode.md)


