---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522643"
---
# <span data-ttu-id="0f267-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="0f267-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="0f267-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f267-102">SYNOPSIS</span></span>
<span data-ttu-id="0f267-103">Skapa ett objekt i minnet för DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="0f267-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="0f267-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f267-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f267-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f267-105">DESCRIPTION</span></span>
<span data-ttu-id="0f267-106">Skapa ett objekt i minnet för DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="0f267-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="0f267-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f267-107">EXAMPLES</span></span>

### <span data-ttu-id="0f267-108">Exempel 1: skapa en DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="0f267-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="0f267-109">Skapa en DigitalTwinsIdentityObject utifrån ID och plats</span><span class="sxs-lookup"><span data-stu-id="0f267-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="0f267-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f267-110">PARAMETERS</span></span>

### <span data-ttu-id="0f267-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0f267-111">-EndpointName</span></span>
<span data-ttu-id="0f267-112">Namn på slut punkts resurs.</span><span class="sxs-lookup"><span data-stu-id="0f267-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="0f267-113">-ID</span><span class="sxs-lookup"><span data-stu-id="0f267-113">-Id</span></span>
<span data-ttu-id="0f267-114">Resurs identitets Sök väg.</span><span class="sxs-lookup"><span data-stu-id="0f267-114">Resource identity path.</span></span>

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

### <span data-ttu-id="0f267-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="0f267-115">-Location</span></span>
<span data-ttu-id="0f267-116">Plats för DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0f267-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0f267-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f267-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f267-118">Namnet på resurs gruppen som innehåller DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0f267-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0f267-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0f267-119">-ResourceName</span></span>
<span data-ttu-id="0f267-120">Namnet på DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="0f267-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="0f267-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f267-121">-SubscriptionId</span></span>
<span data-ttu-id="0f267-122">Prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="0f267-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="0f267-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f267-123">CommonParameters</span></span>
<span data-ttu-id="0f267-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f267-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f267-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f267-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f267-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f267-126">INPUTS</span></span>

## <span data-ttu-id="0f267-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f267-127">OUTPUTS</span></span>

### <span data-ttu-id="0f267-128">Microsoft. Azure. PowerShell. cmdletar. DigitalTwins. Models. DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="0f267-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="0f267-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f267-129">NOTES</span></span>

<span data-ttu-id="0f267-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0f267-130">ALIASES</span></span>

## <span data-ttu-id="0f267-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f267-131">RELATED LINKS</span></span>

