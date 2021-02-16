---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233582"
---
# Get-AzBillingInvoice

## SYNOPSIS
Hämta faktureringsfakturor för prenumerationen.
Hämta faktureringsfakturor för ett faktureringskonto och en faktureringsprofil

## SYNTAX

### Lista (standard)
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### Senaste
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### Enkel
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzBillingInvoice** hämtar faktureringsfakturor för prenumerationen. 

## EXEMPEL

### Exempel 1
```
PS C:\> Get-AzBillingInvoice -Latest
```

Hämta den senaste fakturan för prenumerationen.

### Exempel 2
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

Hämta fakturan för prenumerationen med det angivna namnet.

### Exempel 3
```
PS C:\> Get-AzBillingInvoice
```

Hämta alla tillgängliga fakturor för prenumerationen i omvänd kronologisk ordning med början från den senaste fakturan utan att ladda ned URL. 

### Exempel 4
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

Få de senaste 10 fakturorna för prenumerationen och inkludera URL-adressen för nedladdning i resultatet.

### Exempel 5
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

Få den specifika fakturan med namn och inkludera url för nedladdning i resultatet.

### Exempel 6
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Få fakturor med namnet på faktureringskontot och inkludera hämtnings-URL för varje faktura i resultatet.

### Exempel 7
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Få en särskild faktura med fakturanamn och kontonamn för fakturering och inkludera URL för nedladdning för varje faktura i resultatet.

### Exempel 8
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

Få senaste fakturan med namnet på faktureringskontot och inkludera url för nedladdning av faktura i resultatet.

### Exempel 9
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

Få de senaste 10 fakturorna för det specifika faktureringskontot och den specifika faktureringsprofilen och inkludera URL-adressen för nedladdning i resultatet.

### Exempel 10
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

Få senaste fakturan med namnet på faktureringskontot och namnet på faktureringsprofilen och inkludera url-adressen för faktura i resultatet.

### Exempel 10
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

Hämta fakturorna med namnet på faktureringskontot och namnet på faktureringsprofilen för en faktureringsperiod som anges perioStartdatum och periodNummerdatum.


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

### -GenerateDownloadUrl
Generera nedladdnings-URL:en för fakturorna.

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
Hämta den senaste fakturan.

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
Bestämmer det maximala antalet poster som ska returneras.

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

### -Name
Namnet på en viss faktura som du vill få eller den senaste om den inte anges.

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
Namnet på ett visst faktureringskonto som du kan hämta fakturor för.

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
Namnet på en viss faktureringsprofil som du kan hämta fakturor för.

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
Startdatum för faktura.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Billing.Models.PSInvoice

## ANTECKNINGAR

## RELATERADE LÄNKAR
