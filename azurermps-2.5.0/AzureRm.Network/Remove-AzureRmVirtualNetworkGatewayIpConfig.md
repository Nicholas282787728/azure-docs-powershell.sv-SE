---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929281"
---
# <span data-ttu-id="16fe9-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="16fe9-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="16fe9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16fe9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16fe9-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16fe9-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16fe9-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16fe9-104">DESCRIPTION</span></span>

## <span data-ttu-id="16fe9-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16fe9-105">EXAMPLES</span></span>

### <span data-ttu-id="16fe9-106">9.1</span><span class="sxs-lookup"><span data-stu-id="16fe9-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="16fe9-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16fe9-107">PARAMETERS</span></span>

### <span data-ttu-id="16fe9-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fe9-108">-DefaultProfile</span></span>
<span data-ttu-id="16fe9-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16fe9-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16fe9-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="16fe9-110">-Name</span></span>
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

### <span data-ttu-id="16fe9-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16fe9-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="16fe9-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16fe9-112">-Confirm</span></span>
<span data-ttu-id="16fe9-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16fe9-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16fe9-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16fe9-114">-WhatIf</span></span>
<span data-ttu-id="16fe9-115">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16fe9-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16fe9-116">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16fe9-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16fe9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fe9-117">CommonParameters</span></span>
<span data-ttu-id="16fe9-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16fe9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fe9-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16fe9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fe9-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16fe9-120">INPUTS</span></span>

### <span data-ttu-id="16fe9-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16fe9-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="16fe9-122">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="16fe9-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="16fe9-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16fe9-123">OUTPUTS</span></span>

### <span data-ttu-id="16fe9-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="16fe9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="16fe9-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16fe9-125">NOTES</span></span>

## <span data-ttu-id="16fe9-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16fe9-126">RELATED LINKS</span></span>

