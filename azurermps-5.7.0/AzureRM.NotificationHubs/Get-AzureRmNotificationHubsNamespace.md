---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 996904a68e8cb55aa4964a6c776064722c63dbab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577118"
---
# Get-AzureRmNotificationHubsNamespace

## Sammanfattning
Hämtar information om ett namn område för aviseringar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmNotificationHubsNamespace** hämtar information om namn rymder för aviseringar.
Med den här cmdleten kan du hämta information för alla dina namn områden, information om de namn områden som har tilldelats till en viss resurs grupp; eller för att returnera information om ett specifikt namn område.

Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.
Du måste ha minst en namnrymd för aviserings navet: alla aviserings NAV måste kopplas till ett namn område.
Ett enda namn område kan House flera nav, vilket innebär att du kanske bara behöver ett namn område i organisationen.
Men du kan också ha flera namn områden för att bättre organisera dina nav, eller ge specifika enskilda personer tillstånd att hantera en viss delmängd av NAV.

Cmdleten **Get-AzureRmNotificationHubsNamespace** returnerar grundläggande information om själva namn området.
Om du vill ha information om de auktoriseringsregler som är associerade med ett namn område använder du get-AzureRmNotificationHubsNamespaceAuthorizationRules.

## BESKRIVS

### Exempel 1: Hämta information för alla namn områden för aviseringar
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

Det här kommandot returnerar information för alla dina namn områden i meddelande navet.

### Exempel 2: Hämta information om ett namn område för en enskild avisering
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Det här kommandot får information om ett namn område för en enskild aviserings hubb: ContosoNamespace.

### Exempel 3: Hämta information om alla aviserings nav som har tilldelats till ett visst namn område
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Med det här kommandot får du information för alla namn rymder för aviseringar som tilldelats resurs gruppen ContosoNotificationsGroup.

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

### -Namnrymd
Anger ett unikt namn för namn området.

Med namn utrymmen kan du gruppera och kategorisera meddelande nav.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Anger den resurs grupp som namn området tilldelats till.

Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


