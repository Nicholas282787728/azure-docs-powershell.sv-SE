---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745934"
---
# <span data-ttu-id="14a4a-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="14a4a-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="14a4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14a4a-102">SYNOPSIS</span></span>
<span data-ttu-id="14a4a-103">Uppdaterar eller skapar Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="14a4a-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="14a4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14a4a-104">SYNTAX</span></span>

### <span data-ttu-id="14a4a-105">InputObjectRgExcludeParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="14a4a-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14a4a-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="14a4a-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14a4a-107">DESCRIPTION</span></span>
<span data-ttu-id="14a4a-108">Används för att uppdatera konfigurationen av Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="14a4a-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="14a4a-109">Två typer av konfiguration finns: konfiguration av prenumerations nivå och ResourceGroup nivå.</span><span class="sxs-lookup"><span data-stu-id="14a4a-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="14a4a-110">Prenumerations nivå konfiguration: det kan bara finnas en konfiguration för den här typen för ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="14a4a-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="14a4a-111">LowCpuThreshold och exkludera egenskaper kan uppdateras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a4a-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="14a4a-112">Konfiguration av ResourceGroup nivå: det kan bara finnas en konfiguration för varje ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="14a4a-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="14a4a-113">Det går bara att uppdatera egenskapen exclude med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a4a-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="14a4a-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14a4a-114">EXAMPLES</span></span>

###  <span data-ttu-id="14a4a-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14a4a-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14a4a-116">Uppdaterar konfigurationen (lowCpuThreshold) för konfiguration av prenumerations nivå.</span><span class="sxs-lookup"><span data-stu-id="14a4a-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="14a4a-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="14a4a-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14a4a-118">Uppdaterar konfigurationen (lowCpuThreshold, exkludera) för konfiguration av prenumerations nivå och exkluderar från den generationens rekommendation.</span><span class="sxs-lookup"><span data-stu-id="14a4a-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="14a4a-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="14a4a-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14a4a-120">Uppdaterar konfigurationen (exkludera) för resourceGroupName1 som ska uteslutas i den uppgenererade rekommendationen.</span><span class="sxs-lookup"><span data-stu-id="14a4a-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="14a4a-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="14a4a-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14a4a-122">Uppdaterar konfigurationen för den angivna rekommendationen som skickas från pipelinen.</span><span class="sxs-lookup"><span data-stu-id="14a4a-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="14a4a-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14a4a-123">PARAMETERS</span></span>

### <span data-ttu-id="14a4a-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14a4a-124">-Confirm</span></span>
<span data-ttu-id="14a4a-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a4a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a4a-126">-DefaultProfile</span></span>
<span data-ttu-id="14a4a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14a4a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-128">-Exkludera</span><span class="sxs-lookup"><span data-stu-id="14a4a-128">-Exclude</span></span>
<span data-ttu-id="14a4a-129">Exkludera från den generationens rekommendation.</span><span class="sxs-lookup"><span data-stu-id="14a4a-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="14a4a-130">Om ej angiven exkluderings egenskap kommer att vara falskt.</span><span class="sxs-lookup"><span data-stu-id="14a4a-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a4a-131">-InputObject</span></span>
<span data-ttu-id="14a4a-132">PowerShell-objekttypen PsAzureAdvisorConfigurationData returneras av Get-AzAdvisorConfiguration-samtal.</span><span class="sxs-lookup"><span data-stu-id="14a4a-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="14a4a-133">-LowCpuThreshold</span></span>
<span data-ttu-id="14a4a-134">Värde för tröskelvärdet för lågt processor.</span><span class="sxs-lookup"><span data-stu-id="14a4a-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a4a-135">-ResourceGroupName</span></span>
<span data-ttu-id="14a4a-136">Resurs grupp namn för konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="14a4a-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a4a-137">-WhatIf</span></span>
<span data-ttu-id="14a4a-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14a4a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a4a-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14a4a-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a4a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a4a-140">CommonParameters</span></span>
<span data-ttu-id="14a4a-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a4a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14a4a-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a4a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a4a-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14a4a-143">INPUTS</span></span>

### <span data-ttu-id="14a4a-144">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="14a4a-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="14a4a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14a4a-145">OUTPUTS</span></span>

### <span data-ttu-id="14a4a-146">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="14a4a-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="14a4a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14a4a-147">NOTES</span></span>

## <span data-ttu-id="14a4a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14a4a-148">RELATED LINKS</span></span>
