---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421696"
---
# <span data-ttu-id="06106-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06106-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="06106-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06106-102">SYNOPSIS</span></span>
<span data-ttu-id="06106-103">Skapar en Azure-IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="06106-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="06106-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06106-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06106-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06106-105">DESCRIPTION</span></span>
<span data-ttu-id="06106-106">Cmdleten **New-AzIpAllocation** skapar en Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="06106-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="06106-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06106-107">EXAMPLES</span></span>

### <span data-ttu-id="06106-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06106-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="06106-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="06106-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="06106-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06106-110">PARAMETERS</span></span>

### <span data-ttu-id="06106-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06106-111">-AsJob</span></span>
<span data-ttu-id="06106-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="06106-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06106-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06106-113">-DefaultProfile</span></span>
<span data-ttu-id="06106-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06106-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06106-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06106-115">-Force</span></span>
<span data-ttu-id="06106-116">Fråga inte efter bekräftelse om du vill åsidosätta en resurs</span><span class="sxs-lookup"><span data-stu-id="06106-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="06106-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="06106-117">-IpAllocationTag</span></span>
<span data-ttu-id="06106-118">Tilldelnings flaggorna för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="06106-118">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="06106-119">-IpAllocationType</span></span>
<span data-ttu-id="06106-120">Typ av IP-tilldelning</span><span class="sxs-lookup"><span data-stu-id="06106-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="06106-121">-IpamAllocationId</span></span>
<span data-ttu-id="06106-122">IPAM-allokeringens ID för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="06106-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="06106-123">-Location</span></span>
<span data-ttu-id="06106-124">plats.</span><span class="sxs-lookup"><span data-stu-id="06106-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="06106-125">-Name</span></span>
<span data-ttu-id="06106-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="06106-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="06106-127">-Prefix</span></span>
<span data-ttu-id="06106-128">Prefixet för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="06106-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="06106-129">-PrefixLength</span></span>
<span data-ttu-id="06106-130">Prefixlängden för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="06106-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="06106-131">-PrefixType</span></span>
<span data-ttu-id="06106-132">Prefixlängden för IP-tilldelningen</span><span class="sxs-lookup"><span data-stu-id="06106-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06106-133">-ResourceGroupName</span></span>
<span data-ttu-id="06106-134">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="06106-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="06106-135">-Tag</span></span>
<span data-ttu-id="06106-136">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="06106-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06106-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06106-137">-Confirm</span></span>
<span data-ttu-id="06106-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06106-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06106-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06106-139">-WhatIf</span></span>
<span data-ttu-id="06106-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06106-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06106-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06106-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06106-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06106-142">CommonParameters</span></span>
<span data-ttu-id="06106-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06106-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06106-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06106-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06106-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06106-145">INPUTS</span></span>

### <span data-ttu-id="06106-146">System. String</span><span class="sxs-lookup"><span data-stu-id="06106-146">System.String</span></span>

### <span data-ttu-id="06106-147">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06106-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="06106-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="06106-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="06106-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06106-149">OUTPUTS</span></span>

### <span data-ttu-id="06106-150">Microsoft. Azure. commands. Networks. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="06106-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="06106-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06106-151">NOTES</span></span>

## <span data-ttu-id="06106-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06106-152">RELATED LINKS</span></span>
