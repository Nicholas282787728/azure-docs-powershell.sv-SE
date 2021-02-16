---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253784"
---
# New-AzDnsZone

## SYNOPSIS
Skapar en ny DNS-zon.

## SYNTAX

### Ids (standard)
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Namn
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzDnsZone** skapar en ny DNS-zon (Domain Name System) i den angivna resursgruppen. Du måste ange ett unikt DNS-zonnamn för *parametern Name,* annars returnerar cmdleten ett fel. När zonen har skapats använder du cmdleten New-AzDnsRecordSet för att skapa postuppsättningar i zonen.
Du kan använda *parametern Confirm* och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.

## EXEMPEL

### Exempel 1: Skapa en DNS-zon
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Med det här kommandot skapas en ny DNS myzone.com med namnet myzone.com den angivna resursgruppen och sedan lagras den i $Zone variabeln.

### Exempel 2: Skapa en privat DNS-zon genom att ange virtuella nätverks-ID
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resursgruppen med ett associerat virtuellt lösningsnätverk (anger dess ID) och lagrar det sedan i den $Zone variabeln.

### Exempel 3: Skapa en privat DNS-zon genom att ange virtuella nätverksobjekt
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

Det här kommandot skapar en ny privat DNS-zon med namnet myprivatezone.com i den angivna resursgruppen med ett associerat virtuellt lösningsnätverk (som refereras av variabeln $ResVirtualNetwork) och lagrar sedan den i $Zone-variabeln.

### Exempel 4: Skapa en DNS-zon med delegering genom att ange namnet på en överordnad zon
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

Det här kommandot skapar en ny underordnad DNS-zon mychild.zone.com den angivna resursgruppen och lagrar i den $Zone variabeln.
Den lägger också till delegering i den överordnade DNS-zone.com som finns i samma prenumeration och resursgrupp som underzon.

### Exempel 5: Skapa en DNS-zon med delegering genom att ange id för överordnad zon
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

Det här kommandot skapar en ny underordnad DNS-zon mychild.zone.com den angivna resursgruppen och lagrar i den $Zone variabeln.
Det lägger också till delegering i den överordnade DNS-zonen med namnet zone.com i resursgruppens andra prenumerationer som tillhandahålls är samma som i den underordnade zon som skapats.

### Exempel 6: Skapa en DNS-zon med delegering genom att ange ett överordnat zonobjekt
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

Det här kommandot skapar en ny underordnad DNS-zon mychild.zone.com den angivna resursgruppen och lagrar i den $Zone variabeln.
Det lägger också till delegering i den överordnade DNS-zone.com som överförs i ParentZone-objektet

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
Anger namnet på den DNS-zon som ska skapas.

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

### -ParentZone
Det fullständiga namnet på den överordnade zonen som du vill lägga till delegering för (utan en avslutande punkt).

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneId
Resurs-ID för den överordnade zonen som du vill lägga till delegering för (utan en avslutande punkt).

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentZoneName
Det fullständiga namnet på den överordnade zonen som du vill lägga till delegering för (utan en avslutande punkt).

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegistrationVirtualNetwork
Listan över virtuella nätverk som registrerar värdnamn för virtuell dator i den här DNS-zonen, endast tillgänglig för privata zoner.

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
Listan med virtuella nätverks-ID som registrerar värdnamn för virtuell dator i den här DNS-zonen, endast tillgänglig för privata zoner.

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
Listan över virtuella nätverk som kan lösa poster i den här DNS-zonen, endast tillgänglig för privata zoner.

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
Listan med virtuella nätverks-IDs som kan matcha poster i den här DNS-zonen, endast tillgänglig för privata zoner.

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
Anger den resursgrupp där zonen ska skapas.

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

### -Tag
Nyckelvärdepar i form av en hash-tabell. Exempel: @{key0="value0";key1=$null;key2="value2"}

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
Typ av zon, offentlig eller privat. Zoner utan en typ eller med en typ av offentlig blir tillgängliga på den offentliga DNS-servergrupp som används i DNS-hierarkin. Zoner med en typ av privat visas bara från en uppsättning associerade virtuella nätverk (den här funktionen är i förhandsversion). Den här egenskapen kan inte ändras för en zon.

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
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte. Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Collections.Hashtable

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## UTDATA

### Microsoft.Azure.Commands.DNS.DNSZone

## ANTECKNINGAR
Du kan använda *parametern Bekräfta* för att styra om den här cmdleten uppmanar dig att bekräfta.
Som standard uppmanar cmdleten dig att bekräfta om variabeln $ConfirmPreference Windows PowerShell har värdet Medel eller lägre.
Om du anger *Bekräfta* *eller Bekräfta:$True,* uppmanas du i den här cmdleten att bekräfta innan den körs.
Om du *anger Bekräfta:$False* visas ingen bekräftelse i cmdleten.

## RELATERADE LÄNKAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)
