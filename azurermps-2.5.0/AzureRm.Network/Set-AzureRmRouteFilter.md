---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930874"
---
# <span data-ttu-id="77f55-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="77f55-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="77f55-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77f55-102">SYNOPSIS</span></span>
<span data-ttu-id="77f55-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="77f55-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f55-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77f55-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77f55-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77f55-105">DESCRIPTION</span></span>
<span data-ttu-id="77f55-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="77f55-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="77f55-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77f55-107">EXAMPLES</span></span>

### <span data-ttu-id="77f55-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77f55-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="77f55-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="77f55-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="77f55-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77f55-110">PARAMETERS</span></span>

### <span data-ttu-id="77f55-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77f55-111">-AsJob</span></span>
<span data-ttu-id="77f55-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="77f55-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77f55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f55-113">-DefaultProfile</span></span>
<span data-ttu-id="77f55-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77f55-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f55-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77f55-115">-Force</span></span>
<span data-ttu-id="77f55-116">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="77f55-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="77f55-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="77f55-117">-RouteFilter</span></span>
<span data-ttu-id="77f55-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="77f55-118">The RouteFilter</span></span>

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

### <span data-ttu-id="77f55-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77f55-119">-Confirm</span></span>
<span data-ttu-id="77f55-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77f55-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77f55-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f55-121">-WhatIf</span></span>
<span data-ttu-id="77f55-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77f55-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77f55-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77f55-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77f55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f55-124">CommonParameters</span></span>
<span data-ttu-id="77f55-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f55-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f55-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77f55-127">INPUTS</span></span>

### <span data-ttu-id="77f55-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="77f55-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="77f55-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77f55-129">OUTPUTS</span></span>

### <span data-ttu-id="77f55-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="77f55-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="77f55-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77f55-131">NOTES</span></span>

## <span data-ttu-id="77f55-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77f55-132">RELATED LINKS</span></span>

