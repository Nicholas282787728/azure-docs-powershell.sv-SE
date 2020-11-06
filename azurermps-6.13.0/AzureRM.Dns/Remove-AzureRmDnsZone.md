---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580103"
---
# Remove-AzureRmDnsZone

## Sammanfattning
Tar bort en DNS-zon från en resurs grupp.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Fält
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Serverobjektet
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmDnsZone** tar permanent bort en DNS-zon (Domain Name System) från en viss resurs grupp.
Alla post uppsättningar i zonen tas också bort.
Du kan skicka ett **dnsZone** -objekt med parametern *Name* eller med hjälp av pipeline-operatorn eller så kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .
Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.
När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).
Det skyddar ändringar i den gemensamma zonen.
Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.

## BESKRIVS

### Exempel 1: ta bort en zon
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Det här kommandot tar bort zonen med namnet myzone.com från resurs gruppen som heter MyResourceGroup.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Namn
Anger namnet på den DNS-zon som denna cmdlet tar bort.
Du måste också ange parametern *ResourceGroupName* .
Alternativt kan du ange DNS-zonen med parametern *Zone* .

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

### -Skriver över
När du anger zonen med ett **dnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).
Det skyddar ändringar i den gemensamma zonen.
Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.

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
Anger namnet på den resurs grupp som innehåller den zon som ska tas bort.
Du måste också ange parametern *Zonnamn* .
Alternativt kan du ange DNS-zonen med ett **dnsZone** -objekt, som skickas via pipelinen eller parametern *Zone* .

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
Anger den DNS-zon som ska tas bort.
Det **dnsZone** -objekt som skickades kan också överföras via pipeline.
Alternativt kan du ange vilken DNS-zon som ska tas bort med parametrarna *Zonnamn* och *ResourceGroupName* .

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
Visar vad som händer om cmdleten körs.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. DNS. DnsZone
Parametrar: Zone (ByValue)

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR
På grund av den potentiellt omfattande effekten av att ta bort en DNS-zon ber den här cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har något annat värde än none.
Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.
Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta. 

## RELATERADE LÄNKAR

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
