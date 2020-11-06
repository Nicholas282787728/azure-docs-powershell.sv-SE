---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: eb7f7b85286d491d4168e08ef94c1a46ff9076ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573633"
---
# <span data-ttu-id="d876a-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d876a-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="d876a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d876a-102">SYNOPSIS</span></span>
<span data-ttu-id="d876a-103">Tar bort en konfiguration för en server dels adresspool från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="d876a-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d876a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d876a-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d876a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d876a-105">DESCRIPTION</span></span>
<span data-ttu-id="d876a-106">Cmdleten **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** tar bort en server dels adress från en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="d876a-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="d876a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d876a-107">EXAMPLES</span></span>

### <span data-ttu-id="d876a-108">Exempel 1: ta bort en konfiguration av en server dels adresspool från en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="d876a-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d876a-109">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer och skickar det till **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , som tar bort BackendAddressPool02-konfigurationen från MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d876a-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="d876a-110">Slutligen uppdaterar Set-AzureRmLoadBalancer cmdleten MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d876a-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="d876a-111">Observera att en konfiguration för en server dels adresspool måste finnas innan du kan ta bort den.</span><span class="sxs-lookup"><span data-stu-id="d876a-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="d876a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d876a-112">PARAMETERS</span></span>

### <span data-ttu-id="d876a-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d876a-113">-LoadBalancer</span></span>
<span data-ttu-id="d876a-114">Anger den belastningsutjämnare som innehåller den server dels adress som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d876a-114">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="d876a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d876a-115">-Name</span></span>
<span data-ttu-id="d876a-116">Anger namnet på Server dels adresspoolen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="d876a-116">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d876a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d876a-117">-DefaultProfile</span></span>
<span data-ttu-id="d876a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d876a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d876a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d876a-119">CommonParameters</span></span>
<span data-ttu-id="d876a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d876a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d876a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d876a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d876a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d876a-122">INPUTS</span></span>

### <span data-ttu-id="d876a-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d876a-123">PSLoadBalancer</span></span>
<span data-ttu-id="d876a-124">Parametern ' LoadBalancer ' godkänner värdet av typen ' PSLoadBalancer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d876a-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d876a-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d876a-125">OUTPUTS</span></span>

### <span data-ttu-id="d876a-126">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d876a-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d876a-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d876a-127">NOTES</span></span>

## <span data-ttu-id="d876a-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d876a-128">RELATED LINKS</span></span>

[<span data-ttu-id="d876a-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d876a-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d876a-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d876a-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d876a-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d876a-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d876a-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d876a-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


