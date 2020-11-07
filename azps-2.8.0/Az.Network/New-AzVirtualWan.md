---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919067"
---
# <span data-ttu-id="1f23a-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1f23a-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="1f23a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f23a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f23a-103">Skapar ett Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="1f23a-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="1f23a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f23a-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f23a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f23a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f23a-106">Skapar en ny Azure VirtualWAN-resurs.</span><span class="sxs-lookup"><span data-stu-id="1f23a-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="1f23a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f23a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f23a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f23a-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="1f23a-109">Ovanstående skapar en resurs grupp "testRG" i regionen "West" och ett Azure Virtual WAN med gren till filial trafik som tillåts i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="1f23a-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="1f23a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f23a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f23a-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="1f23a-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="1f23a-112">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1f23a-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="1f23a-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="1f23a-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="1f23a-114">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="1f23a-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="1f23a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f23a-115">-AsJob</span></span>
<span data-ttu-id="1f23a-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1f23a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f23a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f23a-117">-DefaultProfile</span></span>
<span data-ttu-id="1f23a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f23a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f23a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="1f23a-119">-Location</span></span>
<span data-ttu-id="1f23a-120">Platsen för VirtualWAN-resursen.</span><span class="sxs-lookup"><span data-stu-id="1f23a-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="1f23a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f23a-121">-Name</span></span>
<span data-ttu-id="1f23a-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="1f23a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f23a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f23a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f23a-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1f23a-124">The resource group name.</span></span>

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

### <span data-ttu-id="1f23a-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1f23a-125">-Tag</span></span>
<span data-ttu-id="1f23a-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="1f23a-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1f23a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f23a-127">-Confirm</span></span>
<span data-ttu-id="1f23a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f23a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f23a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f23a-129">-WhatIf</span></span>
<span data-ttu-id="1f23a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f23a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f23a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f23a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f23a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f23a-132">CommonParameters</span></span>
<span data-ttu-id="1f23a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f23a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f23a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f23a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f23a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f23a-135">INPUTS</span></span>

### <span data-ttu-id="1f23a-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="1f23a-136">None</span></span>

## <span data-ttu-id="1f23a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f23a-137">OUTPUTS</span></span>

### <span data-ttu-id="1f23a-138">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1f23a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="1f23a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f23a-139">NOTES</span></span>

## <span data-ttu-id="1f23a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f23a-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f23a-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1f23a-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="1f23a-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1f23a-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="1f23a-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="1f23a-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
