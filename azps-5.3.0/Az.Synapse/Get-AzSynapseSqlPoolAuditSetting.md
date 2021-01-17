---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424403"
---
# <span data-ttu-id="f1b08-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f1b08-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="f1b08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1b08-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b08-103">Hämtar gransknings inställningarna för en Azure Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="f1b08-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f1b08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1b08-104">SYNTAX</span></span>

### <span data-ttu-id="f1b08-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1b08-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1b08-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1b08-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1b08-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1b08-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1b08-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1b08-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1b08-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1b08-109">DESCRIPTION</span></span>
<span data-ttu-id="f1b08-110">Cmdleten **Get-AzSynapseSqlPoolAuditSetting** hämtar gransknings inställningarna för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="f1b08-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f1b08-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1b08-111">EXAMPLES</span></span>

### <span data-ttu-id="f1b08-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f1b08-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="f1b08-113">Det här kommandot får gransknings inställningarna för en SQL-pool som heter ContosoSqlPool i arbets ytans ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f1b08-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="f1b08-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f1b08-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="f1b08-115">Det här kommandot får gransknings inställningarna för en SQL-pool som heter ContosoSqlPool i arbets ytans ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1b08-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f1b08-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1b08-116">PARAMETERS</span></span>

### <span data-ttu-id="f1b08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b08-117">-DefaultProfile</span></span>
<span data-ttu-id="f1b08-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b08-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1b08-119">-InputObject</span></span>
<span data-ttu-id="f1b08-120">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1b08-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1b08-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1b08-121">-Name</span></span>
<span data-ttu-id="f1b08-122">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="f1b08-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b08-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1b08-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f1b08-124">Resource group name.</span></span>

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

### <span data-ttu-id="f1b08-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1b08-125">-ResourceId</span></span>
<span data-ttu-id="f1b08-126">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="f1b08-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="f1b08-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1b08-127">-WorkspaceName</span></span>
<span data-ttu-id="f1b08-128">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="f1b08-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f1b08-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1b08-129">-WorkspaceObject</span></span>
<span data-ttu-id="f1b08-130">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1b08-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1b08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b08-131">CommonParameters</span></span>
<span data-ttu-id="f1b08-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b08-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1b08-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b08-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1b08-134">INPUTS</span></span>

### <span data-ttu-id="f1b08-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f1b08-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f1b08-136">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f1b08-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f1b08-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1b08-137">OUTPUTS</span></span>

### <span data-ttu-id="f1b08-138">Microsoft. Azure. commands. Synapse. Models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="f1b08-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="f1b08-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1b08-139">NOTES</span></span>

## <span data-ttu-id="f1b08-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1b08-140">RELATED LINKS</span></span>
