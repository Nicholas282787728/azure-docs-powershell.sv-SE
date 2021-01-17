---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkStatement.md
ms.openlocfilehash: a553f5e1e6b4929997cbd850ca199e6fd7acef08
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424475"
---
# <span data-ttu-id="08e9e-101">Get-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="08e9e-101">Get-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="08e9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="08e9e-103">Hämtar en Synapse Analytics Spark-programsats.</span><span class="sxs-lookup"><span data-stu-id="08e9e-103">Gets a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="08e9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08e9e-104">SYNTAX</span></span>

### <span data-ttu-id="08e9e-105">GetSparkStatementsByIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="08e9e-105">GetSparkStatementsByIdParameterSet (Default)</span></span>
```
Get-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> [-LivyId <Int32>]
 -SessionId <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e9e-106">GetSparkStatementsByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08e9e-106">GetSparkStatementsByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> [-LivyId <Int32>] [-SessionId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e9e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08e9e-107">DESCRIPTION</span></span>
<span data-ttu-id="08e9e-108">Cmdleten **Get-AzSynapseSparkStatement** hämtar information om ett Azure Synapse Analytics Spark-uttryck.</span><span class="sxs-lookup"><span data-stu-id="08e9e-108">The **Get-AzSynapseSparkStatement** cmdlet gets information about an Azure Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="08e9e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08e9e-109">EXAMPLES</span></span>

### <span data-ttu-id="08e9e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08e9e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120
```

<span data-ttu-id="08e9e-111">Det här kommandot får alla Spark-instruktioner under en spark-session.</span><span class="sxs-lookup"><span data-stu-id="08e9e-111">This command gets all the Spark statements under a Spark session.</span></span>

### <span data-ttu-id="08e9e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="08e9e-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 120 -LivyId 0
```

<span data-ttu-id="08e9e-113">Det här kommandot får Spark-instruktionen med angivet livy-ID.</span><span class="sxs-lookup"><span data-stu-id="08e9e-113">This command gets the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="08e9e-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="08e9e-114">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 107
PS C:\> $session | Get-AzSynapseSparkStatement
```

<span data-ttu-id="08e9e-115">Det här kommandot får alla Spark-instruktioner under en spark-session genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="08e9e-115">This command gets all the Spark statements under a Spark session through pipeline.</span></span>

## <span data-ttu-id="08e9e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08e9e-116">PARAMETERS</span></span>

### <span data-ttu-id="08e9e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e9e-117">-DefaultProfile</span></span>
<span data-ttu-id="08e9e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08e9e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e9e-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="08e9e-119">-LivyId</span></span>
<span data-ttu-id="08e9e-120">Identifierare för Spark-instruktionen.</span><span class="sxs-lookup"><span data-stu-id="08e9e-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="08e9e-121">-SessionId</span><span class="sxs-lookup"><span data-stu-id="08e9e-121">-SessionId</span></span>
<span data-ttu-id="08e9e-122">Identifierare för Spark-session.</span><span class="sxs-lookup"><span data-stu-id="08e9e-122">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e9e-123">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="08e9e-123">-SessionObject</span></span>
<span data-ttu-id="08e9e-124">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="08e9e-124">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: GetSparkStatementsByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08e9e-125">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="08e9e-125">-SparkPoolName</span></span>
<span data-ttu-id="08e9e-126">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="08e9e-126">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e9e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="08e9e-127">-WorkspaceName</span></span>
<span data-ttu-id="08e9e-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="08e9e-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSparkStatementsByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e9e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e9e-129">CommonParameters</span></span>
<span data-ttu-id="08e9e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e9e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e9e-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08e9e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e9e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08e9e-132">INPUTS</span></span>

### <span data-ttu-id="08e9e-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="08e9e-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="08e9e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08e9e-134">OUTPUTS</span></span>

### <span data-ttu-id="08e9e-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="08e9e-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkStatement</span></span>

## <span data-ttu-id="08e9e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08e9e-136">NOTES</span></span>

## <span data-ttu-id="08e9e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08e9e-137">RELATED LINKS</span></span>
