---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400592"
---
# <span data-ttu-id="ee199-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ee199-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="ee199-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee199-102">SYNOPSIS</span></span>
<span data-ttu-id="ee199-103">Tar bort en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="ee199-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ee199-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee199-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee199-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee199-105">DESCRIPTION</span></span>
<span data-ttu-id="ee199-106">Tar bort en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="ee199-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ee199-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee199-107">EXAMPLES</span></span>

### <span data-ttu-id="ee199-108">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="ee199-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="ee199-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee199-109">PARAMETERS</span></span>

### <span data-ttu-id="ee199-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee199-110">-AsJob</span></span>
<span data-ttu-id="ee199-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ee199-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee199-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee199-112">-DefaultProfile</span></span>
<span data-ttu-id="ee199-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee199-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee199-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ee199-114">-Force</span></span>
<span data-ttu-id="ee199-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ee199-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee199-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee199-116">-Name</span></span>
<span data-ttu-id="ee199-117">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="ee199-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="ee199-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee199-118">-PassThru</span></span>
<span data-ttu-id="ee199-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ee199-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ee199-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ee199-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee199-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee199-121">-ResourceGroupName</span></span>
<span data-ttu-id="ee199-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="ee199-122">The resource group name</span></span>

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

### <span data-ttu-id="ee199-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ee199-123">-VirtualNetworkName</span></span>
<span data-ttu-id="ee199-124">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="ee199-124">The virtual network name.</span></span>

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

### <span data-ttu-id="ee199-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee199-125">-Confirm</span></span>
<span data-ttu-id="ee199-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee199-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee199-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee199-127">-WhatIf</span></span>
<span data-ttu-id="ee199-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee199-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee199-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee199-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee199-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee199-130">CommonParameters</span></span>
<span data-ttu-id="ee199-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee199-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee199-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee199-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee199-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee199-133">INPUTS</span></span>

### <span data-ttu-id="ee199-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ee199-134">System.String</span></span>

## <span data-ttu-id="ee199-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee199-135">OUTPUTS</span></span>

### <span data-ttu-id="ee199-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee199-136">System.Boolean</span></span>

## <span data-ttu-id="ee199-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee199-137">NOTES</span></span>

## <span data-ttu-id="ee199-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee199-138">RELATED LINKS</span></span>

[<span data-ttu-id="ee199-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ee199-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ee199-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ee199-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ee199-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ee199-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
