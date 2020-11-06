---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584900"
---
# <span data-ttu-id="4e343-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4e343-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="4e343-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e343-102">SYNOPSIS</span></span>
<span data-ttu-id="4e343-103">Anger mål tillståndet för ett virtuellt nätverk tryck.</span><span class="sxs-lookup"><span data-stu-id="4e343-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e343-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e343-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e343-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e343-105">DESCRIPTION</span></span>
<span data-ttu-id="4e343-106">**Set-AzureRmVirtualNetworkTap** anger mål tillståndet för ett Azure Virtual Network-tryck.</span><span class="sxs-lookup"><span data-stu-id="4e343-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="4e343-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e343-107">EXAMPLES</span></span>

### <span data-ttu-id="4e343-108">Exempel 1: Konfigurera ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="4e343-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="4e343-109">Kommandot uppdaterar mål-IpConfiguration och uppdaterar det virtuella nätverkets tryckning.</span><span class="sxs-lookup"><span data-stu-id="4e343-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="4e343-110">Om det finns några trycknings konfigurationer som refererar till den kommer inte all käll trafik att starta till nya mål uppdateringar för konfiguration efter inlägg.</span><span class="sxs-lookup"><span data-stu-id="4e343-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="4e343-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e343-111">PARAMETERS</span></span>

### <span data-ttu-id="4e343-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e343-112">-AsJob</span></span>
<span data-ttu-id="4e343-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4e343-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e343-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e343-114">-DefaultProfile</span></span>
<span data-ttu-id="4e343-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e343-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e343-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4e343-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="4e343-117">Det virtuella nätverket trycker du på</span><span class="sxs-lookup"><span data-stu-id="4e343-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e343-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e343-118">-Confirm</span></span>
<span data-ttu-id="4e343-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e343-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e343-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e343-120">-WhatIf</span></span>
<span data-ttu-id="4e343-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e343-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e343-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e343-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e343-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e343-123">CommonParameters</span></span>
<span data-ttu-id="4e343-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e343-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e343-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e343-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e343-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e343-126">INPUTS</span></span>

### <span data-ttu-id="4e343-127">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4e343-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="4e343-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e343-128">OUTPUTS</span></span>

### <span data-ttu-id="4e343-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4e343-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="4e343-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e343-130">NOTES</span></span>

## <span data-ttu-id="4e343-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e343-131">RELATED LINKS</span></span>
