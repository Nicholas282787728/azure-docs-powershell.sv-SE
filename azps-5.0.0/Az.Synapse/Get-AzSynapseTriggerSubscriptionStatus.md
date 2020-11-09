---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerSubscriptionStatus.md
ms.openlocfilehash: b18a308b94bdb486945186c67c3a905bcb0408d3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323538"
---
# <span data-ttu-id="50733-101">Get-AzSynapseTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="50733-101">Get-AzSynapseTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="50733-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50733-102">SYNOPSIS</span></span>
<span data-ttu-id="50733-103">Hämta status för prenumerationen för händelse utlösaren till angivna externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="50733-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="50733-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50733-104">SYNTAX</span></span>

### <span data-ttu-id="50733-105">GetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="50733-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50733-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="50733-106">GetByObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50733-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="50733-107">GetByInputObject</span></span>
```
Get-AzSynapseTriggerSubscriptionStatus -InputObject <PSTriggerResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50733-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50733-108">DESCRIPTION</span></span>
<span data-ttu-id="50733-109">Cmdleten **Get-AzSynapseTriggerSubscriptionStatus** får statusen för prenumerationen för händelse utlösaren till angivna externa tjänst händelser.</span><span class="sxs-lookup"><span data-stu-id="50733-109">The **Get-AzSynapseTriggerSubscriptionStatus** cmdlet gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="50733-110">Utlösaren kan inte startas förrän den returnerade statusen är "aktive rad".</span><span class="sxs-lookup"><span data-stu-id="50733-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="50733-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50733-111">EXAMPLES</span></span>

### <span data-ttu-id="50733-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="50733-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerSubscriptionStatus -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="50733-113">Det här kommandot får statusen för subscribtion för triggern ContosoTrigger till de externa tjänst händelserna.</span><span class="sxs-lookup"><span data-stu-id="50733-113">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events.</span></span>

### <span data-ttu-id="50733-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="50733-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerSubscriptionStatus -Name ContosoTrigger
```

<span data-ttu-id="50733-115">Det här kommandot får statusen för subscribtion för utlösaren heter ContosoTrigger till de externa tjänst händelserna via pipeline.</span><span class="sxs-lookup"><span data-stu-id="50733-115">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

### <span data-ttu-id="50733-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="50733-116">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Get-AzSynapseTriggerSubscriptionStatus
```

<span data-ttu-id="50733-117">Det här kommandot får statusen för subscribtion för utlösaren heter ContosoTrigger till de externa tjänst händelserna via pipeline.</span><span class="sxs-lookup"><span data-stu-id="50733-117">This command will get the status of the subscribtion for trigger called ContosoTrigger to the external service events through pipeline.</span></span>

## <span data-ttu-id="50733-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50733-118">PARAMETERS</span></span>

### <span data-ttu-id="50733-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50733-119">-DefaultProfile</span></span>
<span data-ttu-id="50733-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50733-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50733-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50733-121">-InputObject</span></span>
<span data-ttu-id="50733-122">Utlös ande objekt.</span><span class="sxs-lookup"><span data-stu-id="50733-122">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50733-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="50733-123">-Name</span></span>
<span data-ttu-id="50733-124">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="50733-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, GetByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50733-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50733-125">-WorkspaceName</span></span>
<span data-ttu-id="50733-126">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="50733-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50733-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50733-127">-WorkspaceObject</span></span>
<span data-ttu-id="50733-128">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="50733-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50733-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50733-129">CommonParameters</span></span>
<span data-ttu-id="50733-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50733-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50733-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50733-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50733-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50733-132">INPUTS</span></span>

### <span data-ttu-id="50733-133">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="50733-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="50733-134">Microsoft. Azure. commands. Synapse. Models. PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="50733-134">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="50733-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50733-135">OUTPUTS</span></span>

### <span data-ttu-id="50733-136">Microsoft. Azure. commands. Synapse. Models. PSTriggerSubscriptionOperationStatus</span><span class="sxs-lookup"><span data-stu-id="50733-136">Microsoft.Azure.Commands.Synapse.Models.PSTriggerSubscriptionOperationStatus</span></span>

## <span data-ttu-id="50733-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50733-137">NOTES</span></span>

## <span data-ttu-id="50733-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50733-138">RELATED LINKS</span></span>
