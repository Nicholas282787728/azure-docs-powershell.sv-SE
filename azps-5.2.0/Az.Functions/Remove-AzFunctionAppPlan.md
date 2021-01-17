---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389643"
---
# Remove-AzFunctionAppPlan

## Sammanfattning
Tar bort en program plan för en funktion.

## FRÅGESYNTAXEN

### ByName (standard)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Tar bort en program plan för en funktion.

## BESKRIVS

### Exempel 1: skaffa en Function app-plan efter namn och ta bort den.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Det här kommandot får en funktions program plan efter namn och tar bort det.

### Exempel 2: ta bort en funktion program plan efter namn.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Detta kommando tar bort en funktion program plan efter namn.

## MALLPARAMETRAR

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

### -Force
Tvingar cmdleten att ta bort programmet Function utan att behöva bekräfta.

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

### -Namn
Namnet på funktions programmet.

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

### -PassThru
Returnerar sant när kommandot fungerar.

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

### System. Boolean

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

