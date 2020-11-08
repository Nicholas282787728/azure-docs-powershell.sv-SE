---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101035"
---
# <span data-ttu-id="ddead-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ddead-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="ddead-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddead-102">SYNOPSIS</span></span>
<span data-ttu-id="ddead-103">Skapar en tjänsten het under den angivna tjänst-och tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="ddead-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="ddead-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddead-104">SYNTAX</span></span>

### <span data-ttu-id="ddead-105">ByTopologyAndServiceNames (standard)</span><span class="sxs-lookup"><span data-stu-id="ddead-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddead-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ddead-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddead-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ddead-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddead-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="ddead-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddead-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ddead-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddead-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddead-110">DESCRIPTION</span></span>
<span data-ttu-id="ddead-111">Cmdleten **New-AzDeploymentManagerServiceUnit** skapar en tjänst under en tjänst i en tjänst sto pol Ogin och returnerar ett objekt som representerar den tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="ddead-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="ddead-112">Ange tjänst enheten utifrån dess namn, tjänst namn, topologi för tjänsten och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ddead-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="ddead-113">Cmdleten returnerar ett ServiceUnit-objekt.</span><span class="sxs-lookup"><span data-stu-id="ddead-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="ddead-114">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddead-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="ddead-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddead-115">EXAMPLES</span></span>

### <span data-ttu-id="ddead-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ddead-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="ddead-117">Denna cmdlet skapar en ny tjänsten het med namnet ContosoService2Storage i ContosoResourceGroup under tjänsten ContosoService2 i topologi ContosoServiceTopology, i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="ddead-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ddead-118">Mall-och mallparametrar-filerna är definierade som relativa sökvägar till den artefakt käll plats som refereras i ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="ddead-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="ddead-119">De resurser som definierats i den här mallen ska distribueras till mål resurs gruppen service2ResourceGroup med distributions läget inställt på inkrementellt.</span><span class="sxs-lookup"><span data-stu-id="ddead-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="ddead-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ddead-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="ddead-121">Denna cmdlet skapar en ny tjänsten het med namnet ContosoService2Storage i ContosoResourceGroup under tjänsten ContosoService2 i topologi ContosoServiceTopology, i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="ddead-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="ddead-122">Mall-och parameter referenser tillhandahålls som SAS URI: er eftersom artefakt källans ResourceId inte tillhandahölls i ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="ddead-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="ddead-123">De resurser som definierats i den här mallen ska distribueras till mål resurs gruppen service2ResourceGroup med distributions läget inställt på Complete.</span><span class="sxs-lookup"><span data-stu-id="ddead-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="ddead-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddead-124">PARAMETERS</span></span>

### <span data-ttu-id="ddead-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddead-125">-AsJob</span></span>
<span data-ttu-id="ddead-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ddead-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddead-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddead-127">-DefaultProfile</span></span>
<span data-ttu-id="ddead-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddead-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddead-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="ddead-129">-DeploymentMode</span></span>
<span data-ttu-id="ddead-130">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="ddead-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="ddead-131">-Location</span></span>
<span data-ttu-id="ddead-132">Platsen för tjänst enhets resursen.</span><span class="sxs-lookup"><span data-stu-id="ddead-132">The location of the service unit resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddead-133">-Name</span></span>
<span data-ttu-id="ddead-134">Namnet på tjänste enheten.</span><span class="sxs-lookup"><span data-stu-id="ddead-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ddead-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="ddead-136">Sökvägen till parameter filen i förhållande till artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="ddead-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="ddead-137">Kräver att ArtifactSource refereras i ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="ddead-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="ddead-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="ddead-138">-ParametersUri</span></span>
<span data-ttu-id="ddead-139">SAS URI till parameter filen.</span><span class="sxs-lookup"><span data-stu-id="ddead-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="ddead-140">Om ArtifactSourceId refererades i ServiceTopology anger du relativ sökväg med ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="ddead-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="ddead-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddead-141">-ResourceGroupName</span></span>
<span data-ttu-id="ddead-142">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ddead-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ddead-143">-ServiceName</span></span>
<span data-ttu-id="ddead-144">Namnet på tjänsten denna tjänst enhet är en del av.</span><span class="sxs-lookup"><span data-stu-id="ddead-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="ddead-145">-ServiceObject</span></span>
<span data-ttu-id="ddead-146">Serviceobjektet där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ddead-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ddead-147">-ServiceResourceId</span></span>
<span data-ttu-id="ddead-148">ID för tjänste resursen där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ddead-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ddead-149">-ServiceTopologyName</span></span>
<span data-ttu-id="ddead-150">Namnet på tjänst topologin som denna tjänst enhet är en del av.</span><span class="sxs-lookup"><span data-stu-id="ddead-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ddead-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="ddead-152">Det tjänst Topology-objekt där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ddead-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ddead-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ddead-154">Resurs-ID för tjänste topologi där tjänst enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ddead-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-155">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ddead-155">-Tag</span></span>
<span data-ttu-id="ddead-156">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ddead-156">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddead-157">-TargetResourceGroup</span></span>
<span data-ttu-id="ddead-158">Bestämmer platsen där resurserna under tjänst enheten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="ddead-158">Determines the location where resources under the service unit would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddead-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ddead-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="ddead-160">Sökvägen till mallfilen i förhållande till artefakt källan.</span><span class="sxs-lookup"><span data-stu-id="ddead-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="ddead-161">Kräver att ArtifactSource refereras i ServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="ddead-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="ddead-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ddead-162">-TemplateUri</span></span>
<span data-ttu-id="ddead-163">SAS URI till mallfilen.</span><span class="sxs-lookup"><span data-stu-id="ddead-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="ddead-164">Om ArtifactSourceId refererades i ServiceTopology anger du relativ sökväg med TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="ddead-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="ddead-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddead-165">-Confirm</span></span>
<span data-ttu-id="ddead-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddead-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddead-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddead-167">-WhatIf</span></span>
<span data-ttu-id="ddead-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddead-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddead-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddead-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddead-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddead-170">CommonParameters</span></span>
<span data-ttu-id="ddead-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddead-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddead-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddead-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddead-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddead-173">INPUTS</span></span>

### <span data-ttu-id="ddead-174">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ddead-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ddead-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddead-175">OUTPUTS</span></span>

### <span data-ttu-id="ddead-176">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="ddead-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ddead-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddead-177">NOTES</span></span>

## <span data-ttu-id="ddead-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddead-178">RELATED LINKS</span></span>
