---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: cbe72d14eac4864b784f31c4a800db09fc38b042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576931"
---
# <span data-ttu-id="75c17-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="75c17-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="75c17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75c17-102">SYNOPSIS</span></span>
<span data-ttu-id="75c17-103">Anger egenskaperna för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="75c17-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75c17-104">SYNTAX</span></span>

### <span data-ttu-id="75c17-105">SetByIndividualParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="75c17-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75c17-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="75c17-106">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75c17-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="75c17-107">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c17-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75c17-108">DESCRIPTION</span></span>
<span data-ttu-id="75c17-109">Anger alla egenskaper för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="75c17-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="75c17-110">Eftersom den ställer in alla egenskaper när du använder ett kluster objekt måste ett fullständigt giltigt indatameddelande överföras.</span><span class="sxs-lookup"><span data-stu-id="75c17-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="75c17-111">Skrivskyddade egenskaper ignoreras.</span><span class="sxs-lookup"><span data-stu-id="75c17-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="75c17-112">Endast vissa egenskaper är uppdaterings bara, som visas i parameter uppsättningarna.</span><span class="sxs-lookup"><span data-stu-id="75c17-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="75c17-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75c17-113">EXAMPLES</span></span>

### <span data-ttu-id="75c17-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75c17-114">Example 1</span></span>
<span data-ttu-id="75c17-115">Uppdatera ett kluster med enskilda parametrar.</span><span class="sxs-lookup"><span data-stu-id="75c17-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="75c17-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="75c17-116">Example 2</span></span>
<span data-ttu-id="75c17-117">Uppdatera ett kluster med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="75c17-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="75c17-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75c17-118">PARAMETERS</span></span>

### <span data-ttu-id="75c17-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="75c17-119">-AgentCount</span></span>
<span data-ttu-id="75c17-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="75c17-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="75c17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c17-121">-DefaultProfile</span></span>
<span data-ttu-id="75c17-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75c17-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c17-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75c17-123">-InputObject</span></span>
<span data-ttu-id="75c17-124">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="75c17-124">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="75c17-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="75c17-125">-Name</span></span>
<span data-ttu-id="75c17-126">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="75c17-126">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="75c17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c17-127">-ResourceGroupName</span></span>
<span data-ttu-id="75c17-128">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="75c17-128">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="75c17-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75c17-129">-ResourceId</span></span>
<span data-ttu-id="75c17-130">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="75c17-130">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="75c17-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="75c17-131">-SslCertificate</span></span>
<span data-ttu-id="75c17-132">SSL-certifikatets data i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="75c17-132">The SSL certificate data in PEM format.</span></span>

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

### <span data-ttu-id="75c17-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="75c17-133">-SslCName</span></span>
<span data-ttu-id="75c17-134">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="75c17-134">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="75c17-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="75c17-135">-SslKey</span></span>
<span data-ttu-id="75c17-136">SSL-PEM.</span><span class="sxs-lookup"><span data-stu-id="75c17-136">The SSL key data in PEM format.</span></span>

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

### <span data-ttu-id="75c17-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="75c17-137">-SslStatus</span></span>
<span data-ttu-id="75c17-138">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="75c17-138">SSL status.</span></span>
<span data-ttu-id="75c17-139">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="75c17-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="75c17-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75c17-140">-Confirm</span></span>
<span data-ttu-id="75c17-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75c17-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c17-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c17-142">-WhatIf</span></span>
<span data-ttu-id="75c17-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75c17-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c17-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75c17-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c17-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c17-145">CommonParameters</span></span>
<span data-ttu-id="75c17-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c17-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c17-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c17-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c17-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75c17-148">INPUTS</span></span>

### <span data-ttu-id="75c17-149">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="75c17-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="75c17-150">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="75c17-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="75c17-151">System. String</span><span class="sxs-lookup"><span data-stu-id="75c17-151">System.String</span></span>

### <span data-ttu-id="75c17-152">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="75c17-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="75c17-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75c17-153">OUTPUTS</span></span>

### <span data-ttu-id="75c17-154">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="75c17-154">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="75c17-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75c17-155">NOTES</span></span>

## <span data-ttu-id="75c17-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75c17-156">RELATED LINKS</span></span>
