---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214807"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Uppdaterar en DNS-postuppsättning.

## SYNTAX

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzDnsRecordSet** uppdaterar en postuppsättning i Azure DNS-tjänsten från ett lokalt **RecordSet-objekt.**
Du kan överföra ett **RecordSet-objekt** som en parameter eller med hjälp av rörledningsoperatorn.
Du kan använda *parametern Confirm* och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.
Postuppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **RecordSet-objektet** hämtades.
Det här ger skydd för samtidiga ändringar.
Du kan dölja det här *beteendet med parametern Overwrite,* som uppdaterar postuppsättningen oavsett samtidiga ändringar.

## EXEMPEL

### Exempel 1: Uppdatera en postuppsättning
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

Det första kommandot använder cmdleten Get-AzDnsRecordSet för att få den angivna postuppsättningen och lagrar den sedan i $RecordSet variabeln.
Det andra och tredje kommandona är åtgärder som inte är radbaserade för att lägga till två A-poster i postuppsättningen.
Det slutliga kommandot använder **cmdleten Set-AzDnsRecordSet** för att bekräfta uppdateringen.

### Exempel 2: Uppdatera en SOA-post
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

Det första kommandot använder **cmdleten Get-AzDnsRecordset** för att få den angivna postuppsättningen och lagrar den sedan i $RecordSet variabeln.
Det andra kommandot uppdaterar den angivna SOA-posten i $RecordSet.
Det slutliga kommandot använder **cmdleten Set-AzDnsRecordSet** till att sprida uppdateringen i $RecordSet.

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

### -Overwrite
Anger att postuppsättningen ska uppdateras oavsett samtidiga ändringar.
Postuppsättningen uppdateras inte om den har ändrats i Azure DNS sedan det lokala **RecordSet-objektet** hämtades.
Det här ger skydd för samtidiga ändringar.
Om du vill dölja det här beteendet kan du använda parametern *Overwrite,* vilket resulterar i att postuppsättningen uppdateras oavsett samtidiga ändringar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecordSet
Anger den **postuppsättning som** ska uppdateras.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.Commands.dns.dnsRecordSet

## UTDATA

### Microsoft.Azure.Commands.dns.DNSRecordSet

## ANTECKNINGAR
Du kan använda *parametern Bekräfta* för att styra om den här cmdleten uppmanar dig att bekräfta.
Som standard uppmanar cmdleten dig att bekräfta om variabeln $ConfirmPreference Windows PowerShell har värdet Medel eller lägre.
Om du anger *Bekräfta* *eller Bekräfta:$True,* uppmanas du i den här cmdleten att bekräfta innan den körs.
Om du *anger Bekräfta:$False* visas ingen bekräftelse i cmdleten. 

## RELATERADE LÄNKAR

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
