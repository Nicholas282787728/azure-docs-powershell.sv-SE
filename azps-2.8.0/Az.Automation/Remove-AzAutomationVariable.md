---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: cfb8aa96da85cbfe1e9c16277c5c1c3539e04ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745472"
---
# <span data-ttu-id="c9eff-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9eff-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="c9eff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9eff-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eff-103">Tar bort en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="c9eff-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="c9eff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9eff-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9eff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9eff-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eff-106">Cmdleten **Remove-AzAutomationVariable** tar bort en variabel från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c9eff-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="c9eff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9eff-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eff-108">Exempel 1: ta bort en variabel</span><span class="sxs-lookup"><span data-stu-id="c9eff-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c9eff-109">Det här kommandot tar bort en variabel som heter StringVariable22 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c9eff-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c9eff-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="c9eff-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c9eff-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c9eff-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c9eff-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-112">PARAMETERS</span></span>

### <span data-ttu-id="c9eff-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9eff-113">-AutomationAccountName</span></span>
<span data-ttu-id="c9eff-114">Anger namnet på det Automation-konto som innehåller den variabel som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="c9eff-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c9eff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eff-115">-DefaultProfile</span></span>
<span data-ttu-id="c9eff-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9eff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9eff-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9eff-117">-Name</span></span>
<span data-ttu-id="c9eff-118">Anger namnet på den variabel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c9eff-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c9eff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9eff-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9eff-120">Anger den resurs grupp för vilken denna cmdlet tar bort en variabel.</span><span class="sxs-lookup"><span data-stu-id="c9eff-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="c9eff-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9eff-121">-Confirm</span></span>
<span data-ttu-id="c9eff-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9eff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9eff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9eff-123">-WhatIf</span></span>
<span data-ttu-id="c9eff-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9eff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9eff-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9eff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9eff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eff-126">CommonParameters</span></span>
<span data-ttu-id="c9eff-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eff-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eff-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eff-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9eff-129">INPUTS</span></span>

### <span data-ttu-id="c9eff-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c9eff-130">System.String</span></span>

## <span data-ttu-id="c9eff-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9eff-131">OUTPUTS</span></span>

### <span data-ttu-id="c9eff-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="c9eff-132">System.Void</span></span>

## <span data-ttu-id="c9eff-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-133">NOTES</span></span>

## <span data-ttu-id="c9eff-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9eff-134">RELATED LINKS</span></span>

[<span data-ttu-id="c9eff-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9eff-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="c9eff-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9eff-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="c9eff-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c9eff-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


