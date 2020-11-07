---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929713"
---
# <span data-ttu-id="3470e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3470e-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3470e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3470e-102">SYNOPSIS</span></span>
<span data-ttu-id="3470e-103">Skapar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="3470e-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3470e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3470e-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3470e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3470e-105">DESCRIPTION</span></span>
<span data-ttu-id="3470e-106">Cmdleten **New-AzureRmLoadBalancerBackendAddressPoolConfig** skapar en konfiguration för en server dels adresspool för en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="3470e-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3470e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3470e-107">EXAMPLES</span></span>

### <span data-ttu-id="3470e-108">Exempel 1: skapa en konfiguration för en server dels adresspool för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="3470e-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="3470e-109">Det här kommandot skapar en konfiguration för en server dels adresspool med namnet BackendAddressPool02 för en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="3470e-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="3470e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3470e-110">PARAMETERS</span></span>

### <span data-ttu-id="3470e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3470e-111">-DefaultProfile</span></span>
<span data-ttu-id="3470e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3470e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3470e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3470e-113">-Name</span></span>
<span data-ttu-id="3470e-114">Anger namnet på den adresspool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3470e-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="3470e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3470e-115">CommonParameters</span></span>
<span data-ttu-id="3470e-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3470e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3470e-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3470e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3470e-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3470e-118">INPUTS</span></span>

## <span data-ttu-id="3470e-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3470e-119">OUTPUTS</span></span>

### <span data-ttu-id="3470e-120">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3470e-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3470e-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3470e-121">NOTES</span></span>

## <span data-ttu-id="3470e-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3470e-122">RELATED LINKS</span></span>

[<span data-ttu-id="3470e-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3470e-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3470e-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3470e-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3470e-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3470e-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


