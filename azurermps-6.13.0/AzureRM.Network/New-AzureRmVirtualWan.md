---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584911"
---
# <span data-ttu-id="f6fc8-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f6fc8-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="f6fc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fc8-103">Skapar ett Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6fc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6fc8-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6fc8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fc8-106">Skapar en ny Azure VirtualWAN-resurs.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="f6fc8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6fc8-107">EXAMPLES</span></span>

### <span data-ttu-id="f6fc8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6fc8-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="f6fc8-109">Ovanstående skapar en resurs grupp "testRG" i regionen "West" och ett Azure Virtual WAN med gren till filial trafik som tillåts i den resurs gruppen i Azure.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="f6fc8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6fc8-110">PARAMETERS</span></span>

### <span data-ttu-id="f6fc8-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="f6fc8-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="f6fc8-112">Tillåt gren till gren trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f6fc8-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="f6fc8-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="f6fc8-114">Tillåt VNet till VNet-trafik för VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="f6fc8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6fc8-115">-AsJob</span></span>
<span data-ttu-id="f6fc8-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f6fc8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6fc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fc8-117">-DefaultProfile</span></span>
<span data-ttu-id="f6fc8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6fc8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="f6fc8-119">-Location</span></span>
<span data-ttu-id="f6fc8-120">Platsen för VirtualWAN-resursen.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="f6fc8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6fc8-121">-Name</span></span>
<span data-ttu-id="f6fc8-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-122">The resource name.</span></span>

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

### <span data-ttu-id="f6fc8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fc8-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6fc8-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-124">The resource group name.</span></span>

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

### <span data-ttu-id="f6fc8-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f6fc8-125">-Tag</span></span>
<span data-ttu-id="f6fc8-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f6fc8-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6fc8-127">-Confirm</span></span>
<span data-ttu-id="f6fc8-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fc8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fc8-129">-WhatIf</span></span>
<span data-ttu-id="f6fc8-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6fc8-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fc8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fc8-132">CommonParameters</span></span>
<span data-ttu-id="f6fc8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fc8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fc8-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6fc8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fc8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6fc8-135">INPUTS</span></span>

### <span data-ttu-id="f6fc8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f6fc8-136">System.String</span></span>

### <span data-ttu-id="f6fc8-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f6fc8-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6fc8-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6fc8-138">OUTPUTS</span></span>

### <span data-ttu-id="f6fc8-139">Microsoft. Azure. commands. Networks. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f6fc8-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f6fc8-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6fc8-140">NOTES</span></span>

## <span data-ttu-id="f6fc8-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6fc8-141">RELATED LINKS</span></span>
