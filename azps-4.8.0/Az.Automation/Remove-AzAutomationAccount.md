---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261450"
---
# <span data-ttu-id="aba16-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aba16-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="aba16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aba16-102">SYNOPSIS</span></span>
<span data-ttu-id="aba16-103">Tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="aba16-103">Removes an Automation account.</span></span>

## <span data-ttu-id="aba16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aba16-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aba16-105">DESCRIPTION</span></span>
<span data-ttu-id="aba16-106">Cmdleten **Remove-AzAutomationAccount** tar bort ett Azure Automation-konto från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="aba16-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="aba16-107">Mer information om automatiserings konton finns i New-AzAutomationAccount cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aba16-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="aba16-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aba16-108">EXAMPLES</span></span>

### <span data-ttu-id="aba16-109">Exempel 1: ta bort ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="aba16-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aba16-110">Det här kommandot tar bort ett Automation-konto med namnet ContosoAutomationAccount utan att fråga efter användar verifiering.</span><span class="sxs-lookup"><span data-stu-id="aba16-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="aba16-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aba16-111">PARAMETERS</span></span>

### <span data-ttu-id="aba16-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba16-112">-DefaultProfile</span></span>
<span data-ttu-id="aba16-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aba16-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aba16-114">-Force</span><span class="sxs-lookup"><span data-stu-id="aba16-114">-Force</span></span>
<span data-ttu-id="aba16-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="aba16-115">ps_force</span></span>

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

### <span data-ttu-id="aba16-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="aba16-116">-Name</span></span>
<span data-ttu-id="aba16-117">Anger namnet på Automation-kontot som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="aba16-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba16-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba16-118">-ResourceGroupName</span></span>
<span data-ttu-id="aba16-119">Anger namnet på den resurs grupp från vilken denna cmdlet tar bort ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="aba16-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="aba16-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aba16-120">-Confirm</span></span>
<span data-ttu-id="aba16-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aba16-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba16-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba16-122">-WhatIf</span></span>
<span data-ttu-id="aba16-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aba16-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba16-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aba16-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba16-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba16-125">CommonParameters</span></span>
<span data-ttu-id="aba16-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba16-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba16-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba16-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba16-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aba16-128">INPUTS</span></span>

### <span data-ttu-id="aba16-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aba16-129">System.String</span></span>

## <span data-ttu-id="aba16-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aba16-130">OUTPUTS</span></span>

### <span data-ttu-id="aba16-131">Microsoft. Azure. commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aba16-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="aba16-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aba16-132">NOTES</span></span>

## <span data-ttu-id="aba16-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aba16-133">RELATED LINKS</span></span>

[<span data-ttu-id="aba16-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aba16-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="aba16-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aba16-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="aba16-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aba16-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)

