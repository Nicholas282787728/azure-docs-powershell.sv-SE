---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: 942669106e70bbb8c5b5b6f059fe934effe9b7fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924158"
---
# <span data-ttu-id="14a03-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14a03-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="14a03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14a03-102">SYNOPSIS</span></span>
<span data-ttu-id="14a03-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="14a03-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="14a03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14a03-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a03-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14a03-105">DESCRIPTION</span></span>
<span data-ttu-id="14a03-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="14a03-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="14a03-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14a03-107">EXAMPLES</span></span>

### <span data-ttu-id="14a03-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="14a03-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="14a03-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="14a03-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="14a03-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14a03-110">PARAMETERS</span></span>

### <span data-ttu-id="14a03-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14a03-111">-AsJob</span></span>
<span data-ttu-id="14a03-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="14a03-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14a03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a03-113">-DefaultProfile</span></span>
<span data-ttu-id="14a03-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="14a03-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a03-115">-Force</span><span class="sxs-lookup"><span data-stu-id="14a03-115">-Force</span></span>
<span data-ttu-id="14a03-116">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="14a03-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="14a03-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="14a03-117">-RouteFilter</span></span>
<span data-ttu-id="14a03-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="14a03-118">The RouteFilter</span></span>

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

### <span data-ttu-id="14a03-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14a03-119">-Confirm</span></span>
<span data-ttu-id="14a03-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14a03-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a03-121">-WhatIf</span></span>
<span data-ttu-id="14a03-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14a03-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14a03-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14a03-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a03-124">CommonParameters</span></span>
<span data-ttu-id="14a03-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a03-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a03-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a03-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14a03-127">INPUTS</span></span>

### <span data-ttu-id="14a03-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14a03-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="14a03-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14a03-129">OUTPUTS</span></span>

### <span data-ttu-id="14a03-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="14a03-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="14a03-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14a03-131">NOTES</span></span>

## <span data-ttu-id="14a03-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14a03-132">RELATED LINKS</span></span>

