---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271165"
---
# <span data-ttu-id="646bd-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="646bd-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="646bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="646bd-102">SYNOPSIS</span></span>
<span data-ttu-id="646bd-103">Visar en lista över mottagna vägar för en peering.</span><span class="sxs-lookup"><span data-stu-id="646bd-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="646bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="646bd-104">SYNTAX</span></span>

### <span data-ttu-id="646bd-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="646bd-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="646bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="646bd-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="646bd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="646bd-107">DESCRIPTION</span></span>
<span data-ttu-id="646bd-108">Visar en lista över mottagna vägar från en peering</span><span class="sxs-lookup"><span data-stu-id="646bd-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="646bd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="646bd-109">EXAMPLES</span></span>

### <span data-ttu-id="646bd-110">Lista över 100 mottagna vägar för en peering</span><span class="sxs-lookup"><span data-stu-id="646bd-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="646bd-111">Visar alla mottagna vägar för en peering</span><span class="sxs-lookup"><span data-stu-id="646bd-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="646bd-112">Filtrera efter som sökväg</span><span class="sxs-lookup"><span data-stu-id="646bd-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="646bd-113">Visar en lista över alla mottagna vägar för en peering med ett filter aktiverat som</span><span class="sxs-lookup"><span data-stu-id="646bd-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="646bd-114">Filtrera efter RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="646bd-115">Visar en lista över alla mottagna vägar för en peering med ett filter på RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="646bd-116">Filtrera efter OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="646bd-117">Visar en lista över alla mottagna vägar för en peering med ett filter på OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="646bd-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="646bd-118">PARAMETERS</span></span>

### <span data-ttu-id="646bd-119">-Behållning</span><span class="sxs-lookup"><span data-stu-id="646bd-119">-AsPath</span></span>
<span data-ttu-id="646bd-120">Filtrera efter som sökväg.</span><span class="sxs-lookup"><span data-stu-id="646bd-120">Filter by AS Path.</span></span>
<span data-ttu-id="646bd-121">Exempel: ' 9342 1234 4567 '</span><span class="sxs-lookup"><span data-stu-id="646bd-121">Example: '9342 1234 4567'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="646bd-122">-DefaultProfile</span></span>
<span data-ttu-id="646bd-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="646bd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="646bd-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="646bd-124">-Name</span></span>
<span data-ttu-id="646bd-125">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="646bd-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="646bd-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-126">-OriginAsValidationState</span></span>
<span data-ttu-id="646bd-127">Filtrera efter ursprung som validerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="646bd-127">Filter by origin AS validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646bd-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="646bd-128">-Prefix</span></span>
<span data-ttu-id="646bd-129">Filtrera enligt prefix.</span><span class="sxs-lookup"><span data-stu-id="646bd-129">Filter by prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646bd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="646bd-130">-ResourceGroupName</span></span>
<span data-ttu-id="646bd-131">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="646bd-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="646bd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="646bd-132">-ResourceId</span></span>
<span data-ttu-id="646bd-133">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="646bd-133">The resource id string name.</span></span>

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

### <span data-ttu-id="646bd-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="646bd-134">-RPKIValidationState</span></span>
<span data-ttu-id="646bd-135">Filtrera efter RPKI verifierings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="646bd-135">Filter by RPKI validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="646bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="646bd-136">CommonParameters</span></span>
<span data-ttu-id="646bd-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="646bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="646bd-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="646bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="646bd-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="646bd-139">INPUTS</span></span>

### <span data-ttu-id="646bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="646bd-140">System.String</span></span>

## <span data-ttu-id="646bd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="646bd-141">OUTPUTS</span></span>

### <span data-ttu-id="646bd-142">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="646bd-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="646bd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="646bd-143">NOTES</span></span>

## <span data-ttu-id="646bd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="646bd-144">RELATED LINKS</span></span>
