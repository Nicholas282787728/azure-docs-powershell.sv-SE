---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: d3dcdabc84eca5efa7e52e61f4beafd23eb67b05
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922276"
---
# <span data-ttu-id="7f99d-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7f99d-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7f99d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f99d-102">SYNOPSIS</span></span>

## <span data-ttu-id="7f99d-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f99d-103">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f99d-104">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f99d-104">DESCRIPTION</span></span>

## <span data-ttu-id="7f99d-105">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f99d-105">EXAMPLES</span></span>

### <span data-ttu-id="7f99d-106">9.1</span><span class="sxs-lookup"><span data-stu-id="7f99d-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="7f99d-107">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f99d-107">PARAMETERS</span></span>

### <span data-ttu-id="7f99d-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f99d-108">-DefaultProfile</span></span>
<span data-ttu-id="7f99d-109">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f99d-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f99d-110">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f99d-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f99d-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f99d-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f99d-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f99d-112">CommonParameters</span></span>
<span data-ttu-id="7f99d-113">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f99d-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f99d-114">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f99d-114">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f99d-115">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f99d-115">INPUTS</span></span>

### <span data-ttu-id="7f99d-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7f99d-116">PSLoadBalancer</span></span>
<span data-ttu-id="7f99d-117">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7f99d-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7f99d-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f99d-118">OUTPUTS</span></span>

### <span data-ttu-id="7f99d-119">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="7f99d-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="7f99d-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f99d-120">NOTES</span></span>

## <span data-ttu-id="7f99d-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f99d-121">RELATED LINKS</span></span>

