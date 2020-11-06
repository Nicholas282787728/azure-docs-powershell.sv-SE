---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575961"
---
# <span data-ttu-id="9c27f-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c27f-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9c27f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9c27f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c27f-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="9c27f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c27f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9c27f-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c27f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9c27f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c27f-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="9c27f-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9c27f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9c27f-107">EXAMPLES</span></span>

### <span data-ttu-id="9c27f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9c27f-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9c27f-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="9c27f-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9c27f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9c27f-110">PARAMETERS</span></span>

### <span data-ttu-id="9c27f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9c27f-111">-Force</span></span>
<span data-ttu-id="9c27f-112">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="9c27f-112">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c27f-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c27f-113">-RouteFilter</span></span>
<span data-ttu-id="9c27f-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c27f-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c27f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9c27f-115">-Confirm</span></span>
<span data-ttu-id="9c27f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9c27f-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c27f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c27f-117">-WhatIf</span></span>
<span data-ttu-id="9c27f-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9c27f-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c27f-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9c27f-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c27f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c27f-120">-DefaultProfile</span></span>
<span data-ttu-id="9c27f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9c27f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c27f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c27f-122">CommonParameters</span></span>
<span data-ttu-id="9c27f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c27f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c27f-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c27f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c27f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9c27f-125">INPUTS</span></span>

### <span data-ttu-id="9c27f-126">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c27f-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9c27f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9c27f-127">OUTPUTS</span></span>

### <span data-ttu-id="9c27f-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9c27f-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9c27f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9c27f-129">NOTES</span></span>

## <span data-ttu-id="9c27f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9c27f-130">RELATED LINKS</span></span>

