---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924325"
---
# <span data-ttu-id="6722a-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="6722a-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="6722a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6722a-102">SYNOPSIS</span></span>

## <span data-ttu-id="6722a-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6722a-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6722a-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6722a-104">DESCRIPTION</span></span>

## <span data-ttu-id="6722a-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6722a-105">EXAMPLES</span></span>

### <span data-ttu-id="6722a-106">9.1</span><span class="sxs-lookup"><span data-stu-id="6722a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="6722a-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6722a-107">PARAMETERS</span></span>

### <span data-ttu-id="6722a-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6722a-108">-DefaultProfile</span></span>
<span data-ttu-id="6722a-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6722a-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6722a-110">-Namn</span><span class="sxs-lookup"><span data-stu-id="6722a-110">-Name</span></span>
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

### <span data-ttu-id="6722a-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6722a-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="6722a-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6722a-112">-Confirm</span></span>
<span data-ttu-id="6722a-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6722a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6722a-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6722a-114">-WhatIf</span></span>
<span data-ttu-id="6722a-115">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6722a-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6722a-116">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6722a-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6722a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6722a-117">CommonParameters</span></span>
<span data-ttu-id="6722a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6722a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6722a-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6722a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6722a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6722a-120">INPUTS</span></span>

### <span data-ttu-id="6722a-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6722a-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="6722a-122">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6722a-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="6722a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6722a-123">OUTPUTS</span></span>

### <span data-ttu-id="6722a-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6722a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6722a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6722a-125">NOTES</span></span>

## <span data-ttu-id="6722a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6722a-126">RELATED LINKS</span></span>

