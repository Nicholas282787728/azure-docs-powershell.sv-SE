---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSparkPool.md
ms.openlocfilehash: c931bff1ba95ee1be185b5fe4dfdc2256d2cafec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269546"
---
# <span data-ttu-id="6a504-101">New-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6a504-101">New-AzSynapseSparkPool</span></span>

## <span data-ttu-id="6a504-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a504-102">SYNOPSIS</span></span>
<span data-ttu-id="6a504-103">Skapar en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="6a504-103">Creates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6a504-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a504-104">SYNTAX</span></span>

### <span data-ttu-id="6a504-105">CreateByNameAndEnableAutoScaleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6a504-105">CreateByNameAndEnableAutoScaleParameterSet (Default)</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a504-106">CreateByNameAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a504-106">CreateByNameAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a504-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a504-107">CreateByParentObjectAndEnableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeSize <String> -AutoScaleMinNodeCount <Int32> -AutoScaleMaxNodeCount <Int32> [-EnableAutoPause]
 [-AutoPauseDelayInMinute <Int32>] -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a504-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a504-108">CreateByParentObjectAndDisableAutoScaleParameterSet</span></span>
```
New-AzSynapseSparkPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -NodeCount <Int32> -NodeSize <String> [-EnableAutoPause] [-AutoPauseDelayInMinute <Int32>]
 -SparkVersion <String> [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a504-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a504-109">DESCRIPTION</span></span>
<span data-ttu-id="6a504-110">Cmdleten **New-AzSynapseSparkPool** skapar en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="6a504-110">The **New-AzSynapseSparkPool** cmdlet creates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="6a504-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a504-111">EXAMPLES</span></span>

### <span data-ttu-id="6a504-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6a504-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="6a504-113">Det här kommandot skapar en Azure Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="6a504-113">This command creates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="6a504-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6a504-114">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="6a504-115">Det här kommandot skapar en Azure Synapse Analytics Spark-pool med aktiverat Autoskala.</span><span class="sxs-lookup"><span data-stu-id="6a504-115">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled.</span></span>

### <span data-ttu-id="6a504-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6a504-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -NodeCount 3 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="6a504-117">Det här kommandot skapar en Azure Synapse Analytics Spark-pool via pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a504-117">This command creates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="6a504-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="6a504-118">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseSparkPool -Name ContosoSparkPool -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 10 -SparkVersion 2.4 -NodeSize Small
```

<span data-ttu-id="6a504-119">Det här kommandot skapar en Azure Synapse Analytics Spark-pool med aktiverat automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="6a504-119">This command creates an Azure Synapse Analytics Spark pool with auto-scale enabled through pipeline.</span></span>

## <span data-ttu-id="6a504-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a504-120">PARAMETERS</span></span>

### <span data-ttu-id="6a504-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a504-121">-AsJob</span></span>
<span data-ttu-id="6a504-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6a504-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a504-123">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="6a504-123">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="6a504-124">Antal overksamma minuter.</span><span class="sxs-lookup"><span data-stu-id="6a504-124">Number of minutes idle.</span></span> <span data-ttu-id="6a504-125">Den här parametern måste anges när Auto-paus är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6a504-125">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-126">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="6a504-126">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="6a504-127">Maximalt antal noder som ska tilldelas till den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="6a504-127">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="6a504-128">Den här parametern måste anges när Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6a504-128">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-129">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="6a504-129">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="6a504-130">Det minsta antalet noder som ska tilldelas till den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="6a504-130">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="6a504-131">Den här parametern måste anges när Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="6a504-131">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByParentObjectAndEnableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a504-132">-DefaultProfile</span></span>
<span data-ttu-id="6a504-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6a504-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a504-134">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="6a504-134">-EnableAutoPause</span></span>
<span data-ttu-id="6a504-135">Anger om Auto-paus ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="6a504-135">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="6a504-136">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="6a504-136">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="6a504-137">Konfigurations fil för miljön ("PIP Freeze"-utdata).</span><span class="sxs-lookup"><span data-stu-id="6a504-137">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="6a504-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="6a504-138">-Name</span></span>
<span data-ttu-id="6a504-139">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="6a504-139">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-140">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="6a504-140">-NodeCount</span></span>
<span data-ttu-id="6a504-141">Antalet noder som ska tilldelas i den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="6a504-141">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByNameAndDisableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-142">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="6a504-142">-NodeSize</span></span>
<span data-ttu-id="6a504-143">Antal kärnor och minne som ska användas för noder som tilldelats i den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="6a504-143">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="6a504-144">Den här parametern måste anges när Autoskala är inaktiverat</span><span class="sxs-lookup"><span data-stu-id="6a504-144">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a504-145">-ResourceGroupName</span></span>
<span data-ttu-id="6a504-146">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6a504-146">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-147">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="6a504-147">-SparkVersion</span></span>
<span data-ttu-id="6a504-148">Apache Spark-version.</span><span class="sxs-lookup"><span data-stu-id="6a504-148">Apache Spark version.</span></span>
<span data-ttu-id="6a504-149">Tillåtna värden: 2,4</span><span class="sxs-lookup"><span data-stu-id="6a504-149">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="6a504-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6a504-150">-Tag</span></span>
<span data-ttu-id="6a504-151">En sträng, en sträng ord lista med flaggor associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="6a504-151">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-152">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a504-152">-WorkspaceName</span></span>
<span data-ttu-id="6a504-153">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="6a504-153">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameAndEnableAutoScaleParameterSet, CreateByNameAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-154">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a504-154">-WorkspaceObject</span></span>
<span data-ttu-id="6a504-155">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="6a504-155">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectAndEnableAutoScaleParameterSet, CreateByParentObjectAndDisableAutoScaleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a504-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6a504-156">-Confirm</span></span>
<span data-ttu-id="6a504-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6a504-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a504-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a504-158">-WhatIf</span></span>
<span data-ttu-id="6a504-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6a504-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a504-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6a504-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a504-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a504-161">CommonParameters</span></span>
<span data-ttu-id="6a504-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a504-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a504-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a504-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a504-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a504-164">INPUTS</span></span>

### <span data-ttu-id="6a504-165">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a504-165">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6a504-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a504-166">OUTPUTS</span></span>

### <span data-ttu-id="6a504-167">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="6a504-167">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="6a504-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a504-168">NOTES</span></span>

## <span data-ttu-id="6a504-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a504-169">RELATED LINKS</span></span>
