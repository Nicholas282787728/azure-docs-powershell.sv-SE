---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorContent.md
ms.openlocfilehash: c75d8bca528c954cf0612af3392fc79f3cd3b4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572751"
---
# <span data-ttu-id="512b7-101">Remove-AzureRmFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="512b7-101">Remove-AzureRmFrontDoorContent</span></span>

## <span data-ttu-id="512b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="512b7-102">SYNOPSIS</span></span>
<span data-ttu-id="512b7-103">Ta bort innehåll i front dörren</span><span class="sxs-lookup"><span data-stu-id="512b7-103">Remove contents in Front Door</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="512b7-104">SYNTAX</span></span>

```
Remove-AzureRmFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="512b7-105">DESCRIPTION</span></span>
<span data-ttu-id="512b7-106">Remove-AzureRmFrontDoorContent rensar cachelagrat innehåll i en dörr</span><span class="sxs-lookup"><span data-stu-id="512b7-106">Remove-AzureRmFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="512b7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="512b7-107">EXAMPLES</span></span>

### <span data-ttu-id="512b7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="512b7-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="512b7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="512b7-109">PARAMETERS</span></span>

### <span data-ttu-id="512b7-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="512b7-110">-ContentPath</span></span>
<span data-ttu-id="512b7-111">Sök vägarna till innehållet som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="512b7-111">The paths to the content to be purged.</span></span>

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

### <span data-ttu-id="512b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512b7-112">-DefaultProfile</span></span>
<span data-ttu-id="512b7-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="512b7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="512b7-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="512b7-114">-Name</span></span>
<span data-ttu-id="512b7-115">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="512b7-115">Front Door name.</span></span>

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

### <span data-ttu-id="512b7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="512b7-116">-PassThru</span></span>
<span data-ttu-id="512b7-117">Return-objekt (om angivet).</span><span class="sxs-lookup"><span data-stu-id="512b7-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="512b7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512b7-118">-ResourceGroupName</span></span>
<span data-ttu-id="512b7-119">Namnet på den som är resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="512b7-119">The resource group name of the Front Door</span></span>

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

### <span data-ttu-id="512b7-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="512b7-120">-Confirm</span></span>
<span data-ttu-id="512b7-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="512b7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512b7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512b7-122">-WhatIf</span></span>
<span data-ttu-id="512b7-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="512b7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512b7-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="512b7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512b7-125">CommonParameters</span></span>
<span data-ttu-id="512b7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512b7-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512b7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512b7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="512b7-128">INPUTS</span></span>

### <span data-ttu-id="512b7-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="512b7-129">None</span></span>

## <span data-ttu-id="512b7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="512b7-130">OUTPUTS</span></span>

### <span data-ttu-id="512b7-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="512b7-131">System.Boolean</span></span>

## <span data-ttu-id="512b7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="512b7-132">NOTES</span></span>

## <span data-ttu-id="512b7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="512b7-133">RELATED LINKS</span></span>
