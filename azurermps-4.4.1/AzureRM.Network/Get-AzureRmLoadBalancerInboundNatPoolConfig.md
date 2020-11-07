---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 9f9e14b94cbe38ba643d2c39beca5e1fe52138b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756335"
---
# <span data-ttu-id="9d18b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="9d18b-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="9d18b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d18b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d18b-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d18b-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d18b-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d18b-104">DESCRIPTION</span></span>

## <span data-ttu-id="9d18b-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d18b-105">EXAMPLES</span></span>

### <span data-ttu-id="9d18b-106">9.1</span><span class="sxs-lookup"><span data-stu-id="9d18b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9d18b-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d18b-107">PARAMETERS</span></span>

### <span data-ttu-id="9d18b-108">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d18b-108">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d18b-109">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d18b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d18b-110">-DefaultProfile</span></span>
<span data-ttu-id="9d18b-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d18b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d18b-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d18b-112">CommonParameters</span></span>
<span data-ttu-id="9d18b-113">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d18b-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d18b-114">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d18b-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d18b-115">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d18b-115">INPUTS</span></span>

### <span data-ttu-id="9d18b-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9d18b-116">PSLoadBalancer</span></span>
<span data-ttu-id="9d18b-117">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9d18b-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9d18b-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d18b-118">OUTPUTS</span></span>

### <span data-ttu-id="9d18b-119">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="9d18b-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="9d18b-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d18b-120">NOTES</span></span>

## <span data-ttu-id="9d18b-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d18b-121">RELATED LINKS</span></span>
