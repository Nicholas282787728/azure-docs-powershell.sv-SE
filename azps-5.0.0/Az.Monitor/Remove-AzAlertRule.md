---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273141"
---
# <span data-ttu-id="d69b3-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d69b3-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="d69b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d69b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d69b3-103">Tar bort en varnings regel.</span><span class="sxs-lookup"><span data-stu-id="d69b3-103">Removes an alert rule.</span></span>

## <span data-ttu-id="d69b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d69b3-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d69b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d69b3-105">DESCRIPTION</span></span>
<span data-ttu-id="d69b3-106">Cmdleten **Remove-AzAlertRule** tar bort en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="d69b3-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="d69b3-107">Du måste ange namnet på notifieringsregeln och resurs gruppen som den har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="d69b3-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="d69b3-108">Denna cmdlet implementerar ShouldProcess-mönstret, t. ex. det kan begära bekräftelse från användaren innan de skapar, ändrar eller tar bort resursen.</span><span class="sxs-lookup"><span data-stu-id="d69b3-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d69b3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d69b3-109">EXAMPLES</span></span>

### <span data-ttu-id="d69b3-110">Exempel 1: ta bort en notifieringsregel</span><span class="sxs-lookup"><span data-stu-id="d69b3-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="d69b3-111">Med det här kommandot tas notifieringsregeln bort med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8 i resurs gruppens standard webb-centrala.</span><span class="sxs-lookup"><span data-stu-id="d69b3-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="d69b3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d69b3-112">PARAMETERS</span></span>

### <span data-ttu-id="d69b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69b3-113">-DefaultProfile</span></span>
<span data-ttu-id="d69b3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d69b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d69b3-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d69b3-115">-Name</span></span>
<span data-ttu-id="d69b3-116">Anger namnet på den notifieringsregel som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d69b3-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="d69b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d69b3-118">Anger namnet på resurs gruppen för notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="d69b3-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="d69b3-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d69b3-119">-Confirm</span></span>
<span data-ttu-id="d69b3-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d69b3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69b3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69b3-121">-WhatIf</span></span>
<span data-ttu-id="d69b3-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d69b3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d69b3-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d69b3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69b3-124">CommonParameters</span></span>
<span data-ttu-id="d69b3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69b3-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d69b3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69b3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d69b3-127">INPUTS</span></span>

### <span data-ttu-id="d69b3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d69b3-128">System.String</span></span>

## <span data-ttu-id="d69b3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d69b3-129">OUTPUTS</span></span>

### <span data-ttu-id="d69b3-130">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d69b3-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="d69b3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d69b3-131">NOTES</span></span>

## <span data-ttu-id="d69b3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d69b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d69b3-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d69b3-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d69b3-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d69b3-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d69b3-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="d69b3-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="d69b3-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="d69b3-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


