---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkSession.md
ms.openlocfilehash: 587183d72c6fdeec965f1ec1aa6aa88f5d6f36f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259755"
---
# <span data-ttu-id="8ab67-101">Get-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8ab67-101">Get-AzSynapseSparkSession</span></span>

## <span data-ttu-id="8ab67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ab67-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab67-103">Får en Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="8ab67-103">Gets a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8ab67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ab67-104">SYNTAX</span></span>

### <span data-ttu-id="8ab67-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8ab67-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ab67-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab67-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-LivyId <Int32>] [-Name <String>]
 [-ApplicationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab67-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ab67-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab67-108">Cmdleten **Get-AzSynapseSparkSession** hämtar information om en Azure Synapse Analytics Spark-session.</span><span class="sxs-lookup"><span data-stu-id="8ab67-108">The **Get-AzSynapseSparkSession** cmdlet gets information about an Azure Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="8ab67-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ab67-109">EXAMPLES</span></span>

### <span data-ttu-id="8ab67-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8ab67-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
```

<span data-ttu-id="8ab67-111">Det här kommandot får alla Spark-sessioner under den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="8ab67-111">This command gets all the Spark sessions under the specified Spark pool.</span></span>

### <span data-ttu-id="8ab67-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8ab67-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 1
```

<span data-ttu-id="8ab67-113">Det här kommandot får Spark-session med angivet livy-ID.</span><span class="sxs-lookup"><span data-stu-id="8ab67-113">This command gets the Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="8ab67-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8ab67-114">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Get-AzSynapseSparkSession
```

<span data-ttu-id="8ab67-115">Det här kommandot får alla Spark-sessioner under den angivna Spark-poolen genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ab67-115">This command gets all the Spark sessions under the specified Spark pool through pipeline.</span></span>

## <span data-ttu-id="8ab67-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ab67-116">PARAMETERS</span></span>

### <span data-ttu-id="8ab67-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8ab67-117">-ApplicationId</span></span>
<span data-ttu-id="8ab67-118">Programmets program identifierare.</span><span class="sxs-lookup"><span data-stu-id="8ab67-118">The Application identifier of the session.</span></span>

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

### <span data-ttu-id="8ab67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab67-119">-DefaultProfile</span></span>
<span data-ttu-id="8ab67-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab67-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ab67-121">-LivyId</span><span class="sxs-lookup"><span data-stu-id="8ab67-121">-LivyId</span></span>
<span data-ttu-id="8ab67-122">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="8ab67-122">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="8ab67-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ab67-123">-Name</span></span>
<span data-ttu-id="8ab67-124">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="8ab67-124">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="8ab67-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8ab67-125">-SparkPoolName</span></span>
<span data-ttu-id="8ab67-126">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="8ab67-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab67-127">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="8ab67-127">-SparkPoolObject</span></span>
<span data-ttu-id="8ab67-128">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ab67-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab67-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ab67-129">-WorkspaceName</span></span>
<span data-ttu-id="8ab67-130">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="8ab67-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab67-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab67-131">CommonParameters</span></span>
<span data-ttu-id="8ab67-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab67-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab67-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ab67-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab67-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ab67-134">INPUTS</span></span>

### <span data-ttu-id="8ab67-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="8ab67-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="8ab67-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ab67-136">OUTPUTS</span></span>

### <span data-ttu-id="8ab67-137">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8ab67-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8ab67-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ab67-138">NOTES</span></span>

## <span data-ttu-id="8ab67-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ab67-139">RELATED LINKS</span></span>