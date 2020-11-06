---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 10d51bd2e70db0d2b1d06b907769fb6842e413cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585947"
---
# <span data-ttu-id="f070e-101">Add-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f070e-101">Add-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="f070e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f070e-102">SYNOPSIS</span></span>
<span data-ttu-id="f070e-103">Skapar en TapConfiguration resurs kopplad till en NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="f070e-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f070e-104">Detta hänvisar till en befintlig VirtualNetworkTap-resurs.</span><span class="sxs-lookup"><span data-stu-id="f070e-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f070e-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f070e-105">SYNTAX</span></span>

### <span data-ttu-id="f070e-106">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="f070e-106">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f070e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f070e-107">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f070e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f070e-108">DESCRIPTION</span></span>
<span data-ttu-id="f070e-109">Cmdleten **Add-AzureRmNetworkInterfaceTapConfig** skapar en TapConfiguration-resurs som är kopplad till en NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="f070e-109">The **Add-AzureRmNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="f070e-110">Detta hänvisar till en befintlig VirtualNetworkTap-resurs.</span><span class="sxs-lookup"><span data-stu-id="f070e-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f070e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f070e-111">EXAMPLES</span></span>

### <span data-ttu-id="f070e-112">Exempel 1: lägga till TapConfiguration i en given NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f070e-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzureRmNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="f070e-113">Lägg till TapConfiguration på en sourceNic.</span><span class="sxs-lookup"><span data-stu-id="f070e-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="f070e-114">Trafiken från sourceNic virtuella dator kommer att speglas till den virtuella dator som hänvisas till i vVirtualNetworkTap-resursen.</span><span class="sxs-lookup"><span data-stu-id="f070e-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="f070e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f070e-115">PARAMETERS</span></span>

### <span data-ttu-id="f070e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f070e-116">-DefaultProfile</span></span>
<span data-ttu-id="f070e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f070e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f070e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f070e-118">-Name</span></span>
<span data-ttu-id="f070e-119">Namnet på tryck konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f070e-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="f070e-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f070e-120">-NetworkInterface</span></span>
<span data-ttu-id="f070e-121">Referensen för nätverks gränssnitts resursen.</span><span class="sxs-lookup"><span data-stu-id="f070e-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f070e-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f070e-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="f070e-123">Referensen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="f070e-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f070e-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="f070e-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="f070e-125">Referensen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="f070e-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f070e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f070e-126">-Confirm</span></span>
<span data-ttu-id="f070e-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f070e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f070e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f070e-128">-WhatIf</span></span>
<span data-ttu-id="f070e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f070e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f070e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f070e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f070e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f070e-131">CommonParameters</span></span>
<span data-ttu-id="f070e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f070e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f070e-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f070e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f070e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f070e-134">INPUTS</span></span>

### <span data-ttu-id="f070e-135">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f070e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="f070e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f070e-136">System.String</span></span>

### <span data-ttu-id="f070e-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f070e-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="f070e-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f070e-138">OUTPUTS</span></span>

### <span data-ttu-id="f070e-139">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f070e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f070e-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f070e-140">NOTES</span></span>

## <span data-ttu-id="f070e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f070e-141">RELATED LINKS</span></span>
