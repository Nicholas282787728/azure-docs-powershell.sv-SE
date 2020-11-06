---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 504fe8b5aad0e2e028bf27cf08a29fd335edfa33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577114"
---
# New-AzureRmNotificationHubsNamespace

## Sammanfattning
Skapar ett namn område för en aviserings hubb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmNotificationHubsNamespace** skapar ett namn område för meddelande navet.

Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.
Du måste ha minst ett namn område för aviserings navet.
Ett enskilt namn område kan House flera nav.
Du kan ha flera namn utrymmen för att organisera dina nav eller för att ge specifika enskilda personer tillstånd att hantera en viss delmängd av dina nav.

Om du vill skapa ett namn område kontrollerar du att du anger ett unikt namn för namn området. Ange data Center där namn området ska placeras; och ange den resurs grupp som namn området ska tilldelas till.
När namn området har skapats kan du använda New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet för att tilldela auktoriseringsregler till namn området.
Auktoriseringsregler används för att hantera behörigheter till namn området.

## BESKRIVS

### Exempel 1: skapa ett meddelande nav
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.
Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.

### Exempel 2: skapa ett huvud meddelande med Taggar
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Det här kommandot skapar ett meddelande nav med namnet ContosoPartners.
Namn området placeras i det västra amerikanska data centret och kopplas till resurs gruppen ContosoNotificationsGroup.
Dessutom skapar det här kommandot en tagg med namnet Audience och värdet PartnerOrganizations och är tilldelat till namn området.
Då visas namn området när du filtrerar objekt där mål grupps koden är inställd på PartnerOrganizations.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger visnings namnet på det data Center som ska vara värd för namn området.
Även om du kan ange den här parametern till vilken plats som helst, för optimal prestanda kan du använda ett Data Center nära de flesta av dina användare.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namnrymd
Anger namnet på det nya namn området.
Med namn utrymmen kan du gruppera och kategorisera meddelande nav.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Anger den resurs grupp som namn området ska tilldelas till.
Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och administration.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
SKU-nivån i namn området

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.
Funktionen Taggar liknar nyckelord och fungerar i en distribution.
Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.

En enskild tagg består av två delar: *namnet* och, om du vill, *värdet*.
I avdelning: det är alltså namnet avdelning och taggnamnet det.
Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


