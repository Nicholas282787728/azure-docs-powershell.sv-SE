---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214815"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Tar bort en postuppsättning.

## SYNTAX

### Fält
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Mixed
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzDnsRecordSet** tar bort den angivna postuppsättningen från den angivna zonen.
Du kan inte ta bort SOA- eller namnserverposter (NS) som skapas automatiskt i zon apex.
Du kan skicka ett **RecordSet-objekt** till den här cmdleten genom att använda rörledningsoperatorn eller som en parameter.
Om du vill identifiera en post med namn och typ utan att använda ett **RecordSet-objekt** måste du överföra zonen som ett **DnsZone-objekt** till den här cmdleten genom att använda pipelineoperatorn eller parametern, eller så kan du ange parametrarna *ZoneName* och *ResourceGroupName.*
Du kan använda parametern Confirm och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.
När du anger postuppsättningen med ett **RecordSet-objekt** tas inte postuppsättningen bort om den har ändrats i Azure DNS sedan det **lokala RecordSet-objektet** hämtades.
Det här ger skydd för samtidiga ändringar.
Du kan ignorera detta genom att *använda parametern Overwrite,* som tar bort postuppsättningen oavsett samtidiga ändringar.

## EXEMPEL

### Exempel 1: Ta bort en postuppsättning
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

Det första kommandot hämtar den angivna postuppsättningen och lagrar den sedan $RecordSet variabeln. Med det andra kommandot tas postuppsättningen i $RecordSet.

### Exempel 2: Ta bort en postuppsättning och ignorera alla bekräftelser
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Det första kommandot får den angivna postuppsättningen.
Det andra kommandot tar bort postuppsättningen, även om den har ändrats under tiden.
Bekräftelsemeddelanden ignoreras.

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
Anger namnet på den postuppsättning **som ska** tas bort.
När du anger postuppsättningen med namn måste DNS-zonen anges med hjälp av antingen *zonparametern* eller *parametrarna ZoneName* och *ResourceGroupName.*
Du kan också ange postuppsättningen med ett **RecordSet-objekt** och använda *parametern RecordSet.*

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
När du anger postuppsättningen med ett **RecordSet-objekt** tas inte postuppsättningen bort om den har ändrats i Azure DNS sedan det **lokala RecordSet-objektet** hämtades.
Det här ger skydd för samtidiga ändringar.
Det här kan ignoreras med *hjälp av parametern Overwrite,* som tar bort postuppsättningen oavsett samtidiga ändringar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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
Anger det **RecordSet-objekt** som ska tas bort.
Du kan också ange postuppsättningen med  hjälp av parametrarna Namn och Zon eller använda parametrarna *Namn,* Zonnamn och *ResourceGroupName.* 

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Anger typen av DNS-post.
Giltiga värden är:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- TXT SOA-poster tas bort automatiskt när zonen tas bort.
Du kan inte ta bort SOA-poster manuellt.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger resursgruppen som innehåller DNS-zonen som innehåller **recordset** som ska tas bort.
Den här parametern gäller endast när postuppsättningen och DNS-zonen anges med hjälp av *parametrarna Name* och *ZoneName.*
Alternativt kan du ange postuppsättningen med hjälp av *parametern RecordSet* eller *parametrarna Namn* *och* Zon.

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
Anger den DNS-zon som innehåller **RecordSet som ska** tas bort.
Den här parametern gäller endast när du anger postuppsättningen med hjälp av *namnparametern.*
Du kan också ange postuppsättningen med hjälp av parametern *RecordSet* eller parametrarna *Name,* *ZoneName* och *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Anger namnet på zonen som innehåller **RecordSet som ska tas** bort.
Du måste också ange *parametrarna Namn* *och ResourceGroupName.*
Du kan också ange postuppsättningen med hjälp av *parametern RecordSet* eller *parametrarna Name* och *Zone.*

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
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

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

### Microsoft.Azure.Management.DNS.Models.RecordType

### System.String

### Microsoft.Azure.Commands.DNS.DNSZone

### Microsoft.Azure.Commands.dns.DNSRecordSet

## UTDATA

### System.Boolean

## ANTECKNINGAR
Du kan använda *parametern Bekräfta* för att styra om den här cmdleten uppmanar dig att bekräfta.
Som standard uppmanar cmdleten dig att bekräfta om variabeln $ConfirmPreference Windows PowerShell har värdet Medel eller lägre.
Om du anger *Bekräfta* *eller Bekräfta:$True,* uppmanas du i den här cmdleten att bekräfta innan den körs.
Om du *anger Bekräfta:$False* visas ingen bekräftelse i cmdleten.

## RELATERADE LÄNKAR

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
