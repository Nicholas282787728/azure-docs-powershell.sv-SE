---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521926"
---
# Get-AzSupportTicket

## Sammanfattning
Få support biljetter.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Hämtar listan med support biljetter. Då hämtas alla support biljetter om du inte anger några parametrar. Du kan också filtrera support biljetter efter status eller CreatedDate med hjälp av parametern filter. Här är några exempel på filter värden som du kan ange.

| Ovanligt                                                         | Filtrera                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Få biljetter som är öppna                               | "Status EQ" Open "                               |
| Få biljetter som är i stängt tillstånd                             | "Status EQ" stängd "                             |
| Få biljetter som skapades på eller efter den 20 dec, 2019         | "CreatedDate ge 2019-12-20"                      |
| Få biljetter som har skapats efter den 20 dec 2019               | "CreatedDate gt 2019-12-20"                      |
| Hämtar biljetter som skapats efter den 20 dec, 2019 som är i öppet läge | "CreatedDate gt 2019-12-20 och status EQ" Open " |


Denna cmdlet har stöd för växling via första och hoppa över parametrar.

Du kan också hämta ett enskilt support ärende genom att ange biljett namnet. 

## BESKRIVS

### Exempel 1: få första 2 biljetterna
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 2: få första två biljetter efter att ha hoppat av de första två
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 3: skaffa ett support ärende utifrån namn
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Exempel 4: Hämta första 2 support biljetter filtrerade efter status
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Exempel 5: få alla support biljetter som är öppna och skapade efter dec den 2019
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Namn
Namnet på det support ärende som denna cmdlet får.

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
Rapporterar totalt antal objekt i data uppsättningen (ett heltal) följt av de markerade objekten.
Om cmdleten inte kan bestämma det totala antalet visar den "okänt antal". Heltalet har en egenskap för exakthet som anger tillförlitligheten hos det totala värdet.
Värdet för precisions intervall från 0,0 till 1,0 där 0,0 innebär att cmdleten inte kan räkna antalet objekt, ger 1,0 att antalet är exakt och ett värde mellan 0,0 och 1,0 tyder på en allt tillförlitlig uppskattning.

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

### -Hoppa över
Ignorerar angivet antal objekt och hämtar sedan återstående objekt.
Ange antalet objekt som ska hoppas över.

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

### -Först
Hämtar bara angivet antal objekt.
Ange antalet objekt som ska visas.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. support. Models. PSSupportTicket

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
