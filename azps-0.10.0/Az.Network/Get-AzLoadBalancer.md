---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922279"
---
# <span data-ttu-id="413a7-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="413a7-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="413a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="413a7-102">SYNOPSIS</span></span>
<span data-ttu-id="413a7-103">Får en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="413a7-103">Gets a load balancer.</span></span>

## <span data-ttu-id="413a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="413a7-104">SYNTAX</span></span>

### <span data-ttu-id="413a7-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="413a7-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="413a7-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="413a7-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="413a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="413a7-107">DESCRIPTION</span></span>
<span data-ttu-id="413a7-108">Cmdleten **Get-AzLoadBalancer** har en eller flera Azure belastningsutjämnare som ingår i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="413a7-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="413a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="413a7-109">EXAMPLES</span></span>

### <span data-ttu-id="413a7-110">Exempel 1: skaffa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="413a7-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="413a7-111">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="413a7-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="413a7-112">Det måste finnas en belastningsutjämnare innan du kan köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="413a7-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="413a7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="413a7-113">PARAMETERS</span></span>

### <span data-ttu-id="413a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="413a7-114">-DefaultProfile</span></span>
<span data-ttu-id="413a7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="413a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="413a7-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="413a7-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="413a7-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="413a7-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="413a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="413a7-119">CommonParameters</span></span>
<span data-ttu-id="413a7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="413a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="413a7-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="413a7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="413a7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="413a7-122">INPUTS</span></span>

## <span data-ttu-id="413a7-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="413a7-123">OUTPUTS</span></span>

### <span data-ttu-id="413a7-124">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="413a7-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="413a7-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="413a7-125">NOTES</span></span>

## <span data-ttu-id="413a7-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="413a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="413a7-127">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="413a7-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="413a7-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="413a7-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="413a7-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="413a7-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


