---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585103"
---
# <span data-ttu-id="7268c-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7268c-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="7268c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7268c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7268c-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7268c-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7268c-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7268c-104">DESCRIPTION</span></span>

## <span data-ttu-id="7268c-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7268c-105">EXAMPLES</span></span>

### <span data-ttu-id="7268c-106">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="7268c-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="7268c-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7268c-107">PARAMETERS</span></span>

### <span data-ttu-id="7268c-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7268c-108">-AsJob</span></span>
<span data-ttu-id="7268c-109">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7268c-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7268c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7268c-110">-DefaultProfile</span></span>
<span data-ttu-id="7268c-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7268c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7268c-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7268c-112">-Force</span></span>
<span data-ttu-id="7268c-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7268c-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7268c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="7268c-114">-Name</span></span>
<span data-ttu-id="7268c-115">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="7268c-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="7268c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7268c-116">-PassThru</span></span>
<span data-ttu-id="7268c-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7268c-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7268c-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7268c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7268c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7268c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7268c-120">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7268c-120">The resource group name</span></span>

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

### <span data-ttu-id="7268c-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7268c-121">-VirtualNetworkName</span></span>
<span data-ttu-id="7268c-122">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="7268c-122">The virtual network name.</span></span>

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

### <span data-ttu-id="7268c-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7268c-123">-Confirm</span></span>
<span data-ttu-id="7268c-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7268c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7268c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7268c-125">-WhatIf</span></span>
<span data-ttu-id="7268c-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7268c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7268c-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7268c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7268c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7268c-128">CommonParameters</span></span>
<span data-ttu-id="7268c-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7268c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7268c-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7268c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7268c-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7268c-131">INPUTS</span></span>

### <span data-ttu-id="7268c-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="7268c-132">None</span></span>
<span data-ttu-id="7268c-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7268c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7268c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7268c-134">OUTPUTS</span></span>

## <span data-ttu-id="7268c-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7268c-135">NOTES</span></span>

## <span data-ttu-id="7268c-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7268c-136">RELATED LINKS</span></span>

