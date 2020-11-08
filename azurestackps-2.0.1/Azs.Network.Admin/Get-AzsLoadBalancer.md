---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092941"
---
# <span data-ttu-id="dab97-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dab97-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="dab97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dab97-102">SYNOPSIS</span></span>
<span data-ttu-id="dab97-103">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="dab97-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="dab97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dab97-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dab97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dab97-105">DESCRIPTION</span></span>
<span data-ttu-id="dab97-106">Få en lista över alla belastnings utjämningar.</span><span class="sxs-lookup"><span data-stu-id="dab97-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="dab97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dab97-107">EXAMPLES</span></span>

### <span data-ttu-id="dab97-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dab97-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="dab97-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dab97-109">PARAMETERS</span></span>

### <span data-ttu-id="dab97-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab97-110">-DefaultProfile</span></span>
<span data-ttu-id="dab97-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dab97-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dab97-112">-Filter</span><span class="sxs-lookup"><span data-stu-id="dab97-112">-Filter</span></span>
<span data-ttu-id="dab97-113">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="dab97-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="dab97-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="dab97-114">-InlineCount</span></span>
<span data-ttu-id="dab97-115">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="dab97-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="dab97-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="dab97-116">-OrderBy</span></span>
<span data-ttu-id="dab97-117">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="dab97-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="dab97-118">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="dab97-118">-Skip</span></span>
<span data-ttu-id="dab97-119">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="dab97-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="dab97-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dab97-120">-SubscriptionId</span></span>
<span data-ttu-id="dab97-121">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="dab97-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dab97-122">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dab97-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dab97-123">-Överst</span><span class="sxs-lookup"><span data-stu-id="dab97-123">-Top</span></span>
<span data-ttu-id="dab97-124">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="dab97-124">OData top parameter.</span></span>

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

### <span data-ttu-id="dab97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab97-125">CommonParameters</span></span>
<span data-ttu-id="dab97-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dab97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab97-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dab97-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab97-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dab97-128">INPUTS</span></span>

## <span data-ttu-id="dab97-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dab97-129">OUTPUTS</span></span>

### <span data-ttu-id="dab97-130">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dab97-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="dab97-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dab97-131">NOTES</span></span>

## <span data-ttu-id="dab97-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dab97-132">RELATED LINKS</span></span>

