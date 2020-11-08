---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100693"
---
# <span data-ttu-id="e870d-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e870d-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e870d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e870d-102">SYNOPSIS</span></span>
<span data-ttu-id="e870d-103">Kontrollerar om det finns en Synapse Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e870d-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e870d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e870d-104">SYNTAX</span></span>

### <span data-ttu-id="e870d-105">TestByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e870d-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e870d-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e870d-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e870d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e870d-107">DESCRIPTION</span></span>
<span data-ttu-id="e870d-108">**Test-AzSynapseSqlPool-** cmdleten söker efter en Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e870d-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e870d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e870d-109">EXAMPLES</span></span>

### <span data-ttu-id="e870d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e870d-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e870d-111">Det här kommandot kontrollerar förekomsten av angiven SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e870d-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="e870d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e870d-112">PARAMETERS</span></span>

### <span data-ttu-id="e870d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e870d-113">-DefaultProfile</span></span>
<span data-ttu-id="e870d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e870d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e870d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e870d-115">-Name</span></span>
<span data-ttu-id="e870d-116">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="e870d-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e870d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e870d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e870d-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e870d-118">Resource group name.</span></span>

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

### <span data-ttu-id="e870d-119">-Version</span><span class="sxs-lookup"><span data-stu-id="e870d-119">-Version</span></span>
<span data-ttu-id="e870d-120">Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e870d-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e870d-121">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="e870d-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="e870d-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e870d-122">-WorkspaceName</span></span>
<span data-ttu-id="e870d-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e870d-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e870d-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e870d-124">-WorkspaceObject</span></span>
<span data-ttu-id="e870d-125">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e870d-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e870d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e870d-126">CommonParameters</span></span>
<span data-ttu-id="e870d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e870d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e870d-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e870d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e870d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e870d-129">INPUTS</span></span>

### <span data-ttu-id="e870d-130">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e870d-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e870d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e870d-131">OUTPUTS</span></span>

### <span data-ttu-id="e870d-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="e870d-132">System.Object</span></span>
## <span data-ttu-id="e870d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e870d-133">NOTES</span></span>

## <span data-ttu-id="e870d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e870d-134">RELATED LINKS</span></span>