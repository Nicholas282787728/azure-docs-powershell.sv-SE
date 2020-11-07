---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921533"
---
# <span data-ttu-id="c8c33-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c8c33-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="c8c33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8c33-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c33-103">Lista alla kvoter.</span><span class="sxs-lookup"><span data-stu-id="c8c33-103">List all quotas.</span></span>

## <span data-ttu-id="c8c33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8c33-104">SYNTAX</span></span>

### <span data-ttu-id="c8c33-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c8c33-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8c33-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c8c33-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c8c33-107">ID</span><span class="sxs-lookup"><span data-stu-id="c8c33-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c8c33-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8c33-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c33-109">Lista alla kvoter.</span><span class="sxs-lookup"><span data-stu-id="c8c33-109">List all quotas.</span></span>
<span data-ttu-id="c8c33-110">Begränsa listan genom att skicka ett namn eller ett filter.</span><span class="sxs-lookup"><span data-stu-id="c8c33-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="c8c33-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8c33-111">EXAMPLES</span></span>

### <span data-ttu-id="c8c33-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="c8c33-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="c8c33-113">Visar alla nätverks kvoter.</span><span class="sxs-lookup"><span data-stu-id="c8c33-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="c8c33-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="c8c33-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c8c33-115">Hämtar den angivna nätverks kvoten.</span><span class="sxs-lookup"><span data-stu-id="c8c33-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="c8c33-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8c33-116">PARAMETERS</span></span>

### <span data-ttu-id="c8c33-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8c33-117">-Name</span></span>
<span data-ttu-id="c8c33-118">Resurs namn för nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="c8c33-118">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c33-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="c8c33-119">-Location</span></span>
<span data-ttu-id="c8c33-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="c8c33-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c33-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c33-121">-ResourceId</span></span>
<span data-ttu-id="c8c33-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="c8c33-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c33-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="c8c33-123">-Filter</span></span>
<span data-ttu-id="c8c33-124">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="c8c33-124">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c33-125">CommonParameters</span></span>
<span data-ttu-id="c8c33-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c33-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c33-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c33-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8c33-128">INPUTS</span></span>

## <span data-ttu-id="c8c33-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8c33-129">OUTPUTS</span></span>

### <span data-ttu-id="c8c33-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="c8c33-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="c8c33-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8c33-131">NOTES</span></span>

## <span data-ttu-id="c8c33-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8c33-132">RELATED LINKS</span></span>
