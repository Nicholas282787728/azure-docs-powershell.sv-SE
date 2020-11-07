---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924321"
---
# <span data-ttu-id="1b06b-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1b06b-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="1b06b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b06b-102">SYNOPSIS</span></span>

## <span data-ttu-id="1b06b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b06b-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b06b-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b06b-104">DESCRIPTION</span></span>

## <span data-ttu-id="1b06b-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b06b-105">EXAMPLES</span></span>

### <span data-ttu-id="1b06b-106">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="1b06b-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="1b06b-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b06b-107">PARAMETERS</span></span>

### <span data-ttu-id="1b06b-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b06b-108">-AsJob</span></span>
<span data-ttu-id="1b06b-109">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b06b-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b06b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b06b-110">-DefaultProfile</span></span>
<span data-ttu-id="1b06b-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b06b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b06b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1b06b-112">-Force</span></span>
<span data-ttu-id="1b06b-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1b06b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1b06b-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b06b-114">-Name</span></span>
<span data-ttu-id="1b06b-115">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="1b06b-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="1b06b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b06b-116">-PassThru</span></span>
<span data-ttu-id="1b06b-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="1b06b-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1b06b-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="1b06b-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b06b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b06b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b06b-120">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="1b06b-120">The resource group name</span></span>

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

### <span data-ttu-id="1b06b-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1b06b-121">-VirtualNetworkName</span></span>
<span data-ttu-id="1b06b-122">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="1b06b-122">The virtual network name.</span></span>

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

### <span data-ttu-id="1b06b-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b06b-123">-Confirm</span></span>
<span data-ttu-id="1b06b-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b06b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b06b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b06b-125">-WhatIf</span></span>
<span data-ttu-id="1b06b-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b06b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b06b-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b06b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b06b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b06b-128">CommonParameters</span></span>
<span data-ttu-id="1b06b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b06b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b06b-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b06b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b06b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b06b-131">INPUTS</span></span>

## <span data-ttu-id="1b06b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b06b-132">OUTPUTS</span></span>

## <span data-ttu-id="1b06b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b06b-133">NOTES</span></span>

## <span data-ttu-id="1b06b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b06b-134">RELATED LINKS</span></span>

