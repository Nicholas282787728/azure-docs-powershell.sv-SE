---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 93c51e71cf912a072daafd721d9e9626ccefbb06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929877"
---
# <span data-ttu-id="9eba3-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9eba3-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="9eba3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eba3-102">SYNOPSIS</span></span>
<span data-ttu-id="9eba3-103">Tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9eba3-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eba3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eba3-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eba3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eba3-105">DESCRIPTION</span></span>
<span data-ttu-id="9eba3-106">Cmdleten **Remove-AzureRmAutoscaleSetting** tar bort en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="9eba3-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="9eba3-107">Du måste ange namnet på inställningen och namnet på resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="9eba3-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>
<span data-ttu-id="9eba3-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="9eba3-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9eba3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eba3-109">EXAMPLES</span></span>

## <span data-ttu-id="9eba3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eba3-110">PARAMETERS</span></span>

### <span data-ttu-id="9eba3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eba3-111">-DefaultProfile</span></span>
<span data-ttu-id="9eba3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9eba3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eba3-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eba3-113">-Name</span></span>
<span data-ttu-id="9eba3-114">Anger namnet på den autoskalningsinställning som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="9eba3-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eba3-115">-ResourceGroupName</span></span>
<span data-ttu-id="9eba3-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9eba3-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9eba3-117">-Confirm</span></span>
<span data-ttu-id="9eba3-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9eba3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eba3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eba3-119">-WhatIf</span></span>
<span data-ttu-id="9eba3-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9eba3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9eba3-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9eba3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eba3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eba3-122">CommonParameters</span></span>
<span data-ttu-id="9eba3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eba3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eba3-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eba3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eba3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eba3-125">INPUTS</span></span>

### <span data-ttu-id="9eba3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9eba3-126">System.String</span></span>

## <span data-ttu-id="9eba3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eba3-127">OUTPUTS</span></span>

### <span data-ttu-id="9eba3-128">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9eba3-128">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9eba3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eba3-129">NOTES</span></span>

## <span data-ttu-id="9eba3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eba3-130">RELATED LINKS</span></span>

[<span data-ttu-id="9eba3-131">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9eba3-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9eba3-132">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9eba3-132">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


