---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921823"
---
# <span data-ttu-id="044a6-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="044a6-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="044a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="044a6-102">SYNOPSIS</span></span>
<span data-ttu-id="044a6-103">Lista alla kvoter.</span><span class="sxs-lookup"><span data-stu-id="044a6-103">List all quotas.</span></span>

## <span data-ttu-id="044a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="044a6-104">SYNTAX</span></span>

### <span data-ttu-id="044a6-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="044a6-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="044a6-106">Lära</span><span class="sxs-lookup"><span data-stu-id="044a6-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="044a6-107">ID</span><span class="sxs-lookup"><span data-stu-id="044a6-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="044a6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="044a6-108">DESCRIPTION</span></span>
<span data-ttu-id="044a6-109">Lista alla kvoter.</span><span class="sxs-lookup"><span data-stu-id="044a6-109">List all quotas.</span></span>
<span data-ttu-id="044a6-110">Begränsa listan genom att skicka ett namn eller ett filter.</span><span class="sxs-lookup"><span data-stu-id="044a6-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="044a6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="044a6-111">EXAMPLES</span></span>

### <span data-ttu-id="044a6-112">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="044a6-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="044a6-113">Visar alla nätverks kvoter.</span><span class="sxs-lookup"><span data-stu-id="044a6-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="044a6-114">EXEMPEL 2</span><span class="sxs-lookup"><span data-stu-id="044a6-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="044a6-115">Hämtar den angivna nätverks kvoten.</span><span class="sxs-lookup"><span data-stu-id="044a6-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="044a6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="044a6-116">PARAMETERS</span></span>

### <span data-ttu-id="044a6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="044a6-117">-Name</span></span>
<span data-ttu-id="044a6-118">Resurs namn för nätverks kvot.</span><span class="sxs-lookup"><span data-stu-id="044a6-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="044a6-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="044a6-119">-Location</span></span>
<span data-ttu-id="044a6-120">Plats för resursen.</span><span class="sxs-lookup"><span data-stu-id="044a6-120">Location of the resource.</span></span>

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

### <span data-ttu-id="044a6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="044a6-121">-ResourceId</span></span>
<span data-ttu-id="044a6-122">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="044a6-122">The resource id.</span></span>

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

### <span data-ttu-id="044a6-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="044a6-123">-Filter</span></span>
<span data-ttu-id="044a6-124">Parametern OData filter.</span><span class="sxs-lookup"><span data-stu-id="044a6-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="044a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044a6-125">CommonParameters</span></span>
<span data-ttu-id="044a6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="044a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044a6-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044a6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044a6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="044a6-128">INPUTS</span></span>

## <span data-ttu-id="044a6-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="044a6-129">OUTPUTS</span></span>

### <span data-ttu-id="044a6-130">Microsoft. AzureStack. Management. Network. admin. Models. quota</span><span class="sxs-lookup"><span data-stu-id="044a6-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="044a6-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="044a6-131">NOTES</span></span>

## <span data-ttu-id="044a6-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="044a6-132">RELATED LINKS</span></span>
