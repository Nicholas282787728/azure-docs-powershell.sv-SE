---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: f83a52281cbe244e91b22300b7f10582d6ca6349
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089185"
---
# <span data-ttu-id="cfebc-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="cfebc-101">New-AzHostGroup</span></span>

## <span data-ttu-id="cfebc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfebc-102">SYNOPSIS</span></span>
<span data-ttu-id="cfebc-103">Skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="cfebc-103">Creates a host group.</span></span>

## <span data-ttu-id="cfebc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfebc-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfebc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfebc-105">DESCRIPTION</span></span>
<span data-ttu-id="cfebc-106">Denna cmdlet skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="cfebc-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="cfebc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfebc-107">EXAMPLES</span></span>

### <span data-ttu-id="cfebc-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cfebc-108">Example 1</span></span>
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

<span data-ttu-id="cfebc-109">Det här kommandot skapar en värd grupp på den angivna platsen och zonen.</span><span class="sxs-lookup"><span data-stu-id="cfebc-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="cfebc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfebc-110">PARAMETERS</span></span>

### <span data-ttu-id="cfebc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfebc-111">-AsJob</span></span>
<span data-ttu-id="cfebc-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cfebc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfebc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfebc-113">-DefaultProfile</span></span>
<span data-ttu-id="cfebc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfebc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfebc-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="cfebc-115">-Location</span></span>
<span data-ttu-id="cfebc-116">Anger plats.</span><span class="sxs-lookup"><span data-stu-id="cfebc-116">Specifies location.</span></span>

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

### <span data-ttu-id="cfebc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfebc-117">-Name</span></span>
<span data-ttu-id="cfebc-118">Anger namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfebc-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="cfebc-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="cfebc-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="cfebc-120">Anger antalet fel domäner som värd gruppen kan spänna med.</span><span class="sxs-lookup"><span data-stu-id="cfebc-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="cfebc-121">Minimivärdet är 1 och Max värdet är 3.</span><span class="sxs-lookup"><span data-stu-id="cfebc-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="cfebc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfebc-122">-ResourceGroupName</span></span>
<span data-ttu-id="cfebc-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfebc-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="cfebc-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cfebc-124">-Tag</span></span>
<span data-ttu-id="cfebc-125">Anger Taggar</span><span class="sxs-lookup"><span data-stu-id="cfebc-125">Specifies Tags</span></span>

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

### <span data-ttu-id="cfebc-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="cfebc-126">-Zone</span></span>
<span data-ttu-id="cfebc-127">Anger zoner i värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="cfebc-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="cfebc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfebc-128">-Confirm</span></span>
<span data-ttu-id="cfebc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfebc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfebc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfebc-130">-WhatIf</span></span>
<span data-ttu-id="cfebc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cfebc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfebc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cfebc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfebc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfebc-133">CommonParameters</span></span>
<span data-ttu-id="cfebc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfebc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfebc-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfebc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfebc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfebc-136">INPUTS</span></span>

### <span data-ttu-id="cfebc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cfebc-137">System.String</span></span>

## <span data-ttu-id="cfebc-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfebc-138">OUTPUTS</span></span>

### <span data-ttu-id="cfebc-139">Microsoft. Azure. commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="cfebc-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="cfebc-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfebc-140">NOTES</span></span>

## <span data-ttu-id="cfebc-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfebc-141">RELATED LINKS</span></span>
