---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575216"
---
# <span data-ttu-id="5c9a0-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="5c9a0-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="5c9a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9a0-103">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5c9a0-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c9a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c9a0-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c9a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c9a0-105">DESCRIPTION</span></span>
<span data-ttu-id="5c9a0-106">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5c9a0-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="5c9a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c9a0-107">EXAMPLES</span></span>

### <span data-ttu-id="5c9a0-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5c9a0-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="5c9a0-109">Skapa ett PSLoadBalancingSetting-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5c9a0-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="5c9a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c9a0-110">PARAMETERS</span></span>

### <span data-ttu-id="5c9a0-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="5c9a0-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="5c9a0-112">Den ytterligare svars tiden i millisekunder för avsökningar för att falla in i den lägsta fördröjnings perioden.</span><span class="sxs-lookup"><span data-stu-id="5c9a0-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="5c9a0-113">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="5c9a0-113">Default value is 0</span></span>

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

### <span data-ttu-id="5c9a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9a0-114">-DefaultProfile</span></span>
<span data-ttu-id="5c9a0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c9a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c9a0-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c9a0-116">-Name</span></span>
<span data-ttu-id="5c9a0-117">inställnings namn för hälso avsökning.</span><span class="sxs-lookup"><span data-stu-id="5c9a0-117">health probe setting name.</span></span>

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

### <span data-ttu-id="5c9a0-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="5c9a0-118">-SampleSize</span></span>
<span data-ttu-id="5c9a0-119">Antalet prov att överväga för beslut om belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="5c9a0-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="5c9a0-120">Standardvärdet är 4</span><span class="sxs-lookup"><span data-stu-id="5c9a0-120">Default value is 4</span></span>

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

### <span data-ttu-id="5c9a0-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="5c9a0-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="5c9a0-122">Antalet sampel inom samplings perioden som måste uppfylla standardvärdet är 2</span><span class="sxs-lookup"><span data-stu-id="5c9a0-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="5c9a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9a0-123">CommonParameters</span></span>
<span data-ttu-id="5c9a0-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c9a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9a0-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c9a0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9a0-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c9a0-126">INPUTS</span></span>

### <span data-ttu-id="5c9a0-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="5c9a0-127">None</span></span>

## <span data-ttu-id="5c9a0-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c9a0-128">OUTPUTS</span></span>

### <span data-ttu-id="5c9a0-129">Microsoft. Azure. commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="5c9a0-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="5c9a0-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c9a0-130">NOTES</span></span>

## <span data-ttu-id="5c9a0-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c9a0-131">RELATED LINKS</span></span>

<span data-ttu-id="5c9a0-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5c9a0-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
