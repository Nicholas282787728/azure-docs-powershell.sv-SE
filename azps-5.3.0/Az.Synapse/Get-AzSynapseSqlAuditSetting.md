---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424432"
---
# <span data-ttu-id="85e47-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="85e47-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="85e47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85e47-102">SYNOPSIS</span></span>
<span data-ttu-id="85e47-103">Hämtar gransknings inställningarna för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="85e47-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="85e47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85e47-104">SYNTAX</span></span>

### <span data-ttu-id="85e47-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="85e47-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85e47-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e47-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85e47-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e47-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85e47-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85e47-108">DESCRIPTION</span></span>
<span data-ttu-id="85e47-109">Cmdleten **Get-AzSynapseSqlAuditSetting** hämtar gransknings inställningarna för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="85e47-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="85e47-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85e47-110">EXAMPLES</span></span>

### <span data-ttu-id="85e47-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="85e47-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="85e47-112">Hämtar gransknings inställningarna för en arbets yta som heter ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="85e47-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="85e47-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="85e47-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="85e47-114">Hämtar gransknings inställningarna för en arbets yta som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="85e47-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="85e47-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85e47-115">PARAMETERS</span></span>

### <span data-ttu-id="85e47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e47-116">-DefaultProfile</span></span>
<span data-ttu-id="85e47-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85e47-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e47-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85e47-118">-InputObject</span></span>
<span data-ttu-id="85e47-119">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="85e47-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85e47-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e47-120">-ResourceGroupName</span></span>
<span data-ttu-id="85e47-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="85e47-121">Resource group name.</span></span>

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

### <span data-ttu-id="85e47-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85e47-122">-ResourceId</span></span>
<span data-ttu-id="85e47-123">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="85e47-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="85e47-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="85e47-124">-WorkspaceName</span></span>
<span data-ttu-id="85e47-125">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="85e47-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="85e47-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e47-126">CommonParameters</span></span>
<span data-ttu-id="85e47-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e47-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e47-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85e47-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e47-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85e47-129">INPUTS</span></span>

### <span data-ttu-id="85e47-130">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="85e47-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="85e47-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85e47-131">OUTPUTS</span></span>

### <span data-ttu-id="85e47-132">Microsoft. Azure. commands. Synapse. Models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="85e47-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="85e47-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85e47-133">NOTES</span></span>

## <span data-ttu-id="85e47-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85e47-134">RELATED LINKS</span></span>
