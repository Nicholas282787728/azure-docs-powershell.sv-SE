---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 3622b7ad87658091d4b54af62678d12a324ef56a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931198"
---
# <span data-ttu-id="2d206-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d206-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2d206-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d206-102">SYNOPSIS</span></span>
<span data-ttu-id="2d206-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="2d206-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d206-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d206-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d206-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d206-105">DESCRIPTION</span></span>
<span data-ttu-id="2d206-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="2d206-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2d206-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d206-107">EXAMPLES</span></span>

### <span data-ttu-id="2d206-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2d206-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2d206-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="2d206-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2d206-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d206-110">PARAMETERS</span></span>

### <span data-ttu-id="2d206-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d206-111">-DefaultProfile</span></span>
<span data-ttu-id="2d206-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d206-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d206-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2d206-113">-Force</span></span>
<span data-ttu-id="2d206-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2d206-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2d206-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d206-115">-Name</span></span>
<span data-ttu-id="2d206-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="2d206-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d206-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d206-117">-PassThru</span></span>
<span data-ttu-id="2d206-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2d206-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d206-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d206-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d206-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2d206-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d206-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d206-121">-Confirm</span></span>
<span data-ttu-id="2d206-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d206-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d206-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d206-123">-WhatIf</span></span>
<span data-ttu-id="2d206-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d206-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d206-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d206-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d206-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d206-126">CommonParameters</span></span>
<span data-ttu-id="2d206-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d206-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d206-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d206-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d206-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d206-129">INPUTS</span></span>

### <span data-ttu-id="2d206-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d206-130">System.String</span></span>

## <span data-ttu-id="2d206-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d206-131">OUTPUTS</span></span>

### <span data-ttu-id="2d206-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="2d206-132">System.Object</span></span>

## <span data-ttu-id="2d206-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d206-133">NOTES</span></span>

## <span data-ttu-id="2d206-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d206-134">RELATED LINKS</span></span>

