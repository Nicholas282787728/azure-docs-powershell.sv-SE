---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkJob.md
ms.openlocfilehash: 6af36401c8b1ebd4a059493ae7afd70c5e9b4dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271189"
---
# <span data-ttu-id="3c6b4-101">Get-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3c6b4-101">Get-AzSynapseSparkJob</span></span>

## <span data-ttu-id="3c6b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6b4-103">Får ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-103">Gets a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="3c6b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c6b4-104">SYNTAX</span></span>

### <span data-ttu-id="3c6b4-105">GetSparkJobsByIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3c6b4-105">GetSparkJobsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c6b4-106">GetSparkJobsByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c6b4-106">GetSparkJobsByIdFromParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c6b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c6b4-107">DESCRIPTION</span></span>
<span data-ttu-id="3c6b4-108">Cmdleten **Get-AzSynapseSparkJob** får ett Azure Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-108">The **Get-AzSynapseSparkJob** cmdlet gets an Azure Synapse Analytics Spark job.</span></span>
<span data-ttu-id="3c6b4-109">Om du inte anger något jobb får denna cmdlet alla jobb.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="3c6b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c6b4-110">EXAMPLES</span></span>

### <span data-ttu-id="3c6b4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3c6b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="3c6b4-112">Det här kommandot får alla jobb under en spark-pool.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-112">This command gets all jobs under a Spark pool.</span></span>

### <span data-ttu-id="3c6b4-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3c6b4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 119
```

<span data-ttu-id="3c6b4-114">Det här kommandot får jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-114">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="3c6b4-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3c6b4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -ApplicationId application_1585023543211_0004
```

<span data-ttu-id="3c6b4-116">Det här kommandot får jobbet med angivet program-ID.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-116">This command gets the job with the specified application ID.</span></span>

### <span data-ttu-id="3c6b4-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3c6b4-117">Example 4</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkJob
```

<span data-ttu-id="3c6b4-118">Det här kommandot får alla jobb under en spark-pool genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-118">This command gets all jobs under a Spark pool through pipeline.</span></span>

## <span data-ttu-id="3c6b4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c6b4-119">PARAMETERS</span></span>

### <span data-ttu-id="3c6b4-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3c6b4-120">-ApplicationId</span></span>
<span data-ttu-id="3c6b4-121">Programmets program identifierare.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-121">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="3c6b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6b4-122">-DefaultProfile</span></span>
<span data-ttu-id="3c6b4-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c6b4-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3c6b4-124">-LivyId</span></span>
<span data-ttu-id="3c6b4-125">Identifierare för Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-125">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b4-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c6b4-126">-Name</span></span>
<span data-ttu-id="3c6b4-127">Namn på Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-127">Name of Spark job.</span></span>

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

### <span data-ttu-id="3c6b4-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3c6b4-128">-SparkPoolName</span></span>
<span data-ttu-id="3c6b4-129">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b4-130">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3c6b4-130">-SparkPoolObject</span></span>
<span data-ttu-id="3c6b4-131">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-131">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetSparkJobsByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b4-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3c6b4-132">-WorkspaceName</span></span>
<span data-ttu-id="3c6b4-133">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkJobsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6b4-134">CommonParameters</span></span>
<span data-ttu-id="3c6b4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c6b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6b4-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c6b4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6b4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c6b4-137">INPUTS</span></span>

### <span data-ttu-id="3c6b4-138">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3c6b4-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="3c6b4-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c6b4-139">OUTPUTS</span></span>

### <span data-ttu-id="3c6b4-140">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="3c6b4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="3c6b4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c6b4-141">NOTES</span></span>

## <span data-ttu-id="3c6b4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c6b4-142">RELATED LINKS</span></span>