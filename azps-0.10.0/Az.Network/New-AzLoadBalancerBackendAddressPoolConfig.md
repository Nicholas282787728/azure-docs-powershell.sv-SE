---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922134"
---
# <span data-ttu-id="02a14-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="02a14-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="02a14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02a14-102">SYNOPSIS</span></span>
<span data-ttu-id="02a14-103">Skapar en konfiguration för en server dels adresspool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="02a14-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="02a14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02a14-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02a14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02a14-105">DESCRIPTION</span></span>
<span data-ttu-id="02a14-106">Cmdleten **New-AzLoadBalancerBackendAddressPoolConfig** skapar en konfiguration för en server dels adresspool för en Azure belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="02a14-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="02a14-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02a14-107">EXAMPLES</span></span>

### <span data-ttu-id="02a14-108">Exempel 1: skapa en konfiguration för en server dels adresspool för belastningsutjämnaren</span><span class="sxs-lookup"><span data-stu-id="02a14-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="02a14-109">Det här kommandot skapar en konfiguration för en server dels adresspool med namnet BackendAddressPool02 för en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="02a14-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="02a14-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02a14-110">PARAMETERS</span></span>

### <span data-ttu-id="02a14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a14-111">-DefaultProfile</span></span>
<span data-ttu-id="02a14-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02a14-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a14-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="02a14-113">-Name</span></span>
<span data-ttu-id="02a14-114">Anger namnet på den adresspool som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="02a14-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="02a14-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a14-115">CommonParameters</span></span>
<span data-ttu-id="02a14-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a14-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a14-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a14-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a14-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02a14-118">INPUTS</span></span>

## <span data-ttu-id="02a14-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02a14-119">OUTPUTS</span></span>

### <span data-ttu-id="02a14-120">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="02a14-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="02a14-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02a14-121">NOTES</span></span>

## <span data-ttu-id="02a14-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02a14-122">RELATED LINKS</span></span>

[<span data-ttu-id="02a14-123">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="02a14-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="02a14-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="02a14-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="02a14-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="02a14-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


