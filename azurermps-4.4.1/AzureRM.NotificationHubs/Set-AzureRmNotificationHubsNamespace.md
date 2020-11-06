---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 90fbdc94c372cbe02aaecde4ff27ad28dcec8e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575930"
---
# Set-AzureRmNotificationHubsNamespace

## Sammanfattning
Anger egenskaps värden för ett namn område i en aviserings hubb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tags] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmNotificationHubsNamespace** anger egenskaps värden för ett namn område för en befintlig avisering.

Namn utrymmen är logiska behållare som hjälper dig att organisera och hantera dina meddelande nav.
Du måste ha minst ett namn område för aviserings navet.
Dessutom måste alla aviserings nav ha ett tilldelat namn område.

Denna cmdlet används främst för att aktivera och inaktivera ett namn område.
När ett namn område är inaktiverat kan användare inte ansluta till något av meddelandets nav i namn området, eller administratörer kan inte använda de hubbarna för att skicka push-meddelanden.
Om du vill återaktivera ett inaktiverat namn område kan du använda denna cmdlet för att ange egenskapen **State** för namn området till aktiv.

Du kan också använda denna cmdlet för att tagga ett namn område som kritiskt.
Detta förhindrar att namn området raderas.
Om du vill ta bort ett kritiskt namn område måste du först ta bort den kritiska taggen.

## BESKRIVS

### Exempel 1: inaktivera ett namn område
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Det här kommandot inaktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till ContosoNotificationsGroup-resurs gruppen.

### Exempel 2: aktivera ett namn område
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Det här kommandot aktiverar namn området som heter ContosoPartners i det amerikanska data centret och tilldelat till resurs gruppen ContosoNotificationsGroup.

## MALLPARAMETRAR

### -Kritiskt
Anger om namn området är ett kritiskt namn område.
Kritiska namn områden kan inte tas bort.
Om du vill ta bort ett kritiskt namn område måste du ange värdet för den här egenskapen till falskt för att markera namn området som icke-kritiskt.

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

### -Force
Fråga inte efter bekräftelse.

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
Anger visnings namnet på det data Center som är värd för namn området.
Även om du kan ange den här parametern till valfri giltig Azure-plats bör du använda ett Data Center nära de flesta av dina användare.

Kör följande kommando för att få en aktuell lista över Azure-platser:

`Get-AzureLocation | Select-Object DisplayName`

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

### -Namnrymd
Anger den namnrymd som denna cmdlet ändrar.

Med namn utrymmen kan du gruppera och kategorisera meddelande nav.

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
Anger den resurs grupp som namn området tilldelats till.

Resurs grupper organiserar objekt som namn områden, aviserings nav och auktoriseringsregler på olika sätt som underlättar lager hantering och Azure-administrationen.

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
SKU-nivån i namn området

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

### -State
Anger namn områdets aktuella status.
De acceptabla värdena för denna parameter är: Active och disabled.

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

### -Taggar
Anger namn värde par som kan användas för att kategorisera och ordna Azure-objekt.
Funktionen Taggar liknar nyckelord och fungerar i en distribution.
Om du till exempel söker efter alla objekt med tagg avdelningen: då returnerar Sök alla de Azure-objekt som har den taggen, oavsett objekt typ, plats eller resurs grupp.

En enskild tagg består av två delar: *namnet* och (valfritt) *värdet*.
I till exempel avdelning: den är namnet avdelning och taggnamnet det.
Om du vill lägga till en tagg använder du syntax för hash-tabell som liknar den, som skapar taggen CalendarYear: 2016:

-Taggar @ {Name = "CalendarYear"; Värde = "2016"}

Om du vill lägga till flera taggar i samma kommando avgränsar du de enskilda taggarna genom att använda kommatecken:

-Tag @ {Name = "CalendarYear"; Värde = "2016"}; @ {name = "räkenskapsåret"; Värde = "2017"}

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
Visar vad som händer om cmdleten körs. Cmdleten körs inte.

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

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. Azure. commands. NotificationHubs. Models. NamespaceAttributes

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)


