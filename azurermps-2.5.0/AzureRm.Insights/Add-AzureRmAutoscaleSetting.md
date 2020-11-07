---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931438"
---
# <span data-ttu-id="a313d-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="a313d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a313d-102">SYNOPSIS</span></span>
<span data-ttu-id="a313d-103">Skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="a313d-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a313d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a313d-104">SYNTAX</span></span>

### <span data-ttu-id="a313d-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a313d-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a313d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a313d-107">DESCRIPTION</span></span>
<span data-ttu-id="a313d-108">Cmdleten **Add-AzureRmAutoscaleSetting** skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="a313d-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="a313d-109">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="a313d-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a313d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a313d-110">EXAMPLES</span></span>

### <span data-ttu-id="a313d-111">Exempel 1: skapa en autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="a313d-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="a313d-112">De två första kommandona använder New-AzureRmAutoscaleRule för att skapa två Autoskala-regler, $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="a313d-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="a313d-113">De tredje och fjärde kommandona använder New-AzureRmAutoscaleProfile för att skapa Autoskala-profiler, $Profile 1 och $Profile 2, med $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="a313d-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="a313d-114">Med kommandot slut skapas en inställning för autoskalningsinställning med hjälp av profilerna i $Profile 1 och $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="a313d-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="a313d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a313d-115">PARAMETERS</span></span>

### <span data-ttu-id="a313d-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a313d-116">-AutoscaleProfile</span></span>
<span data-ttu-id="a313d-117">Anger en lista med profiler som ska läggas till i den autoskalningsinställning eller $Null att ingen profil ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="a313d-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a313d-118">-DefaultProfile</span></span>
<span data-ttu-id="a313d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a313d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a313d-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-120">-DisableSetting</span></span>
<span data-ttu-id="a313d-121">Inaktiverar en befintlig autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="a313d-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a313d-122">-InputObject</span></span>
<span data-ttu-id="a313d-123">Fullständig specifikation av en AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="a313d-124">-Location</span></span>
<span data-ttu-id="a313d-125">Anger platsen för den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="a313d-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a313d-126">-Name</span></span>
<span data-ttu-id="a313d-127">Anger namnet på den autoskalningsinställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a313d-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-128">-Meddelande</span><span class="sxs-lookup"><span data-stu-id="a313d-128">-Notification</span></span>
<span data-ttu-id="a313d-129">Anger en lista med kommaavgränsade meddelanden.</span><span class="sxs-lookup"><span data-stu-id="a313d-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a313d-130">-ResourceGroupName</span></span>
<span data-ttu-id="a313d-131">Anger namnet på resurs gruppen för resursen som är associerad med den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="a313d-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="a313d-132">-TargetResourceId</span></span>
<span data-ttu-id="a313d-133">Anger ID för resursen till Autoskala.</span><span class="sxs-lookup"><span data-stu-id="a313d-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a313d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a313d-134">-Confirm</span></span>
<span data-ttu-id="a313d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a313d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a313d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a313d-136">-WhatIf</span></span>
<span data-ttu-id="a313d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a313d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a313d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a313d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a313d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a313d-139">CommonParameters</span></span>
<span data-ttu-id="a313d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a313d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a313d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a313d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a313d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a313d-142">INPUTS</span></span>

### <span data-ttu-id="a313d-143">Microsoft. Azure. commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="a313d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a313d-144">System.String</span></span>

### <span data-ttu-id="a313d-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a313d-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a313d-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleProfile, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a313d-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a313d-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a313d-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a313d-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a313d-148">OUTPUTS</span></span>

### <span data-ttu-id="a313d-149">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a313d-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="a313d-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a313d-150">NOTES</span></span>

## <span data-ttu-id="a313d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a313d-151">RELATED LINKS</span></span>

[<span data-ttu-id="a313d-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="a313d-153">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="a313d-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="a313d-154">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="a313d-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="a313d-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="a313d-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


