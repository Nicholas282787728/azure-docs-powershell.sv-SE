---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093466"
---
# <span data-ttu-id="5ae51-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5ae51-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="5ae51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ae51-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae51-103">Stoppar en pågående felsökningssession för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5ae51-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="5ae51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ae51-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ae51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ae51-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae51-106">Cmdleten **Stop-AzureVirtualNetworkGatewayDiagnostics** stoppar en session med Virtual Network Gateway-diagnostik.</span><span class="sxs-lookup"><span data-stu-id="5ae51-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="5ae51-107">Det här kommandot sparar resultatet av diagnostikprogrammet för det lagrings konto som Start-AzureVirtualNetworkGatewayDiagnostics-cmdleten anger.</span><span class="sxs-lookup"><span data-stu-id="5ae51-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="5ae51-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ae51-108">EXAMPLES</span></span>

## <span data-ttu-id="5ae51-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ae51-109">PARAMETERS</span></span>

### <span data-ttu-id="5ae51-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5ae51-110">-GatewayId</span></span>
<span data-ttu-id="5ae51-111">Anger ID för en gateway.</span><span class="sxs-lookup"><span data-stu-id="5ae51-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="5ae51-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ae51-112">-Profile</span></span>
<span data-ttu-id="5ae51-113">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5ae51-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5ae51-114">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5ae51-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ae51-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae51-115">CommonParameters</span></span>
<span data-ttu-id="5ae51-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae51-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae51-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae51-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae51-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ae51-118">INPUTS</span></span>

## <span data-ttu-id="5ae51-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ae51-119">OUTPUTS</span></span>

## <span data-ttu-id="5ae51-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ae51-120">NOTES</span></span>

## <span data-ttu-id="5ae51-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ae51-121">RELATED LINKS</span></span>

[<span data-ttu-id="5ae51-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5ae51-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="5ae51-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5ae51-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


