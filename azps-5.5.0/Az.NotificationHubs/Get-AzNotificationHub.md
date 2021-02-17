---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227334"
---
# Get-AzNotificationHub

## SYNOPSIS
Hämtar information om dina aviseringshubben.

## SYNTAX

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzNotificationHub** hämtar information om meddelandehubben i ett angivet namnområde och tilldelas till en angiven resursgrupp.
Du kan till exempel få information för alla meddelandehubben i namnområdet ContosoNamespace och tilldelad till resursgruppen ContosoNotificationsGroup.
Alternativt kan du använda Parametern *NotificationHub för* att begränsa data som returneras till information om ett visst meddelandenav.
Meddelandehubben används för att skicka push-meddelanden till flera klienter oavsett plattform, till exempel iOS, Android, Windows Phone 8 och Windows Store, som används av dessa klienter.
Dessa nav motsvarar på ungefär samma sätt enskilda appar och var och en av dina appar har vanligtvis ett eget meddelandenav.
Den här cmdleten hämtar endast information om själva navet.
Andra cmdlets, till exempel Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys och Get-AzNotificationHubPNSCredentials, behövs för att få information om ett navs auktoriseringsregler, anslutningssträngar och autentiseringsuppgifter för plattformsmeddelanden.

## EXEMPEL

### Exempel 1: Hämta information för alla meddelandehubben i ett specifikt namnområde
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Det här kommandot hämtar information för alla meddelandehubben i namnområdet ContosoNamespace som har tilldelats resursgruppen ContosoNotificationsGroup.

### Exempel 2

Hämtar information om dina aviseringshubben. (autogenererat)

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

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

### -Namespace
Anger det namnområde som meddelandehubben är tilldelat till.
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

### -NotificationHub
Anger namnet på meddelandehubben som cmdleten hämtar.
Meddelandehubben används för att skicka push-meddelanden till flera klienter oavsett vilken plattform som används av dessa klienter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Anger den resursgrupp som meddelandehubben är tilldelad till.
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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


