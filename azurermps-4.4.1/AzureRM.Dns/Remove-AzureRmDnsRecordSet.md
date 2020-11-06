---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: e009eea8276bbfe9653c506864604ca955a6367f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574673"
---
# Remove-AzureRmDnsRecordSet

## Sammanfattning
Tar bort en post uppsättning.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Fält
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Mixed
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Serverobjektet
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmDnsRecordSet** tar bort angiven post uppsättning från den angivna zonen.
Du kan inte ta bort SOA-eller namnserver poster som skapas automatiskt vid Zone Apex.

Du kan skicka ett **Recordset** -objekt till denna cmdlet med hjälp av en pipeline-operator eller som en parameter.
Om du vill identifiera en post uppsättning efter namn och typ utan att använda ett **Recordset** -objekt måste du överföra zonen som ett **dnsZone** -objekt till denna cmdlet genom att använda pipeline-operatorn eller som en parameter, eller också kan du ange parametrarna *Zonnamn* och *ResourceGroupName* .

Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.

När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.
Det skyddar mot samtidig ändringar.
Du kan förhindra detta genom att använda parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändring.

## BESKRIVS

### Exempel 1: ta bort en post uppsättning
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

Det första kommandot får den angivna post uppsättningen och lagrar den sedan i $RecordSet variabel. Det andra kommandot tar bort post uppsättningen i $RecordSet.

### Exempel 2: ta bort en post uppsättning och ignorera alla bekräftelser
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

Det första kommandot får den angivna post uppsättningen.

Det andra kommandot tar bort post uppsättningen, även om den har ändrats under tiden.
Bekräftelse uppmaningar ignoreras.

## MALLPARAMETRAR

### -Force
Den här parametern är föråldrad för denna cmdlet.
Den kommer att tas bort i en senare version.

Om du vill kontrol lera om den här cmdleten uppmanar dig att bekräfta kan du använda parametern *Confirm* .

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

### -Namn
Anger namnet på den **post mängd** som ska tas bort.
När du anger post uppsättningen efter namn måste DNS-zonen anges med parametrarna *Zone* eller *Zonnamn* och *ResourceGroupName* .

Du kan också ange en post uppsättning med hjälp av ett **Recordset** -objekt som skickas med hjälp av *post mängds* parametern.

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

### -Skriver över
När du anger en post uppsättning med hjälp av ett **Recordset** -objekt raderas inte post uppsättningen om den har ändrats i Azure DNS sedan det lokala **Recordset** -objektet hämtades.
Det skyddar mot samtidig ändringar.
Det här kan utelämnas med hjälp av parametern *Overwrite* , som tar bort post uppsättningen oavsett samtidig ändringar.

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

### -Post uppsättning
Anger det **Recordset** -objekt som ska tas bort.

Du kan också ange post uppsättningen med *namn* -och *zonkod* eller använda parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .

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

- Kallas
- AAAA
- CNAME
- MX
- NS
- RESURSPOST
- SRV
- TXT

SOA-poster tas bort automatiskt när zonen tas bort.
Du kan inte ta bort SOA-poster manuellt.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger den resurs grupp som innehåller den DNS-zon som innehåller den **post uppsättning** som ska tas bort.
Den här parametern är endast tillämpbar när post uppsättningen och DNS-zonen anges med parametrarna *namn* och *Zonnamn* .

Alternativt kan du ange den post uppsättning som använder parametern *post uppsättning* eller *namn* - *och parameter parametrar* .

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
Anger den DNS-zon som innehåller den **post uppsättning** som ska tas bort.
Den här parametern används endast när du anger en post uppsättning med parametern *Name* .

Eller så kan du ange den post uppsättning som använder parametern *post uppsättning* eller parametrarna *namn* , *Zonnamn* och *ResourceGroupName* .

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

### -Zonnamn
Anger namnet på den zon som innehåller **post mängden** som ska tas bort.
Du måste också ange *namnet* och *ResourceGroupName* parametrar.

Du kan också ange post uppsättningen genom att använda parametern *post mängd* eller *namn* *-och parameter* parametrar.

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

### Microsoft. Azure. commands. DNS. DnsRecordSet
Du kan **göra en pipe** till den här cmdleten.

## VÄRDEN

### Ingen
Denna cmdlet genererar inga utdata.

## ANMÄRKNINGAR
Du kan använda parametern *Confirm* för att kontrol lera om denna cmdlet uppmanar dig att bekräfta.
Som standard ber cmdleten dig att bekräfta om $ConfirmPreference Windows PowerShell-variabeln har värdet medel eller lägre.

Om du anger *Bekräfta* eller *Bekräfta: $true* ber denna cmdlet dig att bekräfta innan den körs.
Om du anger *Bekräfta: $false* ber cmdleten dig inte att bekräfta.

## RELATERADE LÄNKAR

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
