---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94262874"
---
# <span data-ttu-id="a5e3a-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="a5e3a-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="a5e3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e3a-103">Kontrollerar förekomsten av en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a5e3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5e3a-104">SYNTAX</span></span>

### <span data-ttu-id="a5e3a-105">TestByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5e3a-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5e3a-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e3a-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e3a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="a5e3a-108">**Test-AzSynapseSparkPool-** cmdleten söker efter förekomsten av en Synapse Analytics Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="a5e3a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="a5e3a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5e3a-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="a5e3a-111">Det här kommandot kontrollerar förekomsten av den angivna Spark-poolen.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="a5e3a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="a5e3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e3a-113">-DefaultProfile</span></span>
<span data-ttu-id="a5e3a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e3a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5e3a-115">-Name</span></span>
<span data-ttu-id="a5e3a-116">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="a5e3a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e3a-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5e3a-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-118">Resource group name.</span></span>

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

### <span data-ttu-id="a5e3a-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5e3a-119">-WorkspaceName</span></span>
<span data-ttu-id="a5e3a-120">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5e3a-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5e3a-121">-WorkspaceObject</span></span>
<span data-ttu-id="a5e3a-122">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5e3a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e3a-123">CommonParameters</span></span>
<span data-ttu-id="a5e3a-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e3a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e3a-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e3a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e3a-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5e3a-126">INPUTS</span></span>

### <span data-ttu-id="a5e3a-127">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5e3a-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a5e3a-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5e3a-128">OUTPUTS</span></span>

### <span data-ttu-id="a5e3a-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="a5e3a-129">System.Object</span></span>
## <span data-ttu-id="a5e3a-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5e3a-130">NOTES</span></span>

## <span data-ttu-id="a5e3a-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5e3a-131">RELATED LINKS</span></span>
