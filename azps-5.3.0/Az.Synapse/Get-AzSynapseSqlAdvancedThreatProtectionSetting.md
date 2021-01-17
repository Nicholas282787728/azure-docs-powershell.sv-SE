---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424443"
---
# <span data-ttu-id="ae20d-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ae20d-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ae20d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae20d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae20d-103">Hämtar inställningar för avancerat skydd för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="ae20d-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="ae20d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae20d-104">SYNTAX</span></span>

### <span data-ttu-id="ae20d-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ae20d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae20d-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae20d-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae20d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae20d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae20d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae20d-108">DESCRIPTION</span></span>
<span data-ttu-id="ae20d-109">Cmdleten **Get-AzSynapseSqlAdvancedThreatProtectionSetting** får avancerade skydds inställningar för en Azure Synapse Analytics-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ae20d-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="ae20d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae20d-110">EXAMPLES</span></span>

### <span data-ttu-id="ae20d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ae20d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ae20d-112">Det här kommandot får avancerade skydds inställningar för en arbets yta med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ae20d-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ae20d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae20d-113">PARAMETERS</span></span>

### <span data-ttu-id="ae20d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae20d-114">-DefaultProfile</span></span>
<span data-ttu-id="ae20d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae20d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae20d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae20d-116">-InputObject</span></span>
<span data-ttu-id="ae20d-117">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="ae20d-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ae20d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae20d-118">-ResourceGroupName</span></span>
<span data-ttu-id="ae20d-119">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ae20d-119">Resource group name.</span></span>

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

### <span data-ttu-id="ae20d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae20d-120">-ResourceId</span></span>
<span data-ttu-id="ae20d-121">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ae20d-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="ae20d-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ae20d-122">-WorkspaceName</span></span>
<span data-ttu-id="ae20d-123">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="ae20d-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ae20d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae20d-124">CommonParameters</span></span>
<span data-ttu-id="ae20d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae20d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae20d-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae20d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae20d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae20d-127">INPUTS</span></span>

### <span data-ttu-id="ae20d-128">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae20d-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ae20d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae20d-129">OUTPUTS</span></span>

### <span data-ttu-id="ae20d-130">Microsoft. Azure. commands. Synapse. Models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="ae20d-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="ae20d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae20d-131">NOTES</span></span>

## <span data-ttu-id="ae20d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae20d-132">RELATED LINKS</span></span>
