---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4e3b6b596f276f3d36a315354a93950524722adc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424416"
---
# <span data-ttu-id="df4d8-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="df4d8-101">Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="df4d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="df4d8-103">Hämtar inställningar för avancerat skydd för en SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="df4d8-103">Gets the advanced threat protection settings for a SQL pool.</span></span>

## <span data-ttu-id="df4d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df4d8-104">SYNTAX</span></span>

### <span data-ttu-id="df4d8-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="df4d8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4d8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4d8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4d8-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4d8-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4d8-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df4d8-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df4d8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df4d8-109">DESCRIPTION</span></span>
<span data-ttu-id="df4d8-110">Cmdleten **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** får avancerade skydds inställningar för en Azure SYNAPSE Analytics SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="df4d8-110">The **Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="df4d8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df4d8-111">EXAMPLES</span></span>

### <span data-ttu-id="df4d8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="df4d8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="df4d8-113">Det här kommandot får avancerade skydds inställningar för en SQL-pool med namnet ContosoSqlPool under arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="df4d8-113">This command gets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="df4d8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df4d8-114">PARAMETERS</span></span>

### <span data-ttu-id="df4d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4d8-115">-DefaultProfile</span></span>
<span data-ttu-id="df4d8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df4d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4d8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4d8-117">-InputObject</span></span>
<span data-ttu-id="df4d8-118">Objekt i SQL-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="df4d8-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="df4d8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="df4d8-119">-Name</span></span>
<span data-ttu-id="df4d8-120">Namn på SQL-poolen Synapse.</span><span class="sxs-lookup"><span data-stu-id="df4d8-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="df4d8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4d8-121">-ResourceGroupName</span></span>
<span data-ttu-id="df4d8-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="df4d8-122">Resource group name.</span></span>

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

### <span data-ttu-id="df4d8-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4d8-123">-ResourceId</span></span>
<span data-ttu-id="df4d8-124">Resurs-ID för Synapse SQL-pool.</span><span class="sxs-lookup"><span data-stu-id="df4d8-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="df4d8-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df4d8-125">-WorkspaceName</span></span>
<span data-ttu-id="df4d8-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="df4d8-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="df4d8-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="df4d8-127">-WorkspaceObject</span></span>
<span data-ttu-id="df4d8-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="df4d8-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="df4d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4d8-129">CommonParameters</span></span>
<span data-ttu-id="df4d8-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4d8-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df4d8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4d8-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df4d8-132">INPUTS</span></span>

### <span data-ttu-id="df4d8-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="df4d8-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="df4d8-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="df4d8-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="df4d8-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df4d8-135">OUTPUTS</span></span>

### <span data-ttu-id="df4d8-136">Microsoft. Azure. commands. Synapse. Models. PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="df4d8-136">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="df4d8-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df4d8-137">NOTES</span></span>

## <span data-ttu-id="df4d8-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df4d8-138">RELATED LINKS</span></span>
