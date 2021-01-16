---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421624"
---
# <span data-ttu-id="12a8c-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12a8c-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="12a8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="12a8c-103">Skapar ett Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="12a8c-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="12a8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12a8c-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12a8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12a8c-105">DESCRIPTION</span></span>
<span data-ttu-id="12a8c-106">Skapar en ny Azure VirtualWAN-resurs.</span><span class="sxs-lookup"><span data-stu-id="12a8c-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="12a8c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12a8c-107">EXAMPLES</span></span>

### <span data-ttu-id="12a8c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="12a8c-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="12a8c-109">Ovanstående skapar en resurs grupp "testRG" i regionen "West" och ett Azure Virtual WAN med gren till filial trafik som tillåts i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="12a8c-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="12a8c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12a8c-110">PARAMETERS</span></span>

### <span data-ttu-id="12a8c-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="12a8c-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="12a8c-112">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="12a8c-112">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="12a8c-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="12a8c-114">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="12a8c-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12a8c-115">-AsJob</span></span>
<span data-ttu-id="12a8c-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="12a8c-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a8c-117">-DefaultProfile</span></span>
<span data-ttu-id="12a8c-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12a8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="12a8c-119">-Location</span></span>
<span data-ttu-id="12a8c-120">Platsen för VirtualWAN-resursen.</span><span class="sxs-lookup"><span data-stu-id="12a8c-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="12a8c-121">-Name</span></span>
<span data-ttu-id="12a8c-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="12a8c-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="12a8c-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="12a8c-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="12a8c-125">-Tag</span></span>
<span data-ttu-id="12a8c-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="12a8c-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="12a8c-127">-VirtualWANType</span></span>
<span data-ttu-id="12a8c-128">Typen av virtuellt WAN.</span><span class="sxs-lookup"><span data-stu-id="12a8c-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="12a8c-129">-Confirm</span></span>
<span data-ttu-id="12a8c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="12a8c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a8c-131">-WhatIf</span></span>
<span data-ttu-id="12a8c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="12a8c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a8c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="12a8c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a8c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a8c-134">CommonParameters</span></span>
<span data-ttu-id="12a8c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a8c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a8c-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12a8c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a8c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12a8c-137">INPUTS</span></span>

### <span data-ttu-id="12a8c-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="12a8c-138">None</span></span>

## <span data-ttu-id="12a8c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12a8c-139">OUTPUTS</span></span>

### <span data-ttu-id="12a8c-140">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12a8c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="12a8c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12a8c-141">NOTES</span></span>

## <span data-ttu-id="12a8c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12a8c-142">RELATED LINKS</span></span>

[<span data-ttu-id="12a8c-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12a8c-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="12a8c-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12a8c-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="12a8c-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="12a8c-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
