---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214814"
---
# Remove-AzDnsZone

## SYNOPSIS
Tar bort en DNS-zon från en resursgrupp.

## SYNTAX

### Fält
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Remove-AzDnsZone** tar bort en DNS-zon (Domain Name System) permanent från en angiven resursgrupp.
Alla postuppsättningar i zonen tas också bort.
Du kan överföra ett **DnsZone-objekt** med *hjälp* av parametern Name eller med hjälp av rörledningsoperatorn, eller så kan du ange parametrarna *ZoneName* och *ResourceGroupName.*
Du kan använda parametern Confirm och $ConfirmPreference Windows PowerShell för att styra om cmdleten uppmanar dig att bekräfta.
När du anger zonen med ett **DnsZone-objekt** (som skickas via pipeline- eller zonparametern) tas zonen inte bort om den har ändrats i Azure DNS sedan det lokala **DnsZone-objektet** hämtades (endast åtgärder direkt i DNS-zonresursantalet som ändringar, åtgärder för postuppsättningar i zonen påverkas inte). 
Det här ger skydd för samtidiga zonändringar.
Detta kan ignoreras med *parametern Overwrite,* som tar bort zonen oavsett samtidiga ändringar.

## EXEMPEL

### Exempel 1: Ta bort en zon
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Med det här kommandot tas zonen myzone.com från resursgruppen MyResourceGroup.

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
Anger namnet på den DNS-zon som cmdleten tar bort.
Du måste också ange *parametern ResourceGroupName.*
Du kan också ange DNS-zonen med hjälp av *zonparametern.*

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

### -Overwrite
När du anger zonen med ett **DnsZone-objekt** (som skickas via pipeline- eller zonparametern) tas zonen inte bort om den har ändrats i Azure DNS sedan det lokala **DnsZone-objektet** hämtades (endast åtgärder direkt i DNS-zonresursantalet som ändringar, åtgärder för postuppsättningar i zonen påverkas inte). 
Det här ger skydd för samtidiga zonändringar.
Detta kan ignoreras med *parametern Overwrite,* som tar bort zonen oavsett samtidiga ändringar.

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

### -ResourceGroupName
Anger namnet på den resursgrupp som innehåller zonen som ska tas bort.
Du måste också ange *zonename-parametern.*
Du kan också ange DNS-zonen med ett **DnsZone-objekt** som överförs via antingen pipelinen eller *zone-parametern.*

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
Anger DEN DNS-zon som ska tas bort.
**DnsZone-objektet** som överförs kan också skickas via pipelinen.
Du kan också ange vilken DNS-zon som ska tas bort med hjälp av *parametrarna ZoneName* och *ResourceGroupName.*

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

### System.String

### Microsoft.Azure.Commands.dns.DNSZone

## UTDATA

### System.Boolean

## ANTECKNINGAR
På grund av potentiellt hög inverkan med att ta bort en DNS-zon uppmanar den här cmdleten som standard att bekräfta om variabeln $ConfirmPreference Windows PowerShell har något annat värde än Ingen.
Om du anger *Bekräfta* *eller Bekräfta:$True,* uppmanas du i den här cmdleten att bekräfta innan den körs.
Om du *anger Bekräfta:$False* visas ingen bekräftelse i cmdleten. 

## RELATERADE LÄNKAR

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
