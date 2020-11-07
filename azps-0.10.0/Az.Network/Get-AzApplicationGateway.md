---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGateway.md
ms.openlocfilehash: 61547a4ee5f60fccc371ca7b2c426ca1a4bbb005
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922353"
---
# Get-AzApplicationGateway

## Sammanfattning
Hämtar en Programgateway.

## FRÅGESYNTAXEN

```
Get-AzApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzApplicationGateway** hämtar en programport.

## BESKRIVS

### Exempel 1: skaffa en angiven Programgateway
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

Det här kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabeln.

### Exempel 2: Hämta en lista med program gateways i en resurs grupp
```
PS C:\>$AppGwList = Get-AzApplicationGateway -ResourceGroupName "ResourceGroup01"
```

Det här kommandot får en lista över alla programgateways i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGwList variabeln.

### Exempel 3: Hämta en lista med programgateways i ett abonnemang
```
PS C:\>$AppGwList = Get-AzApplicationGateway
```

Det här kommandot får en lista över alla programgateways i prenumerationen och lagrar dem i $AppGwList variabel.

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

### -Namn
Anger namnet på den Application Gateway som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller programgatewayen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. commands. Networks. Models. PSApplicationGateway

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Stopp-AzApplicationGateway](./Stop-AzApplicationGateway.md)


