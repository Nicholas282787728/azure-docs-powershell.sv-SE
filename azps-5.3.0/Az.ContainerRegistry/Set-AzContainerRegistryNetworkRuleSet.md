---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524394"
---
# <span data-ttu-id="25e1c-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="25e1c-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="25e1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="25e1c-103">Skapa eller uppdatera en nätverks regel uppsättning.</span><span class="sxs-lookup"><span data-stu-id="25e1c-103">Create or update a network rule set.</span></span> <span data-ttu-id="25e1c-104">Regel uppsättningen kan endast användas för "Premium"-registret.</span><span class="sxs-lookup"><span data-stu-id="25e1c-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="25e1c-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25e1c-105">SYNTAX</span></span>

### <span data-ttu-id="25e1c-106">AddAddNetworkRuleWithoutInputObject (standard)</span><span class="sxs-lookup"><span data-stu-id="25e1c-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e1c-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="25e1c-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e1c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="25e1c-109">Skapa eller uppdatera en nätverks regel uppsättning</span><span class="sxs-lookup"><span data-stu-id="25e1c-109">Create or update a network rule set</span></span>

## <span data-ttu-id="25e1c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="25e1c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25e1c-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="25e1c-112">Skapa en ny nätverks regel uppsättning.</span><span class="sxs-lookup"><span data-stu-id="25e1c-112">Create a new network rule set.</span></span>

## <span data-ttu-id="25e1c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25e1c-113">PARAMETERS</span></span>

### <span data-ttu-id="25e1c-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="25e1c-114">-DefaultAction</span></span>
<span data-ttu-id="25e1c-115">Standard åtgärd, kan vara "Tillåt" eller "Neka"</span><span class="sxs-lookup"><span data-stu-id="25e1c-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e1c-116">-DefaultProfile</span></span>
<span data-ttu-id="25e1c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25e1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e1c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e1c-118">-InputObject</span></span>
<span data-ttu-id="25e1c-119">Inmatning PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="25e1c-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e1c-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="25e1c-120">-NetworkRule</span></span>
<span data-ttu-id="25e1c-121">Lista över nätverks regler</span><span class="sxs-lookup"><span data-stu-id="25e1c-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e1c-122">CommonParameters</span></span>
<span data-ttu-id="25e1c-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e1c-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25e1c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e1c-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25e1c-125">INPUTS</span></span>

### <span data-ttu-id="25e1c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="25e1c-126">System.String</span></span>

### <span data-ttu-id="25e1c-127">Microsoft. Azure. commands. ContainerRegistry. Models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="25e1c-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="25e1c-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25e1c-128">OUTPUTS</span></span>

### <span data-ttu-id="25e1c-129">Microsoft. Azure. commands. ContainerRegistry. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="25e1c-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="25e1c-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25e1c-130">NOTES</span></span>

## <span data-ttu-id="25e1c-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25e1c-131">RELATED LINKS</span></span>
