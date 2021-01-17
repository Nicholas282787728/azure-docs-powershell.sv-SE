---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424376"
---
# <span data-ttu-id="e9124-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="e9124-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="e9124-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9124-102">SYNOPSIS</span></span>
<span data-ttu-id="e9124-103">Hämtar TDE-tillståndet för en SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9124-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="e9124-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9124-104">SYNTAX</span></span>

### <span data-ttu-id="e9124-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e9124-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9124-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9124-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9124-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9124-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9124-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9124-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9124-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9124-109">DESCRIPTION</span></span>
<span data-ttu-id="e9124-110">Cmdleten **Get-AzSynapseSqlPoolTransparentDataEncryption** får statusen för transparent Data Encryption (TDE) för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9124-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e9124-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9124-111">EXAMPLES</span></span>

### <span data-ttu-id="e9124-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9124-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e9124-113">Det här kommandot får statusen för TDE för SQL-poolen med namnet ContosoSqlPool under arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e9124-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e9124-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9124-114">PARAMETERS</span></span>

### <span data-ttu-id="e9124-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9124-115">-DefaultProfile</span></span>
<span data-ttu-id="e9124-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9124-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9124-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9124-117">-InputObject</span></span>
<span data-ttu-id="e9124-118">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9124-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9124-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9124-119">-Name</span></span>
<span data-ttu-id="e9124-120">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="e9124-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e9124-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9124-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9124-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e9124-122">Resource group name.</span></span>

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

### <span data-ttu-id="e9124-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9124-123">-ResourceId</span></span>
<span data-ttu-id="e9124-124">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="e9124-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="e9124-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9124-125">-WorkspaceName</span></span>
<span data-ttu-id="e9124-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="e9124-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e9124-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9124-127">-WorkspaceObject</span></span>
<span data-ttu-id="e9124-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9124-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e9124-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9124-129">CommonParameters</span></span>
<span data-ttu-id="e9124-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9124-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9124-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9124-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9124-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9124-132">INPUTS</span></span>

### <span data-ttu-id="e9124-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9124-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e9124-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e9124-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e9124-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9124-135">OUTPUTS</span></span>

### <span data-ttu-id="e9124-136">Microsoft. Azure. commands. Synapse. Models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="e9124-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="e9124-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9124-137">NOTES</span></span>

## <span data-ttu-id="e9124-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9124-138">RELATED LINKS</span></span>
