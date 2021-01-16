---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394816"
---
# <span data-ttu-id="85aa8-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="85aa8-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="85aa8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="85aa8-103">Startar en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="85aa8-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="85aa8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85aa8-104">SYNTAX</span></span>

### <span data-ttu-id="85aa8-105">CreateByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85aa8-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85aa8-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85aa8-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85aa8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="85aa8-108">Cmdleten **Start-AzSynapseSparkSession** startar en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="85aa8-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="85aa8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85aa8-109">EXAMPLES</span></span>

### <span data-ttu-id="85aa8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85aa8-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="85aa8-111">Det här kommandot startar en Azure Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="85aa8-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="85aa8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="85aa8-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="85aa8-113">Det här kommandot startar en Azure Synapse Analytics Spark-session genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="85aa8-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="85aa8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85aa8-114">PARAMETERS</span></span>

### <span data-ttu-id="85aa8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85aa8-115">-AsJob</span></span>
<span data-ttu-id="85aa8-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="85aa8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85aa8-117">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="85aa8-117">-Configuration</span></span>
<span data-ttu-id="85aa8-118">Egenskaper för Spark-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="85aa8-118">Spark configuration properties.</span></span>

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

### <span data-ttu-id="85aa8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85aa8-119">-DefaultProfile</span></span>
<span data-ttu-id="85aa8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85aa8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85aa8-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="85aa8-121">-ExecutorCount</span></span>
<span data-ttu-id="85aa8-122">Antal exekverare som ska tilldelas i den angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="85aa8-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="85aa8-123">-ExecutorSize</span></span>
<span data-ttu-id="85aa8-124">Antal kärnor och minne som ska användas för utförare som tilldelats till det angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="85aa8-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

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

### <span data-ttu-id="85aa8-125">-Språk</span><span class="sxs-lookup"><span data-stu-id="85aa8-125">-Language</span></span>
<span data-ttu-id="85aa8-126">Språk för körnings koden.</span><span class="sxs-lookup"><span data-stu-id="85aa8-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="85aa8-127">-Name</span></span>
<span data-ttu-id="85aa8-128">Namn på Spark-session.</span><span class="sxs-lookup"><span data-stu-id="85aa8-128">Name of Spark session.</span></span>

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

### <span data-ttu-id="85aa8-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="85aa8-129">-ReferenceFile</span></span>
<span data-ttu-id="85aa8-130">Ytterligare filer som används för referens i huvud definitions filen.</span><span class="sxs-lookup"><span data-stu-id="85aa8-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="85aa8-131">Lista med kommaavgränsade lagrings-URI.</span><span class="sxs-lookup"><span data-stu-id="85aa8-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="85aa8-132">till exempel " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="85aa8-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="85aa8-133">-SparkPoolName</span></span>
<span data-ttu-id="85aa8-134">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="85aa8-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="85aa8-135">-SparkPoolObject</span></span>
<span data-ttu-id="85aa8-136">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="85aa8-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85aa8-137">-WorkspaceName</span></span>
<span data-ttu-id="85aa8-138">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="85aa8-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85aa8-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="85aa8-139">-Confirm</span></span>
<span data-ttu-id="85aa8-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="85aa8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85aa8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85aa8-141">-WhatIf</span></span>
<span data-ttu-id="85aa8-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="85aa8-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85aa8-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="85aa8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85aa8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85aa8-144">CommonParameters</span></span>
<span data-ttu-id="85aa8-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85aa8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85aa8-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85aa8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85aa8-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85aa8-147">INPUTS</span></span>

### <span data-ttu-id="85aa8-148">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="85aa8-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="85aa8-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85aa8-149">OUTPUTS</span></span>

### <span data-ttu-id="85aa8-150">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="85aa8-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="85aa8-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85aa8-151">NOTES</span></span>

## <span data-ttu-id="85aa8-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85aa8-152">RELATED LINKS</span></span>
