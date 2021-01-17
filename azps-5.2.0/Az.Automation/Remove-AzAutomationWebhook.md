---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418299"
---
# <span data-ttu-id="42d1c-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="42d1c-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="42d1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="42d1c-103">Tar bort en webhook från en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="42d1c-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="42d1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42d1c-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d1c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="42d1c-106">Cmdleten **Remove-AzAutomationWebhook** tar bort en webhook från en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="42d1c-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="42d1c-107">Webhooken tas bort.</span><span class="sxs-lookup"><span data-stu-id="42d1c-107">The webhook is deleted.</span></span>

## <span data-ttu-id="42d1c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42d1c-108">EXAMPLES</span></span>

### <span data-ttu-id="42d1c-109">Exempel 1: ta bort en webhook</span><span class="sxs-lookup"><span data-stu-id="42d1c-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="42d1c-110">Det här kommandot tar bort en webhook med namnet Webhook11 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="42d1c-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="42d1c-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="42d1c-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="42d1c-112">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="42d1c-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="42d1c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42d1c-113">PARAMETERS</span></span>

### <span data-ttu-id="42d1c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42d1c-114">-AutomationAccountName</span></span>
<span data-ttu-id="42d1c-115">Anger namnet på ett Automation-konto som den här cmdleten tar bort en webhook från.</span><span class="sxs-lookup"><span data-stu-id="42d1c-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="42d1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d1c-116">-DefaultProfile</span></span>
<span data-ttu-id="42d1c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="42d1c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42d1c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="42d1c-118">-Name</span></span>
<span data-ttu-id="42d1c-119">Anger namnet på den webhook som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="42d1c-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="42d1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="42d1c-121">Anger namnet på den resurs grupp som denna cmdlet tar bort en webhook för.</span><span class="sxs-lookup"><span data-stu-id="42d1c-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="42d1c-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42d1c-122">-Confirm</span></span>
<span data-ttu-id="42d1c-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42d1c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d1c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d1c-124">-WhatIf</span></span>
<span data-ttu-id="42d1c-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42d1c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d1c-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42d1c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d1c-127">CommonParameters</span></span>
<span data-ttu-id="42d1c-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d1c-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d1c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d1c-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42d1c-130">INPUTS</span></span>

### <span data-ttu-id="42d1c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42d1c-131">System.String</span></span>

## <span data-ttu-id="42d1c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42d1c-132">OUTPUTS</span></span>

### <span data-ttu-id="42d1c-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="42d1c-133">System.Void</span></span>

## <span data-ttu-id="42d1c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42d1c-134">NOTES</span></span>

## <span data-ttu-id="42d1c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42d1c-135">RELATED LINKS</span></span>

[<span data-ttu-id="42d1c-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="42d1c-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="42d1c-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="42d1c-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="42d1c-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="42d1c-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


