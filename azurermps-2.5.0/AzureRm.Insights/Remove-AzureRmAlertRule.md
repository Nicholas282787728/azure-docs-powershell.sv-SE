---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: b0fc044ee2a4704c9bb6803ab0cf7a4be4ea95e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929898"
---
# <span data-ttu-id="c3720-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3720-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="c3720-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3720-102">SYNOPSIS</span></span>
<span data-ttu-id="c3720-103">Tar bort en varnings regel.</span><span class="sxs-lookup"><span data-stu-id="c3720-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3720-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3720-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3720-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3720-105">DESCRIPTION</span></span>
<span data-ttu-id="c3720-106">Cmdleten **Remove-AzureRmAlertRule** tar bort en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="c3720-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="c3720-107">Du måste ange namnet på notifieringsregeln och resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c3720-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="c3720-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="c3720-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c3720-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3720-109">EXAMPLES</span></span>

### <span data-ttu-id="c3720-110">Exempel 1: ta bort en notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="c3720-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="c3720-111">Med det här kommandot tas notifieringsregeln bort med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8 i resurs gruppens standard webb-centrala.</span><span class="sxs-lookup"><span data-stu-id="c3720-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="c3720-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3720-112">PARAMETERS</span></span>

### <span data-ttu-id="c3720-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3720-113">-DefaultProfile</span></span>
<span data-ttu-id="c3720-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c3720-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3720-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3720-115">-Name</span></span>
<span data-ttu-id="c3720-116">Anger namnet på den notifieringsregel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c3720-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="c3720-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3720-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3720-118">Anger namnet på resurs gruppen för notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="c3720-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="c3720-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3720-119">-Confirm</span></span>
<span data-ttu-id="c3720-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3720-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3720-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3720-121">-WhatIf</span></span>
<span data-ttu-id="c3720-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3720-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3720-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3720-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3720-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3720-124">CommonParameters</span></span>
<span data-ttu-id="c3720-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3720-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3720-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3720-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3720-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3720-127">INPUTS</span></span>

### <span data-ttu-id="c3720-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c3720-128">System.String</span></span>

## <span data-ttu-id="c3720-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3720-129">OUTPUTS</span></span>

### <span data-ttu-id="c3720-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c3720-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c3720-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3720-131">NOTES</span></span>

## <span data-ttu-id="c3720-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3720-132">RELATED LINKS</span></span>

[<span data-ttu-id="c3720-133">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3720-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c3720-134">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3720-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c3720-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c3720-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c3720-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c3720-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


