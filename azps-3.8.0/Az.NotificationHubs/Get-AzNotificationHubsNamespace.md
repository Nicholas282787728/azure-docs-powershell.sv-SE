---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 93ee8ceb15d3c07942f87c0187f4b04b8ac4aaa5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413310"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Hämtar information om namnområdet för ett meddelandehubben.

## SYNTAX

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Get-AzNotificationHubsNamespace** hämtar information om namnområden för meddelandehubben.
Med den här cmdleten kan du välja att hämta information för alla dina namnområden, information om namnområden som tilldelats en angiven resursgrupp. eller för att returnera information om ett visst namnområde.
Namnområden är logiska behållare som hjälper dig att organisera och hantera dina meddelandehubben.
Du måste ha minst ett namnområde för meddelandehubben: alla meddelandehubben måste tilldelas till ett namnområde.
Ett enda namnområde kan ha flera nav, vilket innebär att du kanske bara behöver ett namnområde i organisationen.
Men du kan också ha flera namnområden för att ordna dina nav bättre, eller ge specifika personer behörighet att hantera en markerad delmängd nav.
Cmdleten **Get-AzNotificationHubsNamespace** returnerar grundläggande information om själva namnområdet.
Om du vill ha information om auktoriseringsregler som är kopplade till ett namnområde använder du Hämta-AzNotificationHubsNamespaceAuthorizationRules.

## EXEMPEL

### Exempel 1: Hämta information för alla namnområden för meddelandehubben
```
PS C:\>Get-AzNotificationHubsNamespace
```

Med det här kommandot returneras information för alla namnområden i meddelandehubben.

### Exempel 2: Hämta information för ett enda meddelandehubbens namnområde
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Det här kommandot hämtar information för ett enda meddelandehubbens namnområde: ContosoNamespace.

### Exempel 3: Hämta information för alla meddelandehubben som är tilldelade till ett visst namnområde
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Det här kommandot hämtar information för alla namnområden för meddelandehubben som tilldelats resursgruppen ContosoNotificationsGroup.

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
Anger ett unikt namn för namnområdet.
Namnområden är ett sätt att gruppera och kategorisera meddelandehubben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

Required: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ANTECKNINGAR

## RELATERADE LÄNKAR


[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


