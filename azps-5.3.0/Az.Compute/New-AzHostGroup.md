---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524484"
---
# <span data-ttu-id="b064c-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="b064c-101">New-AzHostGroup</span></span>

## <span data-ttu-id="b064c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b064c-102">SYNOPSIS</span></span>
<span data-ttu-id="b064c-103">Skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="b064c-103">Creates a host group.</span></span>

## <span data-ttu-id="b064c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b064c-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b064c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b064c-105">DESCRIPTION</span></span>
<span data-ttu-id="b064c-106">Denna cmdlet skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="b064c-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="b064c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b064c-107">EXAMPLES</span></span>

### <span data-ttu-id="b064c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b064c-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="b064c-109">Det här kommandot skapar en värd grupp på den angivna platsen och zonen.</span><span class="sxs-lookup"><span data-stu-id="b064c-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="b064c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b064c-110">PARAMETERS</span></span>

### <span data-ttu-id="b064c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b064c-111">-AsJob</span></span>
<span data-ttu-id="b064c-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b064c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b064c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b064c-113">-DefaultProfile</span></span>
<span data-ttu-id="b064c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b064c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b064c-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="b064c-115">-Location</span></span>
<span data-ttu-id="b064c-116">Anger plats.</span><span class="sxs-lookup"><span data-stu-id="b064c-116">Specifies location.</span></span>

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

### <span data-ttu-id="b064c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b064c-117">-Name</span></span>
<span data-ttu-id="b064c-118">Anger namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="b064c-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="b064c-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="b064c-120">Anger antalet fel domäner som värd gruppen kan spänna med.</span><span class="sxs-lookup"><span data-stu-id="b064c-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="b064c-121">Minimivärdet är 1 och Max värdet är 3.</span><span class="sxs-lookup"><span data-stu-id="b064c-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b064c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b064c-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b064c-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b064c-124">-Tag</span></span>
<span data-ttu-id="b064c-125">Anger Taggar</span><span class="sxs-lookup"><span data-stu-id="b064c-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="b064c-126">-Zone</span></span>
<span data-ttu-id="b064c-127">Anger zoner i värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="b064c-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b064c-128">-SupportAutomaticPlacement</span><span class="sxs-lookup"><span data-stu-id="b064c-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="b064c-129">Anger om HostGroup ska aktivera automatisk placering av VM för datorer.</span><span class="sxs-lookup"><span data-stu-id="b064c-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="b064c-130">Automatisk placering innebär att dessa datorer placeras på dedikerade värdar, valda av Azure, under den dedikerade värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="b064c-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="b064c-131">Om inget anges är standardvärdet sant.</span><span class="sxs-lookup"><span data-stu-id="b064c-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="b064c-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b064c-132">-Confirm</span></span>
<span data-ttu-id="b064c-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b064c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b064c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b064c-134">-WhatIf</span></span>
<span data-ttu-id="b064c-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b064c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b064c-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b064c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b064c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b064c-137">CommonParameters</span></span>
<span data-ttu-id="b064c-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b064c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b064c-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b064c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b064c-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b064c-140">INPUTS</span></span>

### <span data-ttu-id="b064c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b064c-141">System.String</span></span>

## <span data-ttu-id="b064c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b064c-142">OUTPUTS</span></span>

### <span data-ttu-id="b064c-143">Microsoft. Azure. commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="b064c-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="b064c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b064c-144">NOTES</span></span>

## <span data-ttu-id="b064c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b064c-145">RELATED LINKS</span></span>
