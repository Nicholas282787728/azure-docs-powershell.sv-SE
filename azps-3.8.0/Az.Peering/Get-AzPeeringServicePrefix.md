---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: d36561e2090e5b98bed5a5051715fe3e868bde4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092206"
---
# <span data-ttu-id="3918b-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3918b-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="3918b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3918b-102">SYNOPSIS</span></span>
<span data-ttu-id="3918b-103">Hämtar en lista över peering service-prefix för en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3918b-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="3918b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3918b-104">SYNTAX</span></span>

### <span data-ttu-id="3918b-105">ByResourceGroupAndName (standard)</span><span class="sxs-lookup"><span data-stu-id="3918b-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3918b-106">Vis</span><span class="sxs-lookup"><span data-stu-id="3918b-106">Default</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3918b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3918b-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3918b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3918b-108">DESCRIPTION</span></span>
<span data-ttu-id="3918b-109">List prefix för peering service för peering service-objekt</span><span class="sxs-lookup"><span data-stu-id="3918b-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="3918b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3918b-110">EXAMPLES</span></span>

### <span data-ttu-id="3918b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3918b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="3918b-112">Hämtar prefixen för en peering-tjänst baserad på rör-kommandon.</span><span class="sxs-lookup"><span data-stu-id="3918b-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="3918b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3918b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="3918b-114">Hämtar ett specifikt prefix för en peering service efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3918b-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="3918b-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3918b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="3918b-116">Hämtar ett specifikt prefix för en peering service efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3918b-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="3918b-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3918b-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="3918b-118">Hämtar ett specifikt prefix för en peering-tjänst med utökade attribut</span><span class="sxs-lookup"><span data-stu-id="3918b-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="3918b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3918b-119">PARAMETERS</span></span>

### <span data-ttu-id="3918b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3918b-120">-DefaultProfile</span></span>
<span data-ttu-id="3918b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3918b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3918b-122">-Expandera</span><span class="sxs-lookup"><span data-stu-id="3918b-122">-Expand</span></span>
<span data-ttu-id="3918b-123">Visa händelserna för ett peering service-prefix</span><span class="sxs-lookup"><span data-stu-id="3918b-123">View the events for a peering service prefix</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3918b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="3918b-124">-Name</span></span>
<span data-ttu-id="3918b-125">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3918b-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3918b-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="3918b-126">-PeeringServiceName</span></span>
<span data-ttu-id="3918b-127">Namn på peering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3918b-127">The peering service name.</span></span> <span data-ttu-id="3918b-128">Använd New-AzPeeringService cmdlet för en ny peering-tjänst eller Get-AzPeeringService för en lista.</span><span class="sxs-lookup"><span data-stu-id="3918b-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3918b-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="3918b-129">-PeeringServiceObject</span></span>
<span data-ttu-id="3918b-130">Använda en Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="3918b-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3918b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3918b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3918b-132">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="3918b-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3918b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3918b-133">-ResourceId</span></span>
<span data-ttu-id="3918b-134">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="3918b-134">The resource id string name.</span></span>

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

### <span data-ttu-id="3918b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3918b-135">CommonParameters</span></span>
<span data-ttu-id="3918b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3918b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3918b-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3918b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3918b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3918b-138">INPUTS</span></span>

### <span data-ttu-id="3918b-139">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="3918b-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="3918b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3918b-140">System.String</span></span>

## <span data-ttu-id="3918b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3918b-141">OUTPUTS</span></span>

### <span data-ttu-id="3918b-142">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3918b-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="3918b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3918b-143">NOTES</span></span>

## <span data-ttu-id="3918b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3918b-144">RELATED LINKS</span></span>