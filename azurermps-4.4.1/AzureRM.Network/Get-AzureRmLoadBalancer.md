---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581384"
---
# <span data-ttu-id="ea142-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea142-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="ea142-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea142-102">SYNOPSIS</span></span>
<span data-ttu-id="ea142-103">Får en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="ea142-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea142-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea142-104">SYNTAX</span></span>

### <span data-ttu-id="ea142-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="ea142-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea142-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="ea142-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea142-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea142-107">DESCRIPTION</span></span>
<span data-ttu-id="ea142-108">Cmdleten **Get-AzureRmLoadBalancer** har en eller flera Azure belastningsutjämnare som ingår i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ea142-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="ea142-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea142-109">EXAMPLES</span></span>

### <span data-ttu-id="ea142-110">Exempel 1: skaffa en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="ea142-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ea142-111">Det här kommandot får belastningsutjämnaren med namnet MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="ea142-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="ea142-112">Det måste finnas en belastningsutjämnare innan du kan köra denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea142-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="ea142-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea142-113">PARAMETERS</span></span>

### <span data-ttu-id="ea142-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="ea142-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea142-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea142-116">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea142-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea142-117">-DefaultProfile</span></span>
<span data-ttu-id="ea142-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea142-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea142-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea142-119">CommonParameters</span></span>
<span data-ttu-id="ea142-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea142-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea142-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea142-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea142-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea142-122">INPUTS</span></span>

## <span data-ttu-id="ea142-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea142-123">OUTPUTS</span></span>

### <span data-ttu-id="ea142-124">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea142-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ea142-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea142-125">NOTES</span></span>

## <span data-ttu-id="ea142-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea142-126">RELATED LINKS</span></span>

[<span data-ttu-id="ea142-127">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea142-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="ea142-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea142-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="ea142-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea142-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


