---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260201"
---
# <span data-ttu-id="41004-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="41004-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="41004-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="41004-102">SYNOPSIS</span></span>
<span data-ttu-id="41004-103">Stoppar en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="41004-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="41004-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="41004-104">SYNTAX</span></span>

### <span data-ttu-id="41004-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="41004-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41004-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41004-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41004-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41004-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41004-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="41004-108">DESCRIPTION</span></span>
<span data-ttu-id="41004-109">Cmdleten **Stop-AzSynapseSparkSession** stoppar en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="41004-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="41004-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="41004-110">EXAMPLES</span></span>

### <span data-ttu-id="41004-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="41004-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="41004-112">Det här kommandot stoppar en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="41004-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="41004-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="41004-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="41004-114">Det här kommandot stoppar en Synapse Analytics Spark-session genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="41004-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="41004-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="41004-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="41004-116">Det här kommandot stoppar en Synapse Analytics Spark-session genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="41004-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="41004-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="41004-117">PARAMETERS</span></span>

### <span data-ttu-id="41004-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41004-118">-AsJob</span></span>
<span data-ttu-id="41004-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="41004-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41004-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41004-120">-DefaultProfile</span></span>
<span data-ttu-id="41004-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="41004-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41004-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41004-122">-InputObject</span></span>
<span data-ttu-id="41004-123">Spark session-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="41004-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41004-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="41004-124">-LivyId</span></span>
<span data-ttu-id="41004-125">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="41004-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41004-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41004-126">-PassThru</span></span>
<span data-ttu-id="41004-127">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="41004-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="41004-128">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="41004-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="41004-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="41004-129">-SparkPoolName</span></span>
<span data-ttu-id="41004-130">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="41004-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41004-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="41004-131">-SparkPoolObject</span></span>
<span data-ttu-id="41004-132">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="41004-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41004-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="41004-133">-WorkspaceName</span></span>
<span data-ttu-id="41004-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="41004-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41004-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="41004-135">-Confirm</span></span>
<span data-ttu-id="41004-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="41004-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41004-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41004-137">-WhatIf</span></span>
<span data-ttu-id="41004-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="41004-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41004-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="41004-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41004-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41004-140">CommonParameters</span></span>
<span data-ttu-id="41004-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41004-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41004-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41004-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41004-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="41004-143">INPUTS</span></span>

### <span data-ttu-id="41004-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="41004-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="41004-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="41004-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="41004-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="41004-146">OUTPUTS</span></span>

### <span data-ttu-id="41004-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41004-147">System.Boolean</span></span>

## <span data-ttu-id="41004-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="41004-148">NOTES</span></span>

## <span data-ttu-id="41004-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="41004-149">RELATED LINKS</span></span>
