---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 5a68c17f26109f5000e82d31e21e0f0330b7c87a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919460"
---
# <span data-ttu-id="910f7-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="910f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="910f7-102">SYNOPSIS</span></span>
<span data-ttu-id="910f7-103">Uppdaterar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="910f7-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="910f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="910f7-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="910f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="910f7-105">DESCRIPTION</span></span>
<span data-ttu-id="910f7-106">Cmdleten **set-AzVirtualNetworkTap** uppdaterar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="910f7-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="910f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="910f7-107">EXAMPLES</span></span>

### <span data-ttu-id="910f7-108">Exempel 1: Konfigurera ett virtuellt nätverk tryck</span><span class="sxs-lookup"><span data-stu-id="910f7-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="910f7-109">Kommandot uppdaterar mål-IpConfiguration och uppdaterar det virtuella nätverkets tryckning.</span><span class="sxs-lookup"><span data-stu-id="910f7-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="910f7-110">Om det finns några trycknings konfigurationer som refererar till den kommer inte all käll trafik att starta till nya mål uppdateringar för konfiguration efter inlägg.</span><span class="sxs-lookup"><span data-stu-id="910f7-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="910f7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="910f7-111">PARAMETERS</span></span>

### <span data-ttu-id="910f7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="910f7-112">-AsJob</span></span>
<span data-ttu-id="910f7-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="910f7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="910f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910f7-114">-DefaultProfile</span></span>
<span data-ttu-id="910f7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="910f7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="910f7-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="910f7-117">Det virtuella nätverket trycker du på</span><span class="sxs-lookup"><span data-stu-id="910f7-117">The virtual network tap</span></span>

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

### <span data-ttu-id="910f7-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="910f7-118">-Confirm</span></span>
<span data-ttu-id="910f7-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="910f7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="910f7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="910f7-120">-WhatIf</span></span>
<span data-ttu-id="910f7-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="910f7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="910f7-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="910f7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="910f7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910f7-123">CommonParameters</span></span>
<span data-ttu-id="910f7-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="910f7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910f7-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910f7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910f7-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="910f7-126">INPUTS</span></span>

### <span data-ttu-id="910f7-127">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="910f7-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="910f7-128">OUTPUTS</span></span>

### <span data-ttu-id="910f7-129">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="910f7-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="910f7-130">NOTES</span></span>

## <span data-ttu-id="910f7-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="910f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="910f7-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="910f7-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="910f7-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="910f7-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
