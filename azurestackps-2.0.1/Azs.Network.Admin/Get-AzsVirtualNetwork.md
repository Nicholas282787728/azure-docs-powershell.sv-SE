---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94092989"
---
# <span data-ttu-id="62d56-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62d56-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="62d56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62d56-102">SYNOPSIS</span></span>
<span data-ttu-id="62d56-103">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="62d56-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="62d56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62d56-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="62d56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62d56-105">DESCRIPTION</span></span>
<span data-ttu-id="62d56-106">Få en lista över alla virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="62d56-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="62d56-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62d56-107">EXAMPLES</span></span>

### <span data-ttu-id="62d56-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="62d56-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="62d56-109">Returnera en lista med virtuella nätverk för Azure-huvudstämpeln.</span><span class="sxs-lookup"><span data-stu-id="62d56-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="62d56-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62d56-110">PARAMETERS</span></span>

### <span data-ttu-id="62d56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d56-111">-DefaultProfile</span></span>
<span data-ttu-id="62d56-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62d56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d56-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="62d56-113">-Filter</span></span>
<span data-ttu-id="62d56-114">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="62d56-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="62d56-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="62d56-115">-InlineCount</span></span>
<span data-ttu-id="62d56-116">Parameter för OData-antal.</span><span class="sxs-lookup"><span data-stu-id="62d56-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="62d56-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="62d56-117">-OrderBy</span></span>
<span data-ttu-id="62d56-118">OData orderBy-parameter.</span><span class="sxs-lookup"><span data-stu-id="62d56-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="62d56-119">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="62d56-119">-Skip</span></span>
<span data-ttu-id="62d56-120">OData Skip-parameter.</span><span class="sxs-lookup"><span data-stu-id="62d56-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="62d56-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62d56-121">-SubscriptionId</span></span>
<span data-ttu-id="62d56-122">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="62d56-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="62d56-123">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="62d56-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="62d56-124">-Överst</span><span class="sxs-lookup"><span data-stu-id="62d56-124">-Top</span></span>
<span data-ttu-id="62d56-125">OData Top-parameter.</span><span class="sxs-lookup"><span data-stu-id="62d56-125">OData top parameter.</span></span>

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

### <span data-ttu-id="62d56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d56-126">CommonParameters</span></span>
<span data-ttu-id="62d56-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d56-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62d56-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d56-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62d56-129">INPUTS</span></span>

## <span data-ttu-id="62d56-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62d56-130">OUTPUTS</span></span>

### <span data-ttu-id="62d56-131">Microsoft. Azure. PowerShell. cmdletar. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62d56-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="62d56-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62d56-132">NOTES</span></span>

## <span data-ttu-id="62d56-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62d56-133">RELATED LINKS</span></span>
