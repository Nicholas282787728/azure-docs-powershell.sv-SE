---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258617"
---
# <span data-ttu-id="6d789-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="6d789-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="6d789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d789-102">SYNOPSIS</span></span>
<span data-ttu-id="6d789-103">Skapa eller uppdatera IoT-säkerhetslösning</span><span class="sxs-lookup"><span data-stu-id="6d789-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="6d789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d789-104">SYNTAX</span></span>

### <span data-ttu-id="6d789-105">ResourceGroupLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="6d789-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d789-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6d789-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d789-107">ID</span><span class="sxs-lookup"><span data-stu-id="6d789-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d789-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d789-108">DESCRIPTION</span></span>
<span data-ttu-id="6d789-109">Set-AzIotSecuritySolution cmdlet skapar eller uppdaterar en specifik IoT-säkerhetslösning.</span><span class="sxs-lookup"><span data-stu-id="6d789-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="6d789-110">IoT-säkerhetslösningen samlar in säkerhets data från IoT-enheter och IoT Hub för att förhindra och upptäcka hot.</span><span class="sxs-lookup"><span data-stu-id="6d789-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="6d789-111">Namnet på IoT-säkerhetslösningen bör vara identiskt med namnet på IoT-navet.</span><span class="sxs-lookup"><span data-stu-id="6d789-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="6d789-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d789-112">EXAMPLES</span></span>

### <span data-ttu-id="6d789-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6d789-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="6d789-114">Skapa ny IoT-säkerhetslösning "exempel" för IoT Hub med Resource ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (namnet på lösningen ska vara identiskt med namnet på IoT Hub)</span><span class="sxs-lookup"><span data-stu-id="6d789-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="6d789-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d789-115">PARAMETERS</span></span>

### <span data-ttu-id="6d789-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d789-116">-DefaultProfile</span></span>
<span data-ttu-id="6d789-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d789-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d789-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="6d789-118">-DisabledDataSource</span></span>
<span data-ttu-id="6d789-119">Inaktiverade data källor.</span><span class="sxs-lookup"><span data-stu-id="6d789-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6d789-120">-DisplayName</span></span>
<span data-ttu-id="6d789-121">Visnings namn.</span><span class="sxs-lookup"><span data-stu-id="6d789-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-122">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="6d789-122">-Enabled</span></span>
<span data-ttu-id="6d789-123">Status.</span><span class="sxs-lookup"><span data-stu-id="6d789-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-124">-Exportera</span><span class="sxs-lookup"><span data-stu-id="6d789-124">-Export</span></span>
<span data-ttu-id="6d789-125">Exportera data.</span><span class="sxs-lookup"><span data-stu-id="6d789-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d789-126">-InputObject</span></span>
<span data-ttu-id="6d789-127">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="6d789-127">Input Object.</span></span>

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

### <span data-ttu-id="6d789-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="6d789-128">-IotHub</span></span>
<span data-ttu-id="6d789-129">IoT-hubbar.</span><span class="sxs-lookup"><span data-stu-id="6d789-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="6d789-130">-Location</span></span>
<span data-ttu-id="6d789-131">Plats.</span><span class="sxs-lookup"><span data-stu-id="6d789-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d789-132">-Name</span></span>
<span data-ttu-id="6d789-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="6d789-133">Resource name.</span></span>

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

### <span data-ttu-id="6d789-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d789-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="6d789-135">Rekommendations konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6d789-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="6d789-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d789-136">-ResourceGroupName</span></span>
<span data-ttu-id="6d789-137">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6d789-137">Resource group name.</span></span>

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

### <span data-ttu-id="6d789-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d789-138">-ResourceId</span></span>
<span data-ttu-id="6d789-139">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="6d789-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6d789-140">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6d789-140">-Tag</span></span>
<span data-ttu-id="6d789-141">Taggen.</span><span class="sxs-lookup"><span data-stu-id="6d789-141">Tags.</span></span>

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

### <span data-ttu-id="6d789-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="6d789-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="6d789-143">Status för avaskerad IP-loggning.</span><span class="sxs-lookup"><span data-stu-id="6d789-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="6d789-144">-UserDefinedResource</span></span>
<span data-ttu-id="6d789-145">Användardefinierade resurser.</span><span class="sxs-lookup"><span data-stu-id="6d789-145">User defined resources.</span></span>

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

### <span data-ttu-id="6d789-146">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="6d789-146">-Workspace</span></span>
<span data-ttu-id="6d789-147">Arbetsyte-ID.</span><span class="sxs-lookup"><span data-stu-id="6d789-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d789-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d789-148">-Confirm</span></span>
<span data-ttu-id="6d789-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d789-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d789-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d789-150">-WhatIf</span></span>
<span data-ttu-id="6d789-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d789-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d789-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d789-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d789-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d789-153">CommonParameters</span></span>
<span data-ttu-id="6d789-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d789-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d789-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d789-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d789-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d789-156">INPUTS</span></span>

### <span data-ttu-id="6d789-157">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="6d789-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="6d789-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6d789-158">System.String</span></span>

### <span data-ttu-id="6d789-159">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6d789-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6d789-160">System. string []</span><span class="sxs-lookup"><span data-stu-id="6d789-160">System.String[]</span></span>

### <span data-ttu-id="6d789-161">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="6d789-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="6d789-162">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="6d789-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="6d789-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d789-163">OUTPUTS</span></span>

### <span data-ttu-id="6d789-164">Microsoft. Azure. commands. Security. Models. IotSecuritySolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="6d789-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="6d789-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d789-165">NOTES</span></span>

## <span data-ttu-id="6d789-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d789-166">RELATED LINKS</span></span>
