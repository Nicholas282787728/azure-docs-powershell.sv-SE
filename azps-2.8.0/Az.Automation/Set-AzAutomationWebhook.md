---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745450"
---
# <span data-ttu-id="936bf-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="936bf-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="936bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="936bf-102">SYNOPSIS</span></span>
<span data-ttu-id="936bf-103">Ändrar en webhook för en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="936bf-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="936bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="936bf-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="936bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="936bf-105">DESCRIPTION</span></span>
<span data-ttu-id="936bf-106">Cmdleten **set-AzAutomationWebhook** ändrar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="936bf-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="936bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="936bf-107">EXAMPLES</span></span>

### <span data-ttu-id="936bf-108">Exempel 1: inaktivera en webhook</span><span class="sxs-lookup"><span data-stu-id="936bf-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="936bf-109">Det här kommandot inaktiverar en webhook med namnet Webhook01 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="936bf-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="936bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="936bf-110">PARAMETERS</span></span>

### <span data-ttu-id="936bf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="936bf-111">-AutomationAccountName</span></span>
<span data-ttu-id="936bf-112">Anger namnet på ett Automation-konto där denna cmdlet ändrar en webhook.</span><span class="sxs-lookup"><span data-stu-id="936bf-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="936bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936bf-113">-DefaultProfile</span></span>
<span data-ttu-id="936bf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="936bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="936bf-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="936bf-115">-IsEnabled</span></span>
<span data-ttu-id="936bf-116">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="936bf-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936bf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="936bf-117">-Name</span></span>
<span data-ttu-id="936bf-118">Anger namnet på den webhook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="936bf-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="936bf-119">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="936bf-119">-Parameters</span></span>
<span data-ttu-id="936bf-120">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="936bf-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="936bf-121">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="936bf-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="936bf-122">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="936bf-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="936bf-123">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="936bf-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="936bf-125">Anger namnet på den resurs grupp som den här cmdleten ändrar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="936bf-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="936bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936bf-126">CommonParameters</span></span>
<span data-ttu-id="936bf-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936bf-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936bf-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="936bf-129">INPUTS</span></span>

### <span data-ttu-id="936bf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="936bf-130">System.String</span></span>

### <span data-ttu-id="936bf-131">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="936bf-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="936bf-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="936bf-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="936bf-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="936bf-133">OUTPUTS</span></span>

### <span data-ttu-id="936bf-134">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="936bf-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="936bf-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="936bf-135">NOTES</span></span>

## <span data-ttu-id="936bf-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="936bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="936bf-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="936bf-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="936bf-138">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="936bf-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="936bf-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="936bf-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


