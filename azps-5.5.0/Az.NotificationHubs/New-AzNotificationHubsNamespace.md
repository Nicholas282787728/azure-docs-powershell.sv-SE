---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225582"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Skapar ett namnområde för meddelandehubben.

## SYNTAX

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzNotificationHubsNamespace** skapar ett namnområde för meddelandehubben.
Namnområden är logiska behållare som hjälper dig att organisera och hantera dina meddelandehubben.
Du måste ha minst ett namnområde för meddelandehubben.
Ett enda namnområde kan ha flera nav.
Du kan ha flera namnområden för att organisera dina nav, eller för att ge enskilda personer behörighet att hantera en markerad delmängd av naven.
Om du vill skapa ett namnområde måste du ange ett unikt namn för namnområdet. ange det datacenter där namnområdet ska vara; och anger den resursgrupp som namnområdet ska tilldelas till.
När namnområdet har skapats kan du använda cmdleten New-AzNotificationHubsNamespaceAuthorizationRules för att tilldela auktoriseringsregler till det namnområdet.
Auktoriseringsregler används för att hantera behörigheter till namnområdet.

## EXEMPEL

### Exempel 1: Skapa ett meddelandenav
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Med det här kommandot skapas ett meddelandenav med namnet ContosoPartners.
Namnområdet finns i datacentret väst i USA och tilldelas till resursgruppen ContosoNotificationsGroup.

### Exempel 2: Skapa ett meddelandenav med taggar
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Med det här kommandot skapas ett meddelandenav med namnet ContosoPartners.
Namnområdet finns i datacentret väst i USA och tilldelas till resursgruppen ContosoNotificationsGroup.
Det här kommandot skapar dessutom en tagg med namnet Målgrupp och värdet PartnerOrganizations och tilldelas till namnområdet.
Detta garanterar att namnområdet visas varje gång du filtrerar för objekt där målgruppstaggen är inställd på PartnerOrganizations.

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

### -Plats
Anger visningsnamnet för det datacenter som kommer att vara värd för namnområdet.
Du kan ange den här parametern till valfri giltig plats, men för optimala prestanda kanske du vill använda ett datacenter nära majoriteten av användarna.

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
Anger namnet på det nya namnområdet.
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
Anger den resursgrupp som namnområdet ska tilldelas till.
Resursgrupper ordnar objekt som namnområden, meddelandehubben och auktoriseringsregler på ett sätt som bara hjälper lagerhantering och administration.

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

### -Tag
Anger namnvärdepar som kan användas för att kategorisera och ordna Azure-objekt.
Taggar fungerar ungefär som nyckelord och fungerar över en distribution.
Om du till exempel söker efter alla objekt med taggavdelningen:IT returneras alla Azure-objekt som har den taggen, oavsett sådant som objekttyp, plats eller resursgrupp.
En enskild tagg består av två delar: *namnet* och, om du vill, *värdet.*
I Avdelning:IT är till exempel taggnamnet Avdelning och taggvärdet är IT.
Om du vill lägga till en tagg använder du hashtabellsyntaxen som liknar den här, så att taggen CalendarYear:2016 skapas:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### System.Collections.Hashtable

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


