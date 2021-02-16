---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225558"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Anger egenskapsvärden för ett meddelandehubbens namnområde.

## SYNTAX

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Set-AzNotificationHubsNamespace** anger egenskapsvärdena för ett befintligt namnområde för meddelandehubben.
Namnområden är logiska behållare som hjälper dig att organisera och hantera dina meddelandehubben.
Du måste ha minst ett namnområde för meddelandehubben.
Dessutom måste alla meddelandehubben ha ett tilldelat namnområde.
Den här cmdleten används främst för att aktivera och inaktivera ett namnområde.
När ett namnområde är inaktiverat kan användare inte ansluta till något av meddelandehubben i namnområdet, och inte heller kan administratörer använda dessa nav för att skicka push-meddelanden.
Om du vill återaktivera ett inaktiverat namnområde använder du den här cmdleten till att ange **egenskapen** Tillstånd för namnområdet till Aktiv.
Du kan också använda den här cmdleten till att märka ett namnområde som kritiskt.
Det förhindrar att namnområdet tas bort.
Om du vill ta bort ett viktigt namnområde måste du först ta bort den kritiska taggen.

## EXEMPEL

### Exempel 1: Inaktivera ett namnområde
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Med det här kommandot inaktiveras namnområdet ContosoPartners som finns i datacentret Väst USA och tilldelas resursgruppen ContosoNotificationsGroup.

### Exempel 2: Aktivera ett namnområde
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Med det här kommandot aktiveras namnområdet ContosoPartners i datacentret Väst USA som tilldelats resursgruppen ContosoNotificationsGroup.

## PARAMETERS

### -Kritiskt
Anger om namnområdet är ett viktigt namnområde.
Kritiska namnområden kan inte tas bort.
Om du vill ta bort ett viktigt namnområde måste du ange värdet för egenskapen till False för att namnområdet ska markeras som icke-kritiskt.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
Be inte om bekräftelse.

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

### -Plats
Anger visningsnamnet för det datacenter som är värd för namnområdet.
Du kan ange den här parametern till valfri giltig Azure-plats, men för optimala prestanda bör du använda ett datacenter nära majoriteten av användarna.
Om du vill ha en uppdaterad lista över Azure-platser kör du följande kommando: `Get-AzLocation | Select-Object DisplayName`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Anger namnområdet som cmdleten ändrar.
Namnområden är ett sätt att gruppera och kategorisera meddelandehubben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Anger den resursgrupp som namnområdet är tilldelat till.
Resursgrupper organiserar objekt som namnområden, meddelandehubben och auktoriseringsregler på ett sätt som bara hjälper lagerhantering och Azure-administration.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
SKU-nivån i namnområdet

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Delstat
Anger namnområdets aktuella status.
De godtagbara värdena för den här parametern är: Aktiva och inaktiverade.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Anger namnvärdepar som kan användas för att kategorisera och ordna Azure-objekt.
Taggar fungerar ungefär som nyckelord och fungerar över en distribution.
Om du till exempel söker efter alla objekt med taggavdelningen:IT returneras alla Azure-objekt som har den taggen, oavsett sådant som objekttyp, plats eller resursgrupp.
En enskild tagg består av två delar: *namnet* och (om du vill) *värdet.*
I Avdelning:IT är till exempel taggnamnet Avdelning och taggvärdet ÄR IT.
Om du vill lägga till en tagg använder du hashtabellsyntaxen som liknar den här, vilket skapar taggen CalendarYear:2016: -Tags @{Name="CalendarYear"; Value="2016"} Om du vill lägga till flera taggar i samma kommando avgränsar du de enskilda taggarna med kommatecken: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


