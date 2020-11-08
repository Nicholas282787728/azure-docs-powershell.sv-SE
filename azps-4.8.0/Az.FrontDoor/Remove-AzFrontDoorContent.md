---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262247"
---
# <span data-ttu-id="2de7f-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="2de7f-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="2de7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2de7f-102">SYNOPSIS</span></span>
<span data-ttu-id="2de7f-103">Ta bort innehåll i front dörren</span><span class="sxs-lookup"><span data-stu-id="2de7f-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="2de7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2de7f-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2de7f-105">DESCRIPTION</span></span>
<span data-ttu-id="2de7f-106">Remove-AzFrontDoorContent rensar cachelagrat innehåll i en dörr</span><span class="sxs-lookup"><span data-stu-id="2de7f-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="2de7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2de7f-107">EXAMPLES</span></span>

### <span data-ttu-id="2de7f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2de7f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="2de7f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2de7f-109">PARAMETERS</span></span>

### <span data-ttu-id="2de7f-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="2de7f-110">-ContentPath</span></span>
<span data-ttu-id="2de7f-111">Sök vägarna till innehållet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2de7f-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de7f-112">-DefaultProfile</span></span>
<span data-ttu-id="2de7f-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2de7f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de7f-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2de7f-114">-Name</span></span>
<span data-ttu-id="2de7f-115">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="2de7f-115">Front Door name.</span></span>

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

### <span data-ttu-id="2de7f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2de7f-116">-PassThru</span></span>
<span data-ttu-id="2de7f-117">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="2de7f-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="2de7f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de7f-118">-ResourceGroupName</span></span>
<span data-ttu-id="2de7f-119">Namnet på den som är resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="2de7f-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="2de7f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2de7f-120">-Confirm</span></span>
<span data-ttu-id="2de7f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2de7f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de7f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de7f-122">-WhatIf</span></span>
<span data-ttu-id="2de7f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2de7f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2de7f-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2de7f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de7f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de7f-125">CommonParameters</span></span>
<span data-ttu-id="2de7f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de7f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de7f-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2de7f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de7f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2de7f-128">INPUTS</span></span>

### <span data-ttu-id="2de7f-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="2de7f-129">None</span></span>

## <span data-ttu-id="2de7f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2de7f-130">OUTPUTS</span></span>

### <span data-ttu-id="2de7f-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2de7f-131">System.Boolean</span></span>

## <span data-ttu-id="2de7f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2de7f-132">NOTES</span></span>

## <span data-ttu-id="2de7f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2de7f-133">RELATED LINKS</span></span>
