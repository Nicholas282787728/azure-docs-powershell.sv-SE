---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237938"
---
# Get-AzDnsZone

## SYNOPSIS
Får en DNS-zon.

## SYNTAX

### Standard (standard)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroup
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDnsZone** får en DNS-zon (Domain Name System) från den angivna resursgruppen.
Om du anger *parametern Name* returneras ett enda **DnsZone-objekt.**
Om du inte anger *parametern Name* returneras en matris som innehåller alla zoner i den angivna resursgruppen.
Du kan använda **DnsZone-objektet** för att uppdatera zonen, till exempel lägga till **RecordSet-objekt** i den.

## EXEMPEL

### Exempel 1: Skaffa en zon
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

I det här exemplet får DNS-zonen myzone.com från den angivna resursgruppen och lagrar den sedan $Zone variabeln.

### Exempel 2: Hämta alla zoner i en resursgrupp
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

I det här exemplet får du alla DNS-zoner i den angivna resursgruppen och lagrar den sedan $Zones variabeln.

### Exempel 3: Hämta alla zoner i en prenumeration
```
PS C:\> $Zones = Get-AzDnsZone
```

I det här exemplet får du alla DNS-zoner i den aktuella Azure-prenumerationen och lagrar dem sedan $Zones variabeln.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Anger namnet på den DNS-zon som ska hämtas.
Om du inte anger ett värde för parametern *Name* får den här cmdleten alla DNS-zoner i den angivna resursgruppen.
Om du utelämnar parametern *ResourceGroupName* får den här cmdleten alla DNS-zoner i den aktuella Azure-prenumerationen.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resursgruppen som innehåller DNS-zonen som ska hämtas.
Om du inte anger *ResourceGroupName* måste du också utelämna *namnparametern.*
I det här fallet får den här cmdleten alla DNS-zoner i den aktuella Azure-prenumerationen.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.DNS.DNSZone

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
