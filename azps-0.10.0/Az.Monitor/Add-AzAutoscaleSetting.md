---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 6efcc4ad0a957fb2e6124d9688163f08de318b70
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924406"
---
# <span data-ttu-id="9c629-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="9c629-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c629-102">SYNOPSIS</span></span>
<span data-ttu-id="9c629-103">Skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9c629-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="9c629-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c629-104">SYNTAX</span></span>

### <span data-ttu-id="9c629-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c629-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c629-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c629-107">DESCRIPTION</span></span>
<span data-ttu-id="9c629-108">Cmdleten **Add-AzAutoscaleSetting** skapar en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9c629-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="9c629-109">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="9c629-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9c629-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c629-110">EXAMPLES</span></span>

### <span data-ttu-id="9c629-111">Exempel 1: skapa en autoskalningsinställning</span><span class="sxs-lookup"><span data-stu-id="9c629-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="9c629-112">De två första kommandona använder New-AzAutoscaleRule för att skapa två Autoskala-regler, $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9c629-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9c629-113">De tredje och fjärde kommandona använder New-AzAutoscaleProfile för att skapa Autoskala-profiler, $Profile 1 och $Profile 2, med $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9c629-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="9c629-114">Med kommandot slut skapas en inställning för autoskalningsinställning med hjälp av profilerna i $Profile 1 och $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="9c629-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="9c629-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c629-115">PARAMETERS</span></span>

### <span data-ttu-id="9c629-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9c629-116">-AutoscaleProfile</span></span>
<span data-ttu-id="9c629-117">Anger en lista med profiler som ska läggas till i den autoskalningsinställning eller $Null att ingen profil ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="9c629-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="9c629-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c629-118">-DefaultProfile</span></span>
<span data-ttu-id="9c629-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9c629-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c629-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-120">-DisableSetting</span></span>
<span data-ttu-id="9c629-121">Inaktiverar en befintlig autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9c629-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="9c629-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c629-122">-InputObject</span></span>
<span data-ttu-id="9c629-123">Fullständig specifikation av en AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="9c629-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="9c629-124">-Location</span></span>
<span data-ttu-id="9c629-125">Anger platsen för den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9c629-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="9c629-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="9c629-126">-Name</span></span>
<span data-ttu-id="9c629-127">Anger namnet på den autoskalningsinställning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9c629-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="9c629-128">-Meddelande</span><span class="sxs-lookup"><span data-stu-id="9c629-128">-Notification</span></span>
<span data-ttu-id="9c629-129">Anger en lista med kommaavgränsade meddelanden.</span><span class="sxs-lookup"><span data-stu-id="9c629-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="9c629-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c629-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c629-131">Anger namnet på resurs gruppen för resursen som är associerad med den autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9c629-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="9c629-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9c629-132">-TargetResourceId</span></span>
<span data-ttu-id="9c629-133">Anger ID för resursen till Autoskala.</span><span class="sxs-lookup"><span data-stu-id="9c629-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="9c629-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c629-134">-Confirm</span></span>
<span data-ttu-id="9c629-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c629-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c629-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c629-136">-WhatIf</span></span>
<span data-ttu-id="9c629-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c629-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c629-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c629-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c629-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c629-139">CommonParameters</span></span>
<span data-ttu-id="9c629-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c629-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c629-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c629-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c629-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c629-142">INPUTS</span></span>

### <span data-ttu-id="9c629-143">Microsoft. Azure. commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="9c629-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9c629-144">System.String</span></span>

### <span data-ttu-id="9c629-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c629-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9c629-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleProfile, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c629-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9c629-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleNotification, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9c629-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9c629-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c629-148">OUTPUTS</span></span>

### <span data-ttu-id="9c629-149">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c629-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="9c629-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c629-150">NOTES</span></span>

## <span data-ttu-id="9c629-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c629-151">RELATED LINKS</span></span>

[<span data-ttu-id="9c629-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="9c629-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9c629-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="9c629-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9c629-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="9c629-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9c629-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


