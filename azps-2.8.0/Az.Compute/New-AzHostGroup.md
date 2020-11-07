---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745100"
---
# <span data-ttu-id="2f462-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="2f462-101">New-AzHostGroup</span></span>

## <span data-ttu-id="2f462-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f462-102">SYNOPSIS</span></span>
<span data-ttu-id="2f462-103">Skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="2f462-103">Creates a host group.</span></span>

## <span data-ttu-id="2f462-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f462-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f462-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f462-105">DESCRIPTION</span></span>
<span data-ttu-id="2f462-106">Denna cmdlet skapar en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="2f462-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="2f462-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f462-107">EXAMPLES</span></span>

### <span data-ttu-id="2f462-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f462-108">Example 1</span></span>
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

<span data-ttu-id="2f462-109">Det här kommandot skapar en värd grupp på den angivna platsen och zonen.</span><span class="sxs-lookup"><span data-stu-id="2f462-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="2f462-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f462-110">PARAMETERS</span></span>

### <span data-ttu-id="2f462-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f462-111">-AsJob</span></span>
<span data-ttu-id="2f462-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2f462-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f462-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f462-113">-DefaultProfile</span></span>
<span data-ttu-id="2f462-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f462-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f462-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="2f462-115">-Location</span></span>
<span data-ttu-id="2f462-116">Anger plats.</span><span class="sxs-lookup"><span data-stu-id="2f462-116">Specifies location.</span></span>

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

### <span data-ttu-id="2f462-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f462-117">-Name</span></span>
<span data-ttu-id="2f462-118">Anger namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f462-118">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="2f462-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="2f462-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="2f462-120">Anger antalet fel domäner som värd gruppen kan spänna med.</span><span class="sxs-lookup"><span data-stu-id="2f462-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="2f462-121">Minimivärdet är 1 och Max värdet är 3.</span><span class="sxs-lookup"><span data-stu-id="2f462-121">The minimum value is 1 and the maximum value is 3.</span></span>

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

### <span data-ttu-id="2f462-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f462-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f462-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f462-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f462-124">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2f462-124">-Tag</span></span>
<span data-ttu-id="2f462-125">Anger Taggar</span><span class="sxs-lookup"><span data-stu-id="2f462-125">Specifies Tags</span></span>

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

### <span data-ttu-id="2f462-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="2f462-126">-Zone</span></span>
<span data-ttu-id="2f462-127">Anger zoner i värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f462-127">Specifies Zones of the host group.</span></span>

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

### <span data-ttu-id="2f462-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f462-128">-Confirm</span></span>
<span data-ttu-id="2f462-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f462-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f462-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f462-130">-WhatIf</span></span>
<span data-ttu-id="2f462-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f462-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f462-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f462-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f462-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f462-133">CommonParameters</span></span>
<span data-ttu-id="2f462-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f462-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f462-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f462-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f462-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f462-136">INPUTS</span></span>

### <span data-ttu-id="2f462-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2f462-137">System.String</span></span>

## <span data-ttu-id="2f462-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f462-138">OUTPUTS</span></span>

### <span data-ttu-id="2f462-139">Microsoft. Azure. commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="2f462-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="2f462-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f462-140">NOTES</span></span>

## <span data-ttu-id="2f462-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f462-141">RELATED LINKS</span></span>
