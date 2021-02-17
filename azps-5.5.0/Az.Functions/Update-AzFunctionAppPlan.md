---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234350"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Uppdaterar ett abonnemang för en funktionsapp.

## SYNTAX

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

## BESKRIVNING
Uppdaterar ett abonnemang för en funktionsapp.

## EXEMPEL

### Exempel 1: Uppdatera en apptjänstplan till EP2-SKU med 20 anställda med högst 20 anställda.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Det här kommandot uppdaterar en apptjänstplan till EP2-SKU med 20 anställda (högst 20 anställda).

## PARAMETERS

### -As Ent
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
Skapa genom att gå till avsnittet NOTES för INPUTOBJECT-egenskaper och skapa en hash-tabell.

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
Det maximala antalet anställda för apptjänstplanen.

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
Lägsta antal medarbetare för apptjänstplanen.

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

### -Name
Namnet på App Service-abonnemanget.

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

### -NoWait
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
Namn på resursgruppen som resursen tillhör.

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
Planens SKU.
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
Azure-prenumerations-ID.

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

### -Tag
Resurstaggar.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.Functions.Models.Api20190801.IAppServicePlan

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.Functions.Models.Api20190801.IAppServicePlan

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT: <IAppServicePlan> 
  - `Location <String>`: Resursplats.
  - `[Kind <String>]`: Typ av resurs.
  - `[Tag <IResourceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[Capacity <Int32?>]`: Aktuellt antal instanser som tilldelats resursen.
  - `[FreeOfferExpirationTime <DateTime?>]`: Tidpunkten då det kostnadsfria erbjudandet för servergruppen går ut.
  - `[HostingEnvironmentProfileId <String>]`: Resurs-ID för apptjänstmiljön.
  - `[HyperV <Boolean?>]`: Om hyper-V-containerappens serviceplan <code>true</code> , <code>false</code> annars.
  - `[IsSpot <Boolean?>]`Om <code>true</code> så är fallet äger det här App Service-abonnemanget platsinstanser.
  - `[IsXenon <Boolean?>]`: Inaktuellt: Om hyper-V-containerappens <code>true</code> <code>false</code> serviceplan annars.
  - `[MaximumElasticWorkerCount <Int32?>]`: Maximalt antal tillåtna medarbetare för det här serviceabonnemanget förscaleScaleEnabled
  - `[PerSiteScaling <Boolean?>]`Om <code>true</code> så är är det går att skala appar som tilldelats det här App Service-abonnemanget oberoende av varandra.         Om så är fallet skalas appar som tilldelats det här App <code>false</code> Service-abonnemanget till alla förekomster av abonnemanget.
  - `[Reserved <Boolean?>]`: Om linux apptjänstplan <code>true</code> , <code>false</code> annars.
  - `[SkuCapability <ICapability[]>]`: Funktioner för SKU:n, t.ex. är trafikhanteraren aktiverad?
    - `[Name <String>]`: Namn på SKU-funktionen.
    - `[Reason <String>]`: Orsak till SKU-funktionen.
    - `[Value <String>]`: Värdet på SKU-funktionen.
  - `[SkuCapacityDefault <Int32?>]`: Standardantalet anställda för SKU för den här App Service-planen.
  - `[SkuCapacityMaximum <Int32?>]`: Maximalt antal medarbetare för den här SKU:n för App Service-abonnemanget.
  - `[SkuCapacityMinimum <Int32?>]`: Lägsta antal medarbetare för den här SKU:n för App Service-abonnemanget.
  - `[SkuCapacityScaleType <String>]`: Tillgängliga skalkonfigurationer för ett App Service-abonnemang.
  - `[SkuFamily <String>]`: Familjekod för resurs-SKU.
  - `[SkuLocation <String[]>]`: SKU:ns platser.
  - `[SkuName <String>]`: Namn på resurs-SKU.
  - `[SkuSize <String>]`: Storleksspecificerare för resurs-SKU.
  - `[SkuTier <String>]`: Tjänstnivå på resurs-SKU:
  - `[SpotExpirationTime <DateTime?>]`: Tidpunkten då servergruppen går ut. Gäller endast om det är en spotservergrupp.
  - `[TargetWorkerCount <Int32?>]`: Skalning av antalet medarbetare.
  - `[TargetWorkerSizeId <Int32?>]`: Skalning av anställds storleks-ID.
  - `[WorkerTierName <String>]`: Nivå för målarbetare som är tilldelad till App Service-planen.

## RELATERADE LÄNKAR

