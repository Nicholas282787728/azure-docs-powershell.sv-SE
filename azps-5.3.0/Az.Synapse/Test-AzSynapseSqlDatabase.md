---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523887"
---
# <span data-ttu-id="ba880-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ba880-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="ba880-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba880-102">SYNOPSIS</span></span>
<span data-ttu-id="ba880-103">Kontrollerar om det finns en Synapse Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ba880-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ba880-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba880-104">SYNTAX</span></span>

### <span data-ttu-id="ba880-105">TestByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ba880-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba880-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba880-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba880-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba880-107">DESCRIPTION</span></span>
<span data-ttu-id="ba880-108">**Test-AzSynapseSqlDatabase-** cmdleten söker efter en SYNAPSE Analytics SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ba880-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="ba880-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba880-109">EXAMPLES</span></span>

### <span data-ttu-id="ba880-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ba880-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="ba880-111">Det här kommandot kontrollerar förekomsten av angiven SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ba880-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="ba880-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba880-112">PARAMETERS</span></span>

### <span data-ttu-id="ba880-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba880-113">-DefaultProfile</span></span>
<span data-ttu-id="ba880-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba880-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba880-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba880-115">-Name</span></span>
<span data-ttu-id="ba880-116">Namn på Synapse SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="ba880-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="ba880-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba880-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba880-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ba880-118">Resource group name.</span></span>

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

### <span data-ttu-id="ba880-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba880-119">-WorkspaceName</span></span>
<span data-ttu-id="ba880-120">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ba880-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ba880-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ba880-121">-WorkspaceObject</span></span>
<span data-ttu-id="ba880-122">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba880-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ba880-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba880-123">CommonParameters</span></span>
<span data-ttu-id="ba880-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba880-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba880-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba880-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba880-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba880-126">INPUTS</span></span>

### <span data-ttu-id="ba880-127">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba880-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ba880-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba880-128">OUTPUTS</span></span>

### <span data-ttu-id="ba880-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba880-129">System.Boolean</span></span>

## <span data-ttu-id="ba880-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba880-130">NOTES</span></span>

## <span data-ttu-id="ba880-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba880-131">RELATED LINKS</span></span>
