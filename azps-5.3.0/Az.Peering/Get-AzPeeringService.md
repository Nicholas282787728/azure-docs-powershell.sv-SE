---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522369"
---
# <span data-ttu-id="3bc1d-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="3bc1d-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="3bc1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc1d-103">Få en lista över peering service-objekt för ett enda objekt.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="3bc1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bc1d-104">SYNTAX</span></span>

### <span data-ttu-id="3bc1d-105">ByResourceGroupName (standard)</span><span class="sxs-lookup"><span data-stu-id="3bc1d-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc1d-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="3bc1d-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bc1d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc1d-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bc1d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bc1d-108">DESCRIPTION</span></span>
<span data-ttu-id="3bc1d-109">Hämtar peering Services för ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="3bc1d-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="3bc1d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bc1d-110">EXAMPLES</span></span>

### <span data-ttu-id="3bc1d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3bc1d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="3bc1d-112">Hämtar en peering-tjänst för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="3bc1d-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="3bc1d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3bc1d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="3bc1d-114">Hämtar en peering-tjänst för en resurs grupp och ett namn</span><span class="sxs-lookup"><span data-stu-id="3bc1d-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="3bc1d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3bc1d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="3bc1d-116">Hämtar en peering-tjänst via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="3bc1d-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="3bc1d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bc1d-117">PARAMETERS</span></span>

### <span data-ttu-id="3bc1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc1d-118">-DefaultProfile</span></span>
<span data-ttu-id="3bc1d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc1d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bc1d-120">-Name</span></span>
<span data-ttu-id="3bc1d-121">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3bc1d-123">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bc1d-124">-ResourceId</span></span>
<span data-ttu-id="3bc1d-125">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc1d-126">CommonParameters</span></span>
<span data-ttu-id="3bc1d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc1d-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc1d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bc1d-129">INPUTS</span></span>

### <span data-ttu-id="3bc1d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc1d-130">System.String</span></span>

## <span data-ttu-id="3bc1d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bc1d-131">OUTPUTS</span></span>

### <span data-ttu-id="3bc1d-132">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="3bc1d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="3bc1d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bc1d-133">NOTES</span></span>

## <span data-ttu-id="3bc1d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bc1d-134">RELATED LINKS</span></span>
