---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269347"
---
# <span data-ttu-id="9dd52-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="9dd52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dd52-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd52-103">Ändrar en webhook för en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="9dd52-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="9dd52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dd52-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9dd52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dd52-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd52-106">Cmdleten **set-AzAutomationWebhook** ändrar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="9dd52-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="9dd52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dd52-107">EXAMPLES</span></span>

### <span data-ttu-id="9dd52-108">Exempel 1: inaktivera en webhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="9dd52-109">Det här kommandot inaktiverar en webhook med namnet Webhook01 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="9dd52-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="9dd52-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9dd52-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="9dd52-111">Det här kommandot anger värdet för kör för webhook och tvingar Runbook-flödet att köras på en hybrid Worker-grupp som heter Windows.</span><span class="sxs-lookup"><span data-stu-id="9dd52-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="9dd52-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9dd52-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="9dd52-113">Det här kommandot uppdaterar värdet för kör för webhook och tvingar Runbook-flödet att köras på en Azure Runbook Worker.</span><span class="sxs-lookup"><span data-stu-id="9dd52-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="9dd52-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dd52-114">PARAMETERS</span></span>

### <span data-ttu-id="9dd52-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9dd52-115">-AutomationAccountName</span></span>
<span data-ttu-id="9dd52-116">Anger namnet på ett Automation-konto där denna cmdlet ändrar en webhook.</span><span class="sxs-lookup"><span data-stu-id="9dd52-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9dd52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd52-117">-DefaultProfile</span></span>
<span data-ttu-id="9dd52-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9dd52-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd52-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9dd52-119">-IsEnabled</span></span>
<span data-ttu-id="9dd52-120">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="9dd52-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="9dd52-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="9dd52-121">-Name</span></span>
<span data-ttu-id="9dd52-122">Anger namnet på den webhook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9dd52-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9dd52-123">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="9dd52-123">-Parameters</span></span>
<span data-ttu-id="9dd52-124">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="9dd52-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="9dd52-125">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="9dd52-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="9dd52-126">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="9dd52-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="9dd52-127">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="9dd52-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="9dd52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd52-128">-ResourceGroupName</span></span>
<span data-ttu-id="9dd52-129">Anger namnet på den resurs grupp som den här cmdleten ändrar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="9dd52-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9dd52-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="9dd52-130">-RunOn</span></span>
<span data-ttu-id="9dd52-131">Valfritt namn på Hybrid agenten som ska köra runbook-flödet</span><span class="sxs-lookup"><span data-stu-id="9dd52-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd52-132">CommonParameters</span></span>
<span data-ttu-id="9dd52-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd52-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dd52-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd52-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dd52-135">INPUTS</span></span>

### <span data-ttu-id="9dd52-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9dd52-136">System.String</span></span>

### <span data-ttu-id="9dd52-137">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dd52-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9dd52-138">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9dd52-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9dd52-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dd52-139">OUTPUTS</span></span>

### <span data-ttu-id="9dd52-140">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9dd52-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dd52-141">NOTES</span></span>

## <span data-ttu-id="9dd52-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dd52-142">RELATED LINKS</span></span>

[<span data-ttu-id="9dd52-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="9dd52-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="9dd52-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9dd52-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


