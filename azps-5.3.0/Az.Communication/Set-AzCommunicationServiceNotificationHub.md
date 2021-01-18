---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524573"
---
# Set-AzCommunicationServiceNotificationHub

## Sammanfattning
Länkar en Azure Notification-hubb till den här kommunikations tjänsten.

## FRÅGESYNTAXEN

### LinkExpanded (standard)
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Länknamn
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Länkar en Azure Notification-hubb till den här kommunikations tjänsten.

## BESKRIVS

### Exempel 1: Tillhandahåll interaktivt med information om meddelandets hubb
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

Med en länkad meddelande hubb kan en ACS-resurs skicka aviseringar för vissa händelser.

## MALLPARAMETRAR

### -CommunicationServiceName
Namnet på CommunicationService-resursen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Anslutnings sträng för meddelande navet

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinkNotificationHubParameter
Beskrivning av ett Azure Notification-nav som länkar till kommunikations tjänsten för att skapa, se avsnittet anteckningar för LINKNOTIFICATIONHUBPARAMETER-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NotificationHubResourceId
Resurs-ID för meddelande navet

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Namnet på resurs gruppen som innehåller resursen.
Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Hämtar abonnemangs-ID som unikt identifierar Microsoft Azure-prenumerationen.
Prenumerations-ID: t utgör en del av URI: n för varje service samtal.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. Communication. Models. Api20200820Preview. ILinkNotificationHubParameters

## VÄRDEN

### System. String

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters> : Beskrivning av ett Azure Notification Hub som länkar till kommunikations tjänsten
  - `ConnectionString <String>`: Anslutnings sträng för meddelande navet
  - `ResourceId <String>`: Meddelande navets resurs-ID

## RELATERADE LÄNKAR

