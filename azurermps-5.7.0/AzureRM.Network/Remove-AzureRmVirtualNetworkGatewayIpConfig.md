---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757395"
---
# <span data-ttu-id="8fbc3-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fbc3-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="8fbc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fbc3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fbc3-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fbc3-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fbc3-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fbc3-104">DESCRIPTION</span></span>

## <span data-ttu-id="8fbc3-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fbc3-105">EXAMPLES</span></span>

### <span data-ttu-id="8fbc3-106">9.1</span><span class="sxs-lookup"><span data-stu-id="8fbc3-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8fbc3-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fbc3-107">PARAMETERS</span></span>

### <span data-ttu-id="8fbc3-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbc3-108">-DefaultProfile</span></span>
<span data-ttu-id="8fbc3-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fbc3-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="8fbc3-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fbc3-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8fbc3-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fbc3-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fbc3-112">-Confirm</span></span>
<span data-ttu-id="8fbc3-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fbc3-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fbc3-114">-WhatIf</span></span>
<span data-ttu-id="8fbc3-115">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fbc3-116">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fbc3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbc3-117">CommonParameters</span></span>
<span data-ttu-id="8fbc3-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbc3-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fbc3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbc3-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fbc3-120">INPUTS</span></span>

### <span data-ttu-id="8fbc3-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8fbc3-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8fbc3-122">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="8fbc3-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8fbc3-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fbc3-123">OUTPUTS</span></span>

### <span data-ttu-id="8fbc3-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8fbc3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8fbc3-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fbc3-125">NOTES</span></span>

## <span data-ttu-id="8fbc3-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fbc3-126">RELATED LINKS</span></span>

