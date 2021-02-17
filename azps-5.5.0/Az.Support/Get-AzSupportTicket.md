---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216903"
---
# Get-AzSupportTicket

## SYNOPSIS
Få supportärenden.

## SYNTAX

### ListParameterSet (standard)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## BESKRIVNING
Får listan över supportärenden. Alla supportärenden hämtas om du inte anger några parametrar. Du kan också filtrera supportärenden efter Status eller CreatedDate med filterparametern. Här är några exempel på filtervärden som du kan ange.

| Scenario                                                         | Filter                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Skaffa biljetter som är öppna                               | "Status eq 'Open'"                               |
| Skaffa biljetter som är i stängt läge                             | "Status eq 'Closed'"                             |
| Hämta biljetter som skapades den 20 december 2019 eller senare         | "CreatedDate ge 2019-12-20"                      |
| Hämta biljetter som skapades efter 20 december 2019               | "CreatedDate gt 2019-12-20"                      |
| Får biljetter skapade efter den 20 december 2019 som är öppna | "CreatedDate gt 2019-12-20 och Status eq 'Open'" |


Den här cmdleten har stöd för parametrar för sidnumrering via first och skip.

Du kan också hämta ett enskilt support ärende genom att ange namnet på biljetten. 

## EXEMPEL

### Exempel 1: Hämta de första två biljetterna
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 2: Hämta de första två biljetterna efter att du hoppat över de första två
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 3: Skapa ett support ärende efter namn
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Exempel 4: Få de första två supportärenden filtrerade efter status
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 5: Få alla supportärenden som är i öppet läge och som skapats efter den 20 december 2019
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Filter
Filter som ska tillämpas på resultatet av denna cmdlet.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Namn på support ärende som denna cmdlet får.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Rapporterar det totala antalet objekt i datauppsättningen (ett heltal) följt av de markerade objekten.
Om cmdleten inte kan fastställa det totala antalet visas "Okänt totalt antal". Heltal har egenskapen Noggrannhet som anger tillförlitligheten för det totala antal-värdet.
Värdet för noggrannhetsområden mellan 0,0 och 1,0 där 0,0 innebär att cmdleten inte kunde räkna objekten, 1,0 innebär att antalet är exakt och ett värde mellan 0,0 och 1,0 anger en mer tillförlitlig uppskattning.

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

### -Skip
Ignorerar det angivna antalet objekt och hämtar sedan återstående objekt.
Ange hur många objekt du vill hoppa över.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Hämtar endast det angivna antalet objekt.
Ange hur många objekt som ska fås.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## ANTECKNINGAR

## RELATERADE LÄNKAR
