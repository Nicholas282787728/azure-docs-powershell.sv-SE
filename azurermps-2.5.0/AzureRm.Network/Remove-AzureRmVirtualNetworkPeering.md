---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931193"
---
# <span data-ttu-id="591a2-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="591a2-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="591a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="591a2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="591a2-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="591a2-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="591a2-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="591a2-104">DESCRIPTION</span></span>

## <span data-ttu-id="591a2-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="591a2-105">EXAMPLES</span></span>

### <span data-ttu-id="591a2-106">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="591a2-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="591a2-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="591a2-107">PARAMETERS</span></span>

### <span data-ttu-id="591a2-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="591a2-108">-AsJob</span></span>
<span data-ttu-id="591a2-109">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="591a2-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="591a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591a2-110">-DefaultProfile</span></span>
<span data-ttu-id="591a2-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="591a2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="591a2-112">-Force</span></span>
<span data-ttu-id="591a2-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="591a2-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="591a2-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="591a2-114">-Name</span></span>
<span data-ttu-id="591a2-115">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="591a2-115">The virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="591a2-116">-PassThru</span></span>
<span data-ttu-id="591a2-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="591a2-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="591a2-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="591a2-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="591a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="591a2-120">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="591a2-120">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="591a2-121">-VirtualNetworkName</span></span>
<span data-ttu-id="591a2-122">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="591a2-122">The virtual network name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="591a2-123">-Confirm</span></span>
<span data-ttu-id="591a2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="591a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="591a2-125">-WhatIf</span></span>
<span data-ttu-id="591a2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="591a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="591a2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="591a2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591a2-128">CommonParameters</span></span>
<span data-ttu-id="591a2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591a2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="591a2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591a2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="591a2-131">INPUTS</span></span>

## <span data-ttu-id="591a2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="591a2-132">OUTPUTS</span></span>

## <span data-ttu-id="591a2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="591a2-133">NOTES</span></span>

## <span data-ttu-id="591a2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="591a2-134">RELATED LINKS</span></span>

