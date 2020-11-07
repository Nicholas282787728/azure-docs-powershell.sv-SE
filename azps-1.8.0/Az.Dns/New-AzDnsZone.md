---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: eb7a2f3494521a5505db0224bb1ae0ff948d406f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754121"
---
# New-AzDnsZone

## Sammanfattning
Skapar en ny DNS-zon.

## FRÅGESYNTAXEN

### ID (standard)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekten
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resurs gruppen. Du måste ange ett unikt DNS-zonnamn för parametern *Name* , eller så returnerar cmdleten ett fel. När zonen har skapats kan du använda New-AzDnsRecordSet cmdlet för att skapa post uppsättningar i zonen.
Du kan använda *Confirm* -parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.

## BESKRIVS

### Exempel 1: skapa en DNS-zon
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Det här kommandot skapar en ny DNS-zon som heter myzone.com i angiven resurs grupp och lagrar den sedan i $Zone variabel.

### Exempel 2: skapa en privat DNS-zon genom att ange virtuella nätverks-ID
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (som anger dess ID) och lagrar det sedan i $Zone variabel.

### Exempel 3: skapa en privat DNS-zon genom att ange virtuella nätverks objekt
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

Det här kommandot skapar en ny privat DNS-zon som heter myprivatezone.com i den angivna resurs gruppen med ett associerat virtuellt nätverk (kallas $ResVirtualNetwork variabel) och lagrar sedan in det i $Zone-variabeln.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Namn
Anger namnet på DNS-zonen som ska skapas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Listan med virtuella nätverk som ska registrera poster för virtuella dator namn i denna DNS-zon är bara tillgängliga för privata zoner.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetworkId
Listan över virtuella nätverks-ID: n som registrerar virtuella dator namn poster i denna DNS-zon är bara tillgängliga för privata zoner.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetwork
Listan med virtuella nätverk som kan lösa poster i den här DNS-zonen, är endast tillgänglig för privata zoner.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResolutionVirtualNetworkId
Listan över virtuella nätverks-ID: n som kan användas för att lösa poster i denna DNS-zon är bara tillgängliga för privata zoner.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger den resurs grupp som du vill skapa zonen i.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Par med nyckelord i form av en hash-tabell. Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ZoneType
Typen av zon, offentlig eller privat. Zoner utan typ eller med en typ av offentliga tjänster görs tillgängliga för det offentliga DNS-tjänsten för användning i DNS-hierarkin. Zoner med en typ av privat är bara synliga från med uppsättningen associerade virtuella nätverk (den här funktionen är i för hands version). Det går inte att ändra den här egenskapen för en zon.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte. Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. ZoneType, Microsoft. Azure. Management. DNS, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Collections. hash

### System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]

### System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. IResourceReference, Microsoft. Azure. PowerShell. clients. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

## VÄRDEN

### Microsoft. Azure. commands. DNS. DnsZone

## ANMÄRKNINGAR
Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.
Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.
Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.
Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.

## RELATERADE LÄNKAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
