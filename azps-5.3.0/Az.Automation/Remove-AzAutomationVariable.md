---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524876"
---
# <span data-ttu-id="40e83-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="40e83-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="40e83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40e83-102">SYNOPSIS</span></span>
<span data-ttu-id="40e83-103">Tar bort en Automation-variabel.</span><span class="sxs-lookup"><span data-stu-id="40e83-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="40e83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40e83-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40e83-105">DESCRIPTION</span></span>
<span data-ttu-id="40e83-106">Cmdleten **Remove-AzAutomationVariable** tar bort en variabel från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="40e83-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="40e83-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40e83-107">EXAMPLES</span></span>

### <span data-ttu-id="40e83-108">Exempel 1: ta bort en variabel</span><span class="sxs-lookup"><span data-stu-id="40e83-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="40e83-109">Det här kommandot tar bort en variabel som heter StringVariable22 i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="40e83-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="40e83-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="40e83-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="40e83-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="40e83-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="40e83-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40e83-112">PARAMETERS</span></span>

### <span data-ttu-id="40e83-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40e83-113">-AutomationAccountName</span></span>
<span data-ttu-id="40e83-114">Anger namnet på det Automation-konto som innehåller den variabel som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="40e83-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="40e83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e83-115">-DefaultProfile</span></span>
<span data-ttu-id="40e83-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40e83-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40e83-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="40e83-117">-Name</span></span>
<span data-ttu-id="40e83-118">Anger namnet på den variabel som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="40e83-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="40e83-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e83-119">-ResourceGroupName</span></span>
<span data-ttu-id="40e83-120">Anger den resurs grupp för vilken denna cmdlet tar bort en variabel.</span><span class="sxs-lookup"><span data-stu-id="40e83-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="40e83-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40e83-121">-Confirm</span></span>
<span data-ttu-id="40e83-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40e83-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e83-123">-WhatIf</span></span>
<span data-ttu-id="40e83-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40e83-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e83-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40e83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e83-126">CommonParameters</span></span>
<span data-ttu-id="40e83-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e83-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e83-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e83-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40e83-129">INPUTS</span></span>

### <span data-ttu-id="40e83-130">System. String</span><span class="sxs-lookup"><span data-stu-id="40e83-130">System.String</span></span>

## <span data-ttu-id="40e83-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40e83-131">OUTPUTS</span></span>

### <span data-ttu-id="40e83-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="40e83-132">System.Void</span></span>

## <span data-ttu-id="40e83-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40e83-133">NOTES</span></span>

## <span data-ttu-id="40e83-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40e83-134">RELATED LINKS</span></span>

[<span data-ttu-id="40e83-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="40e83-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="40e83-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="40e83-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="40e83-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="40e83-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


