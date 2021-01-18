---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/remove-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Remove-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 1c740134cb2613a8efcd950fec4cd780f4f443cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520880"
---
# Remove-AzDigitalTwinsEndpoint

## Sammanfattning
Ta bort en DigitalTwinsInstance slut punkt.

## FRÅGESYNTAXEN

### Ta bort (standard)
```
Remove-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### DeleteViaIdentity
```
Remove-AzDigitalTwinsEndpoint -InputObject <IDigitalTwinsIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Ta bort en DigitalTwinsInstance slut punkt.

## BESKRIVS

### Exempel 1: ta bort azDigitalTwinsEndPoint med EndPointName
```powershell
PS C:\> Remove-AzDigitalTwinsEndpoint -ResourceGroupName youritemp -EndpointName youriEHEndpoint -ResourceName youriDigitalTwinsTest

```

Ta bort azDigitalTwinsEndPoint via EndPointName ResourceGroupName och ResourceName

### Exempel 2: ta bort azDigitalTwinsEndPoint efter objekt
```powershell
PS C:\> $GetAzdigitalTwinsEndpoint = Get-AzDigitalTwinsEndpoint -EndpointName youriEHEndpoint -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest
Remove-AzDigitalTwinsEndpoint -InputObject $GetAzdigitalTwinsEndpoint

```

Ta bort azDigitalTwinsEndPoint efter objekt

## MALLPARAMETRAR

### -AsJob
Köra kommandot som ett jobb

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

### -EndpointName
Namn på slut punkts resurs.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nowait
Kör kommandot asynkront

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

### -PassThru
Returnerar true när kommandot lyckas

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

### -ResourceGroupName
Namnet på resurs gruppen som innehåller DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Namnet på DigitalTwinsInstance.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Prenumerations-ID.

```yaml
Type: System.String
Parameter Sets: Delete
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

### Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. IDigitalTwinsIdentity

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. Api20201031. IDigitalTwinsEndpointResource

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <IDigitalTwinsIdentity> : identitets parameter
  - `[EndpointName <String>]`: Slut punkts resursens namn.
  - `[Id <String>]`: Sökväg till resurs identitet
  - `[Location <String>]`: Plats för DigitalTwinsInstance.
  - `[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller DigitalTwinsInstance.
  - `[ResourceName <String>]`: Namnet på DigitalTwinsInstance.
  - `[SubscriptionId <String>]`: Prenumerationens ID.

## RELATERADE LÄNKAR

