---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416859"
---
# <span data-ttu-id="abf65-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="abf65-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="abf65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abf65-102">SYNOPSIS</span></span>
<span data-ttu-id="abf65-103">Skapar ett nytt peering service-prefix</span><span class="sxs-lookup"><span data-stu-id="abf65-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="abf65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abf65-104">SYNTAX</span></span>

### <span data-ttu-id="abf65-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="abf65-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abf65-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf65-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abf65-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abf65-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abf65-108">DESCRIPTION</span></span>
<span data-ttu-id="abf65-109">Skapar ett peering service-prefix som är associerat med ett peering service-objekt.</span><span class="sxs-lookup"><span data-stu-id="abf65-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="abf65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abf65-110">EXAMPLES</span></span>

### <span data-ttu-id="abf65-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="abf65-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="abf65-112">Skapar ett prefix från ett peering service-objekt</span><span class="sxs-lookup"><span data-stu-id="abf65-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="abf65-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="abf65-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="abf65-114">Skapar ett prefix från ett resurs-ID för peering service.</span><span class="sxs-lookup"><span data-stu-id="abf65-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="abf65-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="abf65-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="abf65-116">Skapar ett prefix från en resurs grupp för peering service och namn</span><span class="sxs-lookup"><span data-stu-id="abf65-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="abf65-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abf65-117">PARAMETERS</span></span>

### <span data-ttu-id="abf65-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abf65-118">-AsJob</span></span>
<span data-ttu-id="abf65-119">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="abf65-119">Run in the background.</span></span>

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

### <span data-ttu-id="abf65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf65-120">-DefaultProfile</span></span>
<span data-ttu-id="abf65-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="abf65-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf65-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="abf65-122">-Name</span></span>
<span data-ttu-id="abf65-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="abf65-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="abf65-124">-PeeringServiceId</span></span>
<span data-ttu-id="abf65-125">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="abf65-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="abf65-126">-PeeringServiceName</span></span>
<span data-ttu-id="abf65-127">Namn på peering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="abf65-127">The peering service name.</span></span>
<span data-ttu-id="abf65-128">Använd New-AzPeeringService cmdlet för en ny peering-tjänst eller Get-AzPeeringService för en lista.</span><span class="sxs-lookup"><span data-stu-id="abf65-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="abf65-129">-PeeringServiceObject</span></span>
<span data-ttu-id="abf65-130">Använda en Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="abf65-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="abf65-131">-Prefix</span></span>
<span data-ttu-id="abf65-132">Prefix för session IPv4</span><span class="sxs-lookup"><span data-stu-id="abf65-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf65-133">-ResourceGroupName</span></span>
<span data-ttu-id="abf65-134">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="abf65-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="abf65-135">-ServiceKey</span></span>
<span data-ttu-id="abf65-136">Det här är ett unikt GUID från din tjänste leverantör</span><span class="sxs-lookup"><span data-stu-id="abf65-136">This is a unique GUID provided by your service provider</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="abf65-137">-Confirm</span></span>
<span data-ttu-id="abf65-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="abf65-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf65-139">-WhatIf</span></span>
<span data-ttu-id="abf65-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="abf65-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf65-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="abf65-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf65-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf65-142">CommonParameters</span></span>
<span data-ttu-id="abf65-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf65-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf65-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abf65-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf65-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abf65-145">INPUTS</span></span>

### <span data-ttu-id="abf65-146">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="abf65-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="abf65-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abf65-147">OUTPUTS</span></span>

### <span data-ttu-id="abf65-148">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="abf65-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="abf65-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abf65-149">NOTES</span></span>

## <span data-ttu-id="abf65-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abf65-150">RELATED LINKS</span></span>
