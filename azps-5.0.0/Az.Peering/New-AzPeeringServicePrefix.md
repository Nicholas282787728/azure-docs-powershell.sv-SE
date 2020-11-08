---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271465"
---
# <span data-ttu-id="67799-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="67799-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="67799-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67799-102">SYNOPSIS</span></span>
<span data-ttu-id="67799-103">Skapar ett nytt peering service-prefix</span><span class="sxs-lookup"><span data-stu-id="67799-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="67799-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67799-104">SYNTAX</span></span>

### <span data-ttu-id="67799-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="67799-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67799-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67799-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67799-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67799-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67799-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67799-108">DESCRIPTION</span></span>
<span data-ttu-id="67799-109">Skapar ett peering service-prefix som är associerat med ett peering service-objekt.</span><span class="sxs-lookup"><span data-stu-id="67799-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="67799-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67799-110">EXAMPLES</span></span>

### <span data-ttu-id="67799-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67799-111">Example 1</span></span>
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

<span data-ttu-id="67799-112">Skapar ett prefix från ett peering service-objekt</span><span class="sxs-lookup"><span data-stu-id="67799-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="67799-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="67799-113">Example 2</span></span>
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

<span data-ttu-id="67799-114">Skapar ett prefix från ett resurs-ID för peering service.</span><span class="sxs-lookup"><span data-stu-id="67799-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="67799-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="67799-115">Example 3</span></span>
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

<span data-ttu-id="67799-116">Skapar ett prefix från en resurs grupp för peering service och namn</span><span class="sxs-lookup"><span data-stu-id="67799-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="67799-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67799-117">PARAMETERS</span></span>

### <span data-ttu-id="67799-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67799-118">-AsJob</span></span>
<span data-ttu-id="67799-119">Kör i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="67799-119">Run in the background.</span></span>

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

### <span data-ttu-id="67799-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67799-120">-DefaultProfile</span></span>
<span data-ttu-id="67799-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67799-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67799-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="67799-122">-Name</span></span>
<span data-ttu-id="67799-123">Det unika namnet på PSPeering.</span><span class="sxs-lookup"><span data-stu-id="67799-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="67799-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="67799-124">-PeeringServiceId</span></span>
<span data-ttu-id="67799-125">Namn på resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="67799-125">The resource id string name.</span></span>

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

### <span data-ttu-id="67799-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="67799-126">-PeeringServiceName</span></span>
<span data-ttu-id="67799-127">Namn på peering-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="67799-127">The peering service name.</span></span>
<span data-ttu-id="67799-128">Använd New-AzPeeringService cmdlet för en ny peering-tjänst eller Get-AzPeeringService för en lista.</span><span class="sxs-lookup"><span data-stu-id="67799-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="67799-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="67799-129">-PeeringServiceObject</span></span>
<span data-ttu-id="67799-130">Använda en Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="67799-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="67799-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="67799-131">-Prefix</span></span>
<span data-ttu-id="67799-132">Prefix för session IPv4</span><span class="sxs-lookup"><span data-stu-id="67799-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="67799-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67799-133">-ResourceGroupName</span></span>
<span data-ttu-id="67799-134">Skapa eller Använd ett befintligt resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="67799-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="67799-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="67799-135">-ServiceKey</span></span>
<span data-ttu-id="67799-136">Det här är ett unikt GUID från din tjänste leverantör</span><span class="sxs-lookup"><span data-stu-id="67799-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="67799-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67799-137">-Confirm</span></span>
<span data-ttu-id="67799-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67799-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67799-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67799-139">-WhatIf</span></span>
<span data-ttu-id="67799-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67799-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67799-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67799-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67799-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67799-142">CommonParameters</span></span>
<span data-ttu-id="67799-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67799-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67799-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67799-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67799-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67799-145">INPUTS</span></span>

### <span data-ttu-id="67799-146">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="67799-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="67799-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67799-147">OUTPUTS</span></span>

### <span data-ttu-id="67799-148">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="67799-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="67799-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67799-149">NOTES</span></span>

## <span data-ttu-id="67799-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67799-150">RELATED LINKS</span></span>
