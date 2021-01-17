---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 8199b14cf7b41eb99bb17f1692e762a07e127f26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424419"
---
# <span data-ttu-id="a4747-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a4747-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a4747-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4747-102">SYNOPSIS</span></span>
<span data-ttu-id="a4747-103">Hämtar en Synapse för SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a4747-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4747-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4747-104">SYNTAX</span></span>

### <span data-ttu-id="a4747-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a4747-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4747-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4747-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4747-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4747-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4747-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4747-108">DESCRIPTION</span></span>
<span data-ttu-id="a4747-109">Cmdleten **Get-AzSynapseSqlPool** hämtar information om en Azure Synapse-BA SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a4747-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4747-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4747-110">EXAMPLES</span></span>

### <span data-ttu-id="a4747-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4747-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a4747-112">Det här kommandot får alla SQL-pooler under en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="a4747-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="a4747-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a4747-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a4747-114">Det här kommandot får SQL-poolen under arbets ytans ContosoWorkspace med namnet ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="a4747-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="a4747-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a4747-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="a4747-116">Det här kommandot får alla SQL-pooler under en arbets yta genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a4747-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="a4747-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a4747-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="a4747-118">Det här kommandot får SQL-poolen med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a4747-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="a4747-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4747-119">PARAMETERS</span></span>

### <span data-ttu-id="a4747-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4747-120">-DefaultProfile</span></span>
<span data-ttu-id="a4747-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4747-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4747-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4747-122">-Name</span></span>
<span data-ttu-id="a4747-123">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4747-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4747-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4747-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a4747-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4747-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4747-126">-ResourceId</span></span>
<span data-ttu-id="a4747-127">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a4747-127">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4747-128">-Version</span><span class="sxs-lookup"><span data-stu-id="a4747-128">-Version</span></span>
<span data-ttu-id="a4747-129">[Den här funktionen är endast tillgänglig för vissa prenumerationer från början.] Version av Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="a4747-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="a4747-130">Till exempel 2 eller 3.</span><span class="sxs-lookup"><span data-stu-id="a4747-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="a4747-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4747-131">-WorkspaceName</span></span>
<span data-ttu-id="a4747-132">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="a4747-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4747-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a4747-133">-WorkspaceObject</span></span>
<span data-ttu-id="a4747-134">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a4747-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4747-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4747-135">CommonParameters</span></span>
<span data-ttu-id="a4747-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4747-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4747-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4747-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4747-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4747-138">INPUTS</span></span>

### <span data-ttu-id="a4747-139">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4747-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a4747-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4747-140">OUTPUTS</span></span>

### <span data-ttu-id="a4747-141">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a4747-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a4747-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4747-142">NOTES</span></span>

## <span data-ttu-id="a4747-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4747-143">RELATED LINKS</span></span>
