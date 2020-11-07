---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915849"
---
# <span data-ttu-id="efad2-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="efad2-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="efad2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="efad2-102">SYNOPSIS</span></span>
<span data-ttu-id="efad2-103">Anger egenskaperna för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="efad2-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="efad2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="efad2-104">SYNTAX</span></span>

### <span data-ttu-id="efad2-105">SetByIndividualParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="efad2-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efad2-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="efad2-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efad2-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="efad2-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efad2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="efad2-108">DESCRIPTION</span></span>
<span data-ttu-id="efad2-109">Anger alla egenskaper för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="efad2-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="efad2-110">Eftersom den ställer in alla egenskaper när du använder ett kluster objekt måste ett fullständigt giltigt indatameddelande överföras.</span><span class="sxs-lookup"><span data-stu-id="efad2-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="efad2-111">Skrivskyddade egenskaper ignoreras.</span><span class="sxs-lookup"><span data-stu-id="efad2-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="efad2-112">Endast vissa egenskaper är uppdaterings bara, som visas i parameter uppsättningarna.</span><span class="sxs-lookup"><span data-stu-id="efad2-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="efad2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="efad2-113">EXAMPLES</span></span>

### <span data-ttu-id="efad2-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="efad2-114">Example 1</span></span>
<span data-ttu-id="efad2-115">Uppdatera ett kluster med enskilda parametrar.</span><span class="sxs-lookup"><span data-stu-id="efad2-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="efad2-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="efad2-116">Example 2</span></span>
<span data-ttu-id="efad2-117">Uppdatera ett kluster med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="efad2-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="efad2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="efad2-118">PARAMETERS</span></span>

### <span data-ttu-id="efad2-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="efad2-119">-AgentCount</span></span>
<span data-ttu-id="efad2-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="efad2-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efad2-121">-DefaultProfile</span></span>
<span data-ttu-id="efad2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="efad2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efad2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efad2-123">-InputObject</span></span>
<span data-ttu-id="efad2-124">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="efad2-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="efad2-125">-Name</span></span>
<span data-ttu-id="efad2-126">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="efad2-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efad2-127">-ResourceGroupName</span></span>
<span data-ttu-id="efad2-128">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="efad2-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efad2-129">-ResourceId</span></span>
<span data-ttu-id="efad2-130">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="efad2-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="efad2-131">-SslCertificate</span></span>
<span data-ttu-id="efad2-132">SSL-certifikatets data i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="efad2-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="efad2-133">-SslCName</span></span>
<span data-ttu-id="efad2-134">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="efad2-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="efad2-135">-SslKey</span></span>
<span data-ttu-id="efad2-136">SSL-PEM.</span><span class="sxs-lookup"><span data-stu-id="efad2-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="efad2-137">-SslStatus</span></span>
<span data-ttu-id="efad2-138">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="efad2-138">SSL status.</span></span>
<span data-ttu-id="efad2-139">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="efad2-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efad2-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="efad2-140">-Confirm</span></span>
<span data-ttu-id="efad2-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="efad2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efad2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efad2-142">-WhatIf</span></span>
<span data-ttu-id="efad2-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="efad2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efad2-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="efad2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efad2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efad2-145">CommonParameters</span></span>
<span data-ttu-id="efad2-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efad2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efad2-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efad2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efad2-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="efad2-148">INPUTS</span></span>

### <span data-ttu-id="efad2-149">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="efad2-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="efad2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="efad2-150">System.String</span></span>

### <span data-ttu-id="efad2-151">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="efad2-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="efad2-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="efad2-152">OUTPUTS</span></span>

### <span data-ttu-id="efad2-153">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="efad2-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="efad2-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="efad2-154">NOTES</span></span>

## <span data-ttu-id="efad2-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="efad2-155">RELATED LINKS</span></span>
