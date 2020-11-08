---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088303"
---
# <span data-ttu-id="2d8a5-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="2d8a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8a5-103">Tar bort en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="2d8a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d8a5-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d8a5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8a5-106">Cmdleten **Remove-AzAutomationVariable** tar bort en variabel från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="2d8a5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-107">EXAMPLES</span></span>

### <span data-ttu-id="2d8a5-108">Exempel 1: ta bort en variabel</span><span class="sxs-lookup"><span data-stu-id="2d8a5-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d8a5-109">Det här kommandot tar bort en variabel som heter StringVariable22 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="2d8a5-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="2d8a5-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2d8a5-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2d8a5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-112">PARAMETERS</span></span>

### <span data-ttu-id="2d8a5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d8a5-113">-AutomationAccountName</span></span>
<span data-ttu-id="2d8a5-114">Anger namnet på det Automation-konto som innehåller den variabel som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-115">-DefaultProfile</span></span>
<span data-ttu-id="2d8a5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d8a5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-117">-Name</span></span>
<span data-ttu-id="2d8a5-118">Anger namnet på den variabel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="2d8a5-120">Anger den resurs grupp för vilken denna cmdlet tar bort en variabel.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a5-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d8a5-121">-Confirm</span></span>
<span data-ttu-id="2d8a5-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d8a5-123">-WhatIf</span></span>
<span data-ttu-id="2d8a5-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d8a5-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d8a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8a5-126">CommonParameters</span></span>
<span data-ttu-id="2d8a5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8a5-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8a5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8a5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-129">INPUTS</span></span>

### <span data-ttu-id="2d8a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d8a5-130">System.String</span></span>

## <span data-ttu-id="2d8a5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d8a5-131">OUTPUTS</span></span>

### <span data-ttu-id="2d8a5-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="2d8a5-132">System.Void</span></span>

## <span data-ttu-id="2d8a5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-133">NOTES</span></span>

## <span data-ttu-id="2d8a5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d8a5-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="2d8a5-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="2d8a5-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)

