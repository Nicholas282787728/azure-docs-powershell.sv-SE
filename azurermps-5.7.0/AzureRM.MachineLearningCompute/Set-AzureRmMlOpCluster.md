---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/set-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Set-AzureRmMlOpCluster.md
ms.openlocfilehash: 142dd983b00b578f47e2c1f2eebcbd0686614430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757931"
---
# <span data-ttu-id="8a873-101">Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8a873-101">Set-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="8a873-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a873-102">SYNOPSIS</span></span>
<span data-ttu-id="8a873-103">Anger egenskaperna för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="8a873-103">Sets the properties of an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a873-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a873-104">SYNTAX</span></span>

### <span data-ttu-id="8a873-105">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a873-105">SetByInputObject</span></span>
```
Set-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a873-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a873-106">SetByResourceId</span></span>
```
Set-AzureRmMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8a873-107">SetByIndividualParameters</span><span class="sxs-lookup"><span data-stu-id="8a873-107">SetByIndividualParameters</span></span>
```
Set-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8a873-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a873-108">DESCRIPTION</span></span>
<span data-ttu-id="8a873-109">Anger alla egenskaper för ett operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="8a873-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="8a873-110">Eftersom den ställer in alla egenskaper när du använder ett kluster objekt måste ett fullständigt giltigt indatameddelande överföras.</span><span class="sxs-lookup"><span data-stu-id="8a873-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="8a873-111">Skrivskyddade egenskaper ignoreras.</span><span class="sxs-lookup"><span data-stu-id="8a873-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="8a873-112">Endast vissa egenskaper är uppdaterings bara, som visas i parameter uppsättningarna.</span><span class="sxs-lookup"><span data-stu-id="8a873-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="8a873-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a873-113">EXAMPLES</span></span>

### <span data-ttu-id="8a873-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a873-114">Example 1</span></span>
<span data-ttu-id="8a873-115">Uppdatera ett kluster med enskilda parametrar.</span><span class="sxs-lookup"><span data-stu-id="8a873-115">Update a cluster using individual parameters.</span></span>
```
PS C:\> Set-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="8a873-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8a873-116">Example 2</span></span>
<span data-ttu-id="8a873-117">Uppdatera ett kluster med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="8a873-117">Update a cluster using an input object.</span></span>
```
PS C:\> $cluster = Get-AzureRmMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzureRmMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="8a873-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a873-118">PARAMETERS</span></span>

### <span data-ttu-id="8a873-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="8a873-119">-AgentCount</span></span>
<span data-ttu-id="8a873-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a873-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a873-121">-DefaultProfile</span></span>
<span data-ttu-id="8a873-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a873-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a873-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a873-123">-InputObject</span></span>
<span data-ttu-id="8a873-124">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="8a873-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a873-125">-Name</span></span>
<span data-ttu-id="8a873-126">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a873-126">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a873-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a873-128">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a873-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByIndividualParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a873-129">-ResourceId</span></span>
<span data-ttu-id="8a873-130">Azure Resource ID för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="8a873-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="8a873-131">-SslCertificate</span></span>
<span data-ttu-id="8a873-132">SSL-certifikatets data i PEM-format.</span><span class="sxs-lookup"><span data-stu-id="8a873-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="8a873-133">-SslCName</span></span>
<span data-ttu-id="8a873-134">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="8a873-134">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="8a873-135">-SslKey</span></span>
<span data-ttu-id="8a873-136">SSL-PEM.</span><span class="sxs-lookup"><span data-stu-id="8a873-136">The SSL key data in PEM format.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="8a873-137">-SslStatus</span></span>
<span data-ttu-id="8a873-138">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="8a873-138">SSL status.</span></span>
<span data-ttu-id="8a873-139">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="8a873-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: SetByInputObject, SetByResourceId, SetByIndividualParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a873-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a873-140">-Confirm</span></span>
<span data-ttu-id="8a873-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a873-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a873-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a873-142">-WhatIf</span></span>
<span data-ttu-id="8a873-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a873-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a873-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a873-144">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8a873-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a873-145">INPUTS</span></span>

### <span data-ttu-id="8a873-146">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8a873-146">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="8a873-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8a873-147">System.String</span></span>
### <span data-ttu-id="8a873-148">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8a873-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="8a873-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a873-149">OUTPUTS</span></span>

### <span data-ttu-id="8a873-150">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8a873-150">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="8a873-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a873-151">NOTES</span></span>

## <span data-ttu-id="8a873-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a873-152">RELATED LINKS</span></span>

