---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 73e4fb2dde10739176a1adfe55c22529e8ccdaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576167"
---
# <span data-ttu-id="f0e62-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f0e62-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="f0e62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0e62-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e62-103">Tar bort en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="f0e62-103">Removes a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0e62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0e62-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0e62-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0e62-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e62-106">Tar bort en virtuell nätverks-peering.</span><span class="sxs-lookup"><span data-stu-id="f0e62-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="f0e62-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0e62-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e62-108">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="f0e62-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="f0e62-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0e62-109">PARAMETERS</span></span>

### <span data-ttu-id="f0e62-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0e62-110">-AsJob</span></span>
<span data-ttu-id="f0e62-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f0e62-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0e62-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e62-112">-DefaultProfile</span></span>
<span data-ttu-id="f0e62-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0e62-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0e62-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f0e62-114">-Force</span></span>
<span data-ttu-id="f0e62-115">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f0e62-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0e62-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0e62-116">-Name</span></span>
<span data-ttu-id="f0e62-117">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="f0e62-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="f0e62-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0e62-118">-PassThru</span></span>
<span data-ttu-id="f0e62-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f0e62-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0e62-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f0e62-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0e62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e62-121">-ResourceGroupName</span></span>
<span data-ttu-id="f0e62-122">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="f0e62-122">The resource group name</span></span>

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

### <span data-ttu-id="f0e62-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f0e62-123">-VirtualNetworkName</span></span>
<span data-ttu-id="f0e62-124">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="f0e62-124">The virtual network name.</span></span>

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

### <span data-ttu-id="f0e62-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0e62-125">-Confirm</span></span>
<span data-ttu-id="f0e62-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0e62-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0e62-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0e62-127">-WhatIf</span></span>
<span data-ttu-id="f0e62-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0e62-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0e62-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0e62-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0e62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e62-130">CommonParameters</span></span>
<span data-ttu-id="f0e62-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e62-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e62-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e62-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0e62-133">INPUTS</span></span>

### <span data-ttu-id="f0e62-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f0e62-134">System.String</span></span>

## <span data-ttu-id="f0e62-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0e62-135">OUTPUTS</span></span>

### <span data-ttu-id="f0e62-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f0e62-136">System.Boolean</span></span>

## <span data-ttu-id="f0e62-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0e62-137">NOTES</span></span>

## <span data-ttu-id="f0e62-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0e62-138">RELATED LINKS</span></span>
