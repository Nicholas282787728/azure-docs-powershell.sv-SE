---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755920"
---
# Install-AzureRmServerManagementGatewayProfile

## Sammanfattning
Installerar en Server Management Gateway-profil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **install-AzureRmServerManagementGatewayProfile** installerar en Azure Server Management Gateway-profil på rätt plats.
Filen som installeras med den här cmdleten kallas profile.jspå.

## BESKRIVS

## MALLPARAMETRAR

### -InputFile
Anger namnet på den lokala filen som innehåller Gateway-profilen som ska installeras.

Filen som installeras av denna cmdlet bör tidigare ha sparats med Save-AzureRmServerManagementGatewayProfile cmdlet.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### FileInfo
Parametern ' InputFile ' godkänner värdet av typen ' FileInfo ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Reset-AzureRmServerManagementGatewayProfile](./Reset-AzureRmServerManagementGatewayProfile.md)

[Spara – AzureRmServerManagementGatewayProfile](./Save-AzureRmServerManagementGatewayProfile.md)


