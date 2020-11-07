---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758284"
---
# <span data-ttu-id="7ba77-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="7ba77-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="7ba77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ba77-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba77-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ba77-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba77-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ba77-104">DESCRIPTION</span></span>

## <span data-ttu-id="7ba77-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ba77-105">EXAMPLES</span></span>

### <span data-ttu-id="7ba77-106">Exempel 1: ta bort en virtuell nätverks-peering</span><span class="sxs-lookup"><span data-stu-id="7ba77-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="7ba77-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ba77-107">PARAMETERS</span></span>

### <span data-ttu-id="7ba77-108">-Force</span><span class="sxs-lookup"><span data-stu-id="7ba77-108">-Force</span></span>
<span data-ttu-id="7ba77-109">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7ba77-109">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ba77-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ba77-110">-Name</span></span>
<span data-ttu-id="7ba77-111">Namn på peering med virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="7ba77-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="7ba77-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ba77-112">-PassThru</span></span>
<span data-ttu-id="7ba77-113">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7ba77-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7ba77-114">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7ba77-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ba77-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba77-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ba77-116">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="7ba77-116">The resource group name</span></span>

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

### <span data-ttu-id="7ba77-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7ba77-117">-VirtualNetworkName</span></span>
<span data-ttu-id="7ba77-118">Det virtuella nätverks namnet.</span><span class="sxs-lookup"><span data-stu-id="7ba77-118">The virtual network name.</span></span>

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

### <span data-ttu-id="7ba77-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ba77-119">-Confirm</span></span>
<span data-ttu-id="7ba77-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ba77-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba77-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba77-121">-WhatIf</span></span>
<span data-ttu-id="7ba77-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ba77-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba77-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ba77-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba77-124">-DefaultProfile</span></span>
<span data-ttu-id="7ba77-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba77-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ba77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba77-126">CommonParameters</span></span>
<span data-ttu-id="7ba77-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba77-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba77-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba77-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ba77-129">INPUTS</span></span>

## <span data-ttu-id="7ba77-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ba77-130">OUTPUTS</span></span>

## <span data-ttu-id="7ba77-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ba77-131">NOTES</span></span>

## <span data-ttu-id="7ba77-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ba77-132">RELATED LINKS</span></span>

