---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926077"
---
# <span data-ttu-id="80553-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="80553-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="80553-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80553-102">SYNOPSIS</span></span>
<span data-ttu-id="80553-103">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="80553-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="80553-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80553-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80553-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80553-105">DESCRIPTION</span></span>
<span data-ttu-id="80553-106">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="80553-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="80553-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80553-107">EXAMPLES</span></span>

### <span data-ttu-id="80553-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="80553-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="80553-109">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="80553-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="80553-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80553-110">PARAMETERS</span></span>

### <span data-ttu-id="80553-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="80553-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="80553-112">Den ytterligare svars tiden i millisekunder för avsökningar för att falla in i den lägsta fördröjnings perioden.</span><span class="sxs-lookup"><span data-stu-id="80553-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="80553-113">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="80553-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80553-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80553-114">-DefaultProfile</span></span>
<span data-ttu-id="80553-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80553-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80553-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="80553-116">-Name</span></span>
<span data-ttu-id="80553-117">inställnings namn för hälso avsökning.</span><span class="sxs-lookup"><span data-stu-id="80553-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80553-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="80553-118">-SampleSize</span></span>
<span data-ttu-id="80553-119">Antalet prov att överväga för beslut om belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="80553-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="80553-120">Standardvärdet är 4</span><span class="sxs-lookup"><span data-stu-id="80553-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80553-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="80553-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="80553-122">Antalet sampel inom samplings perioden som måste uppfylla standardvärdet är 2</span><span class="sxs-lookup"><span data-stu-id="80553-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80553-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80553-123">CommonParameters</span></span>
<span data-ttu-id="80553-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80553-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80553-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80553-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80553-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80553-126">INPUTS</span></span>

### <span data-ttu-id="80553-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="80553-127">None</span></span>

## <span data-ttu-id="80553-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80553-128">OUTPUTS</span></span>

### <span data-ttu-id="80553-129">Microsoft. Azure. commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="80553-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="80553-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80553-130">NOTES</span></span>

## <span data-ttu-id="80553-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80553-131">RELATED LINKS</span></span>

<span data-ttu-id="80553-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="80553-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>