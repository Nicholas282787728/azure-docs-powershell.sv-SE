---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524695"
---
# Get-AzBillingInvoice

## Sammanfattning
Skaffa faktura fakturor för abonnemanget.
Få fakturerings fakturor för ett fakturerings konto och en fakturerings profil

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### RelatesTo
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Enda
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzBillingInvoice** får fakturerings fakturor för abonnemanget. 

## BESKRIVS

### Exempel 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Få den senaste fakturan för abonnemanget.

### Exempel 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Hämta prenumerationen för abonnemanget med det angivna namnet.

### Exempel 3
```
PS C:\> Get-AzBillingInvoice
```

Hämta alla tillgängliga fakturor för abonnemanget i omvänd kronologisk ordning med början med den senaste fakturan utan nedladdnings-URL. 

### Exempel 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Få de senaste 10 fakturorna för abonnemanget och inkludera nedladdnings-URL: en i resultatet.

### Exempel 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Hämta den specifika fakturan efter namn och ta med nedladdnings-URL i resultatet.

### Exempel 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Skaffa fakturor efter namn på fakturerings konto och ta med nedladdnings-URL för varje faktura i resultatet.

### Exempel 7
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Hämta specifika fakturor efter faktura namn och fakturerings konto namn och inkludera URL-adressen för varje faktura i resultatet.

### Exempel 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Hämta senaste faktura efter namn på fakturerings konto och inkludera URL-adressen för en faktura i resultatet.

### Exempel 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Skaffa de senaste 10 fakturorna till det specifika fakturerings kontot och en viss fakturerings profil och inkludera URL-adressen för nedladdning i resultatet.

### Exempel 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Hämta den senaste fakturan med namn på fakturerings kontot och namnet på fakturerings profilen och ta med URL-adressen till nedladdning i resultatet.

### Exempel 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Skaffa fakturor efter namn på fakturerings konto och profil namn för en fakturerings period som anges med perioStart datum och periodEnd datum.


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

### -GenerateDownloadUrl
Generera nedladdnings-URL: en för fakturorna.

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

### -Senaste
Skaffa den senaste fakturan.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCount
Avgör det maximala antalet poster som ska returneras.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namnet på en specifik faktura för att få eller den senaste om den inte anges.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingAccountName
Namnet på ett specifikt fakturerings konto för att få fakturor för.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BillingProfileName
Namnet på en viss fakturerings profil för att få fakturor för.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodStartDate
Start datum för faktura.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeriodEndDate
Slutdatum för faktura.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. Billing. Models. PSInvoice

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
