---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411619"
---
# <span data-ttu-id="c2226-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c2226-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c2226-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2226-102">SYNOPSIS</span></span>
<span data-ttu-id="c2226-103">Kontrollerar förekomsten av en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="c2226-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c2226-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2226-104">SYNTAX</span></span>

### <span data-ttu-id="c2226-105">TestByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2226-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2226-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2226-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2226-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2226-107">DESCRIPTION</span></span>
<span data-ttu-id="c2226-108">**Test-AzSynapseSparkPool-** cmdleten söker efter förekomsten av en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="c2226-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c2226-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2226-109">EXAMPLES</span></span>

### <span data-ttu-id="c2226-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2226-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="c2226-111">Det här kommandot kontrollerar förekomsten av den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="c2226-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="c2226-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2226-112">PARAMETERS</span></span>

### <span data-ttu-id="c2226-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2226-113">-DefaultProfile</span></span>
<span data-ttu-id="c2226-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2226-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2226-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2226-115">-Name</span></span>
<span data-ttu-id="c2226-116">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="c2226-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="c2226-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2226-117">-ResourceGroupName</span></span>
<span data-ttu-id="c2226-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="c2226-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2226-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2226-119">-WorkspaceName</span></span>
<span data-ttu-id="c2226-120">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="c2226-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2226-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2226-121">-WorkspaceObject</span></span>
<span data-ttu-id="c2226-122">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2226-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2226-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2226-123">CommonParameters</span></span>
<span data-ttu-id="c2226-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2226-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2226-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2226-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2226-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2226-126">INPUTS</span></span>

### <span data-ttu-id="c2226-127">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2226-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c2226-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2226-128">OUTPUTS</span></span>

### <span data-ttu-id="c2226-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="c2226-129">System.Object</span></span>
## <span data-ttu-id="c2226-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2226-130">NOTES</span></span>

## <span data-ttu-id="c2226-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2226-131">RELATED LINKS</span></span>
