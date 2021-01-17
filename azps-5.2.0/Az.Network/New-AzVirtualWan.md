---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412307"
---
# <span data-ttu-id="eee71-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="eee71-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="eee71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eee71-102">SYNOPSIS</span></span>
<span data-ttu-id="eee71-103">Skapar ett Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="eee71-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="eee71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eee71-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eee71-105">DESCRIPTION</span></span>
<span data-ttu-id="eee71-106">Skapar en ny Azure VirtualWAN-resurs.</span><span class="sxs-lookup"><span data-stu-id="eee71-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="eee71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eee71-107">EXAMPLES</span></span>

### <span data-ttu-id="eee71-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eee71-108">Example 1</span></span>

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

<span data-ttu-id="eee71-109">Ovanstående skapar en resurs grupp "testRG" i regionen "West" och ett Azure Virtual WAN med gren till filial trafik som tillåts i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="eee71-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="eee71-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eee71-110">PARAMETERS</span></span>

### <span data-ttu-id="eee71-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="eee71-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="eee71-112">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="eee71-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="eee71-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="eee71-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="eee71-114">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="eee71-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="eee71-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eee71-115">-AsJob</span></span>
<span data-ttu-id="eee71-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eee71-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eee71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee71-117">-DefaultProfile</span></span>
<span data-ttu-id="eee71-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eee71-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eee71-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="eee71-119">-Location</span></span>
<span data-ttu-id="eee71-120">Platsen för VirtualWAN-resursen.</span><span class="sxs-lookup"><span data-stu-id="eee71-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="eee71-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="eee71-121">-Name</span></span>
<span data-ttu-id="eee71-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="eee71-122">The resource name.</span></span>

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

### <span data-ttu-id="eee71-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee71-123">-ResourceGroupName</span></span>
<span data-ttu-id="eee71-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="eee71-124">The resource group name.</span></span>

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

### <span data-ttu-id="eee71-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eee71-125">-Tag</span></span>
<span data-ttu-id="eee71-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="eee71-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eee71-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="eee71-127">-VirtualWANType</span></span>
<span data-ttu-id="eee71-128">Typen av virtuellt WAN.</span><span class="sxs-lookup"><span data-stu-id="eee71-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="eee71-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eee71-129">-Confirm</span></span>
<span data-ttu-id="eee71-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eee71-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee71-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee71-131">-WhatIf</span></span>
<span data-ttu-id="eee71-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eee71-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee71-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eee71-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee71-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee71-134">CommonParameters</span></span>
<span data-ttu-id="eee71-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee71-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee71-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eee71-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee71-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eee71-137">INPUTS</span></span>

### <span data-ttu-id="eee71-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="eee71-138">None</span></span>

## <span data-ttu-id="eee71-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eee71-139">OUTPUTS</span></span>

### <span data-ttu-id="eee71-140">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="eee71-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="eee71-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eee71-141">NOTES</span></span>

## <span data-ttu-id="eee71-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eee71-142">RELATED LINKS</span></span>

[<span data-ttu-id="eee71-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="eee71-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="eee71-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="eee71-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="eee71-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="eee71-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
