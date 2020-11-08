---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101973"
---
# <span data-ttu-id="ad263-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="ad263-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="ad263-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad263-102">SYNOPSIS</span></span>
<span data-ttu-id="ad263-103">Uppdatera en eller flera av följande egenskaper i IoT-säkerhetslösningen: taggar, rekommendations konfiguration, användardefinierade resurser</span><span class="sxs-lookup"><span data-stu-id="ad263-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="ad263-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad263-104">SYNTAX</span></span>

### <span data-ttu-id="ad263-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ad263-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad263-106">ID</span><span class="sxs-lookup"><span data-stu-id="ad263-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad263-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad263-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad263-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad263-108">DESCRIPTION</span></span>
<span data-ttu-id="ad263-109">Update-AzIotSecuritySolution cmdlet updayes en eller flera av följande egenskaper i en specifik IoT-säkerhetslösning: taggar, rekommendations konfiguration, användardefinierade resurser.</span><span class="sxs-lookup"><span data-stu-id="ad263-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="ad263-110">Endast de angivna egenskaperna uppdateras i IoT-säkerhetslösningen.</span><span class="sxs-lookup"><span data-stu-id="ad263-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="ad263-111">IoT-säkerhetslösningen samlar in säkerhets data från IoT-enheter och IoT Hub för att förhindra och upptäcka hot.</span><span class="sxs-lookup"><span data-stu-id="ad263-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="ad263-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad263-112">EXAMPLES</span></span>

### <span data-ttu-id="ad263-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad263-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="ad263-114">Update IoT-säkerhetslösningen "mina sampel" från resurs gruppen "MyResourceGroup" med rekommendations konfiguration och användardefinierade resurser</span><span class="sxs-lookup"><span data-stu-id="ad263-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="ad263-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad263-115">PARAMETERS</span></span>

### <span data-ttu-id="ad263-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad263-116">-DefaultProfile</span></span>
<span data-ttu-id="ad263-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad263-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad263-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad263-118">-InputObject</span></span>
<span data-ttu-id="ad263-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="ad263-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad263-120">-Name</span></span>
<span data-ttu-id="ad263-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="ad263-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad263-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="ad263-123">Rekommendations konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ad263-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad263-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad263-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ad263-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad263-126">-ResourceId</span></span>
<span data-ttu-id="ad263-127">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="ad263-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ad263-128">-Tag</span></span>
<span data-ttu-id="ad263-129">Taggen.</span><span class="sxs-lookup"><span data-stu-id="ad263-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="ad263-130">-UserDefinedResource</span></span>
<span data-ttu-id="ad263-131">Användardefinierade resurser.</span><span class="sxs-lookup"><span data-stu-id="ad263-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad263-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad263-132">-Confirm</span></span>
<span data-ttu-id="ad263-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad263-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad263-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad263-134">-WhatIf</span></span>
<span data-ttu-id="ad263-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad263-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad263-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad263-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad263-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad263-137">CommonParameters</span></span>
<span data-ttu-id="ad263-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad263-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad263-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad263-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad263-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad263-140">INPUTS</span></span>

### <span data-ttu-id="ad263-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ad263-141">System.String</span></span>

### <span data-ttu-id="ad263-142">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="ad263-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="ad263-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ad263-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ad263-144">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="ad263-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="ad263-145">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="ad263-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="ad263-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad263-146">OUTPUTS</span></span>

### <span data-ttu-id="ad263-147">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="ad263-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="ad263-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad263-148">NOTES</span></span>

## <span data-ttu-id="ad263-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad263-149">RELATED LINKS</span></span>
