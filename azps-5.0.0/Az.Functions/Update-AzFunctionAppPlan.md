---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263130"
---
# Update-AzFunctionAppPlan

## Sammanfattning
Uppdaterar en tjänste plan för en funktion.

## FRÅGESYNTAXEN

### ByName (standard)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Uppdaterar en tjänste plan för en funktion.

## BESKRIVS

### Exempel 1: uppdatera en app service-plan till EP2 SKU med 20 högsta arbets kraft.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Det här kommandot uppdaterar en app service-plan till EP2 SKU med högst tjugo anställda.

## MALLPARAMETRAR

### -AsJob
Kör kommandot som ett jobb.

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

### -InputObject
För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
Maximalt antal arbetare för App Service-abonnemanget.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
Det minsta antalet arbetare för App Service-abonnemanget.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Namn på App Service-abonnemanget.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nowait
Kör kommandot asynkront.

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
Namnet på den resurs grupp som resursen tillhör.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Abonnemangs-SKU.
Giltiga indata är: EP1, EP2, EP3

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tagg
Resource-taggar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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

### Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan

## VÄRDEN

### Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Resurs plats.
  - `[Kind <String>]`: Typ av resurs.
  - `[Tag <IResourceTags>]`: Resursfiler.
    - `[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[Capacity <Int32?>]`: Aktuellt antal instanser tilldelade till resursen.
  - `[FreeOfferExpirationTime <DateTime?>]`: Den tid då gratis erbjudandet från Server gruppen upphör.
  - `[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.
  - `[HyperV <Boolean?>]`: Om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.
  - `[IsSpot <Boolean?>]`: Om <code>true</code> den här app service-planen äger plats instanser.
  - `[IsXenon <Boolean?>]`: Överflödig: om programmet för Hyper-V-programtjänsten <code>true</code> , <code>false</code> annars.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maximalt antal arbetare som är tillåtna för denna ElasticScaleEnabled App Service-plan
  - `[PerSiteScaling <Boolean?>]`: Om <code>true</code> program som tilldelats den här app service-planen kan skalas oberoende av varandra.         Om <code>false</code> program som tilldelats den här app service-planen anpassas till alla instanser av planen.
  - `[Reserved <Boolean?>]`: Om programmet Linux app service <code>true</code> är på <code>false</code> annat sätt.
  - `[SkuCapability <ICapability[]>]`: Med SKU, till exempel, är Traffic Manager aktiverat?
    - `[Name <String>]`: SKU-funktionens namn.
    - `[Reason <String>]`: Orsaken till SKU-funktionen.
    - `[Value <String>]`: Värdet på SKU-funktionen.
  - `[SkuCapacityDefault <Int32?>]`: Standard antal arbetare för den här app service-abonnemanget.
  - `[SkuCapacityMaximum <Int32?>]`: Det högsta antalet arbetare för den här app service-abonnemanget.
  - `[SkuCapacityMinimum <Int32?>]`: Lägsta antal arbetare för den här app service-abonnemanget.
  - `[SkuCapacityScaleType <String>]`: Tillgängliga skal konfiguration för en app service-plan.
  - `[SkuFamily <String>]`: Familje kod för resurs-SKU.
  - `[SkuLocation <String[]>]`: Lager platsens platser.
  - `[SkuName <String>]`: Resurs-SKU-namnet.
  - `[SkuSize <String>]`: Ange storlek för resurs-SKU.
  - `[SkuTier <String>]`: Tjänst nivå för resurs-SKU.
  - `[SpotExpirationTime <DateTime?>]`: Tiden då Server gruppen upphör att gälla. Endast giltig om det är en plats Server grupp.
  - `[TargetWorkerCount <Int32?>]`: Skala antalet arbets tagare.
  - `[TargetWorkerSizeId <Int32?>]`: Skala arbetarens storleks-ID.
  - `[WorkerTierName <String>]`: Mål jobb nivå som tilldelats App Service-abonnemanget.

## RELATERADE LÄNKAR

