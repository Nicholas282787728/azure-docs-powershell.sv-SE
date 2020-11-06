---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571435"
---
# <span data-ttu-id="b5f67-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b5f67-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b5f67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5f67-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f67-103">Skapar en ny tjänsten het under en tjänst i en tjänst sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="b5f67-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="b5f67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5f67-104">SYNTAX</span></span>

### <span data-ttu-id="b5f67-105">ByTopologyAndServiceNames (standard)</span><span class="sxs-lookup"><span data-stu-id="b5f67-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5f67-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b5f67-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f67-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b5f67-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f67-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="b5f67-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5f67-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f67-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f67-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5f67-110">DESCRIPTION</span></span>
<span data-ttu-id="b5f67-111">Cmdleten **New-AzureRmDeploymentManagerServiceUnit** skapar en tjänst under en tjänst i en tjänst sto pol Ogin och returnerar ett objekt som representerar den tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="b5f67-112">Ange tjänst enheten utifrån dess namn, tjänst namn, topologi för tjänsten och resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b5f67-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="b5f67-113">Cmdleten returnerar ett ServiceUnit-objekt.</span><span class="sxs-lookup"><span data-stu-id="b5f67-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="b5f67-114">Du kan ändra det här objektet lokalt och sedan tillämpa ändringarna på tjänsten genom att använda Set-AzureRmDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5f67-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="b5f67-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5f67-115">EXAMPLES</span></span>

### <span data-ttu-id="b5f67-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b5f67-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="b5f67-117">Denna cmdlet skapar en ny tjänsten het med namnet ContosoService2Storage i ContosoResourceGroup under tjänsten ContosoService2 i topologi ContosoServiceTopology, i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="b5f67-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b5f67-118">Mall-och mallparametrar-filerna är definierade som relativa sökvägar till den artefakt käll plats som refereras i ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="b5f67-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="b5f67-119">De resurser som definierats i den här mallen ska distribueras till mål resurs gruppen service2ResourceGroup med distributions läget inställt på inkrementellt.</span><span class="sxs-lookup"><span data-stu-id="b5f67-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="b5f67-120">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b5f67-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="b5f67-121">Denna cmdlet skapar en ny tjänsten het med namnet ContosoService2Storage i ContosoResourceGroup under tjänsten ContosoService2 i topologi ContosoServiceTopology, i plats centralen.</span><span class="sxs-lookup"><span data-stu-id="b5f67-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="b5f67-122">Mall-och parameter referenser tillhandahålls som SAS URI: er eftersom artefakt källans ResourceId inte tillhandahölls i ContosoServiceTopology1.</span><span class="sxs-lookup"><span data-stu-id="b5f67-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="b5f67-123">De resurser som definierats i den här mallen ska distribueras till mål resurs gruppen service2ResourceGroup med distributions läget inställt på Complete.</span><span class="sxs-lookup"><span data-stu-id="b5f67-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="b5f67-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5f67-124">PARAMETERS</span></span>

### <span data-ttu-id="b5f67-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5f67-125">-AsJob</span></span>
<span data-ttu-id="b5f67-126">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b5f67-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5f67-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f67-127">-DefaultProfile</span></span>
<span data-ttu-id="b5f67-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5f67-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5f67-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="b5f67-129">-DeploymentMode</span></span>
<span data-ttu-id="b5f67-130">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b5f67-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="b5f67-131">-Location</span></span>
<span data-ttu-id="b5f67-132">Platsen för tjänst enhets resursen.</span><span class="sxs-lookup"><span data-stu-id="b5f67-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="b5f67-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="b5f67-133">-Name</span></span>
<span data-ttu-id="b5f67-134">Namnet på tjänste enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="b5f67-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b5f67-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="b5f67-136">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b5f67-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="b5f67-137">-ParametersUri</span></span>
<span data-ttu-id="b5f67-138">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b5f67-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f67-139">-ResourceGroupName</span></span>
<span data-ttu-id="b5f67-140">Resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b5f67-140">The resource group.</span></span>

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

### <span data-ttu-id="b5f67-141">-Service</span><span class="sxs-lookup"><span data-stu-id="b5f67-141">-Service</span></span>
<span data-ttu-id="b5f67-142">Serviceobjektet där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5f67-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b5f67-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b5f67-143">-ServiceName</span></span>
<span data-ttu-id="b5f67-144">Namnet på tjänsten denna tjänst enhet är en del av.</span><span class="sxs-lookup"><span data-stu-id="b5f67-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="b5f67-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f67-145">-ServiceResourceId</span></span>
<span data-ttu-id="b5f67-146">ID för tjänste resursen där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5f67-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b5f67-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b5f67-147">-ServiceTopology</span></span>
<span data-ttu-id="b5f67-148">Det tjänst Topology-objekt där tjänste enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5f67-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b5f67-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b5f67-149">-ServiceTopologyName</span></span>
<span data-ttu-id="b5f67-150">Namnet på den serivce-topologi som den här tjänst enheten är en del av.</span><span class="sxs-lookup"><span data-stu-id="b5f67-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="b5f67-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b5f67-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b5f67-152">Resurs-ID för tjänste topologi där tjänst enheten ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b5f67-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b5f67-153">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b5f67-153">-Tag</span></span>
<span data-ttu-id="b5f67-154">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b5f67-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b5f67-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b5f67-155">-TargetResourceGroup</span></span>
<span data-ttu-id="b5f67-156">Bestämmer platsen där resurserna under tjänst enheten ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="b5f67-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="b5f67-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="b5f67-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="b5f67-158">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b5f67-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b5f67-159">-TemplateUri</span></span>
<span data-ttu-id="b5f67-160">Distributions läge som ska användas vid distribution av resurserna i tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="b5f67-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5f67-161">-Confirm</span></span>
<span data-ttu-id="b5f67-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5f67-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f67-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f67-163">-WhatIf</span></span>
<span data-ttu-id="b5f67-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5f67-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f67-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5f67-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f67-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f67-166">CommonParameters</span></span>
<span data-ttu-id="b5f67-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f67-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f67-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f67-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f67-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5f67-169">INPUTS</span></span>

### <span data-ttu-id="b5f67-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="b5f67-170">None</span></span>

## <span data-ttu-id="b5f67-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5f67-171">OUTPUTS</span></span>

### <span data-ttu-id="b5f67-172">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="b5f67-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b5f67-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5f67-173">NOTES</span></span>

## <span data-ttu-id="b5f67-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5f67-174">RELATED LINKS</span></span>

[<span data-ttu-id="b5f67-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b5f67-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b5f67-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b5f67-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b5f67-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b5f67-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)