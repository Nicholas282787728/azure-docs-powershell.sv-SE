---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230415"
---
# Get-AzDnsRecordSet

## SYNOPSIS
Hämtar en DNS-postuppsättning.

## SYNTAX

### Fält
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzDnsRecordSet får DNS-posten** (Domain Name System) inställd med det angivna namnet och typen i den angivna zonen.
Om du inte anger parametrarna *Name* eller *RecordType* returnerar denna cmdlet alla postuppsättningar av den angivna typen i zonen.
Om du anger *RecordType-parametern* men inte *namnparametern* returnerar den här cmdleten alla postuppsättningar av den angivna posttypen.
Du kan använda en pipelineoperator för att överföra ett **DnsZone-objekt** till den här cmdleten, eller så kan du överföra ett **DnsZone-objekt** som  zonparameter, eller så kan du ange zon- och resursgruppen efter namn.

## EXEMPEL

### Exempel 1: Hämta postuppsättningar med ett angivet namn och en viss typ
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Det här kommandot hämtar postuppsättningen av posttypen A med namnet www i den angivna resursgruppen och -zonen och lagrar den sedan i $RecordSet variabeln.
Eftersom *parametrarna Namn* *och RecordType* anges returneras bara ett **RecordSet-objekt.**

### Exempel 2: Hämta postuppsättningar av en angiven typ
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Det här kommandot hämtar en matris av alla postuppsättningar av posttyp A i zonen myzone.com i resursgruppen MyResourceGroup och lagrar dem sedan i $RecordSets variabeln.

### Exempel 3: Hämta alla postuppsättningar i en zon
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Med det här kommandot får du en matris med alla postuppsättningar i zonen myzone.com i resursgruppen MyResourceGroup och lagrar dem sedan i $RecordSets variabeln.

### Exempel 4: Hämta alla postuppsättningar i en zon med hjälp av ett DnsZone-objekt
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Det här exemplet motsvarar exempel 3 ovan.
Den här gången anges zonen med hjälp av ett zonobjekt.

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
Anger namnet på den **postuppsättning som ska** hämtas.
Om du inte anger *parametern Name* returneras alla postuppsättningar av den angivna typen.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Anger vilken typ av DNS-post som cmdleten hämtar.
Giltiga värden är: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Om du inte anger *RecordType-parametern* måste du också utelämna *name-parametern.* Denna cmdlet returnerar sedan alla postuppsättningar i zonen (för alla namn och typer).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger resursgruppen som innehåller DNS-zonen.
Zonnamnet måste också anges med hjälp av *zonename-parametern.*
Du kan också ange zon- och resursgruppen genom att skicka in ett **DnsZone-objekt** med hjälp av *zonparametern.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Anger den DNS-zon som innehåller postuppsättningen som denna cmdlet hämtar.
Du kan också ange zonen med hjälp av *parametrarna ZoneName* *och ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Anger namnet på den DNS-zon som innehåller postuppsättningen som ska hämtas.
Resursgruppen som innehåller zonen måste också anges, med parametern *ResourceGroupName.*
Du kan också ange zon- och resursgruppen genom att skicka in ett DNS-zonobjekt med hjälp av *zonparametern.*

```yaml
Type: System.String
Parameter Sets: Fields
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

### Microsoft.Azure.Commands.dns.DNSZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## UTDATA

### Microsoft.Azure.Commands.dns.dnsRecordSet

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


