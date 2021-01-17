---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424456"
---
# <span data-ttu-id="835b1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="835b1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="835b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="835b1-102">SYNOPSIS</span></span>
<span data-ttu-id="835b1-103">Hämtar avancerade data säkerhets principer för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="835b1-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="835b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="835b1-104">SYNTAX</span></span>

### <span data-ttu-id="835b1-105">GetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="835b1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835b1-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="835b1-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="835b1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="835b1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="835b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="835b1-108">DESCRIPTION</span></span>
<span data-ttu-id="835b1-109">Cmdleten **Get-AzSynapseSqlAdvancedDataSecurityPolicy** hämtar den avancerade data säkerhets policyn för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="835b1-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="835b1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="835b1-110">EXAMPLES</span></span>

### <span data-ttu-id="835b1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="835b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="835b1-112">Det här kommandot får avancerad data säkerhet på arbets ytan med namnet ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="835b1-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="835b1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="835b1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="835b1-114">Det här kommandot får avancerad data säkerhet på arbets ytan som heter ContosoWorkspace via pipeline.</span><span class="sxs-lookup"><span data-stu-id="835b1-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="835b1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="835b1-115">PARAMETERS</span></span>

### <span data-ttu-id="835b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835b1-116">-DefaultProfile</span></span>
<span data-ttu-id="835b1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="835b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="835b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="835b1-118">-InputObject</span></span>
<span data-ttu-id="835b1-119">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="835b1-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="835b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="835b1-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="835b1-121">Resource group name.</span></span>

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

### <span data-ttu-id="835b1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="835b1-122">-ResourceId</span></span>
<span data-ttu-id="835b1-123">Resurs-ID för Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="835b1-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="835b1-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="835b1-124">-WorkspaceName</span></span>
<span data-ttu-id="835b1-125">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="835b1-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="835b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835b1-126">CommonParameters</span></span>
<span data-ttu-id="835b1-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835b1-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="835b1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835b1-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="835b1-129">INPUTS</span></span>

### <span data-ttu-id="835b1-130">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="835b1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="835b1-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="835b1-131">OUTPUTS</span></span>

### <span data-ttu-id="835b1-132">Microsoft. Azure. commands. Synapse. Models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="835b1-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="835b1-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="835b1-133">NOTES</span></span>

## <span data-ttu-id="835b1-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="835b1-134">RELATED LINKS</span></span>
