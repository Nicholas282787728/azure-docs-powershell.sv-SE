---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583619"
---
# <span data-ttu-id="45b9a-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="45b9a-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="45b9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="45b9a-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="45b9a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45b9a-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b9a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="45b9a-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="45b9a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="45b9a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="45b9a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="45b9a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="45b9a-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="45b9a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="45b9a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45b9a-110">PARAMETERS</span></span>

### <span data-ttu-id="45b9a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45b9a-111">-AsJob</span></span>
<span data-ttu-id="45b9a-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="45b9a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b9a-113">-DefaultProfile</span></span>
<span data-ttu-id="45b9a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45b9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45b9a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="45b9a-115">-Force</span></span>
<span data-ttu-id="45b9a-116">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="45b9a-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="45b9a-117">-RouteFilter</span></span>
<span data-ttu-id="45b9a-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="45b9a-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45b9a-119">-Confirm</span></span>
<span data-ttu-id="45b9a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45b9a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b9a-121">-WhatIf</span></span>
<span data-ttu-id="45b9a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45b9a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b9a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45b9a-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45b9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b9a-124">CommonParameters</span></span>
<span data-ttu-id="45b9a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b9a-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b9a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b9a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45b9a-127">INPUTS</span></span>

### <span data-ttu-id="45b9a-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="45b9a-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="45b9a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45b9a-129">OUTPUTS</span></span>

### <span data-ttu-id="45b9a-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="45b9a-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="45b9a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45b9a-131">NOTES</span></span>

## <span data-ttu-id="45b9a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45b9a-132">RELATED LINKS</span></span>

