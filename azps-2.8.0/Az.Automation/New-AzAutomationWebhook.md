---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 94bc498caa5052df5aa9a9e7724ecb87d253d9f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745508"
---
# <span data-ttu-id="1ee6d-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="1ee6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ee6d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee6d-103">Skapar en webhook för en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="1ee6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ee6d-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ee6d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ee6d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee6d-106">Cmdleten **New-AzAutomationWebhook** skapar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="1ee6d-107">Glöm inte att spara webhook-URL: en som denna cmdlet returnerar eftersom den inte kan hämtas igen.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="1ee6d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ee6d-108">EXAMPLES</span></span>

### <span data-ttu-id="1ee6d-109">Exempel 1: skapa en webhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="1ee6d-110">Det här kommandot skapar en webhook med namnet Webhook06 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1ee6d-111">Kommandot lagrar webhooken i $Webhook variabel.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="1ee6d-112">Webhook är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-112">The webhook is enabled.</span></span>
<span data-ttu-id="1ee6d-113">Webhooken upphör vid den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="1ee6d-114">Det här kommandot ger inga värden för webhook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="1ee6d-115">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="1ee6d-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1ee6d-116">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="1ee6d-117">Exempel 2: skapa en webhook med parametrar</span><span class="sxs-lookup"><span data-stu-id="1ee6d-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="1ee6d-118">Det första kommandot skapar en ord lista med parametrar och lagrar dem i $Params variabeln.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="1ee6d-119">Det andra kommandot skapar en webhook med namnet Webhook11 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="1ee6d-120">Kommandot tilldelar parametrarna i $Params till webhooken.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="1ee6d-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ee6d-121">PARAMETERS</span></span>

### <span data-ttu-id="1ee6d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ee6d-122">-AutomationAccountName</span></span>
<span data-ttu-id="1ee6d-123">Anger namnet på ett Automation-konto där denna cmdlet skapar en webhook.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="1ee6d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee6d-124">-DefaultProfile</span></span>
<span data-ttu-id="1ee6d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1ee6d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ee6d-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1ee6d-126">-ExpiryTime</span></span>
<span data-ttu-id="1ee6d-127">Anger förfallo tiden för webhooken som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1ee6d-128">Du kan ange en sträng eller **datum/tid** som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee6d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="1ee6d-129">-Force</span></span>
<span data-ttu-id="1ee6d-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="1ee6d-130">ps_force</span></span>

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

### <span data-ttu-id="1ee6d-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="1ee6d-131">-IsEnabled</span></span>
<span data-ttu-id="1ee6d-132">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee6d-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ee6d-133">-Name</span></span>
<span data-ttu-id="1ee6d-134">Anger ett namn för webhooken.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="1ee6d-135">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="1ee6d-135">-Parameters</span></span>
<span data-ttu-id="1ee6d-136">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="1ee6d-137">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="1ee6d-138">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="1ee6d-139">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee6d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee6d-140">-ResourceGroupName</span></span>
<span data-ttu-id="1ee6d-141">Anger namnet på den resurs grupp som den här cmdleten skapar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="1ee6d-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1ee6d-142">-RunbookName</span></span>
<span data-ttu-id="1ee6d-143">Anger namnet på den Runbook som ska kopplas till webhooken.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee6d-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="1ee6d-144">-RunOn</span></span>
<span data-ttu-id="1ee6d-145">Valfritt namn på Hybrid Worker-gruppen som ska köra runbook-flödet</span><span class="sxs-lookup"><span data-stu-id="1ee6d-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="1ee6d-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1ee6d-146">-Confirm</span></span>
<span data-ttu-id="1ee6d-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ee6d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ee6d-148">-WhatIf</span></span>
<span data-ttu-id="1ee6d-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ee6d-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ee6d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee6d-151">CommonParameters</span></span>
<span data-ttu-id="1ee6d-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ee6d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee6d-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ee6d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee6d-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ee6d-154">INPUTS</span></span>

### <span data-ttu-id="1ee6d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1ee6d-155">System.String</span></span>

### <span data-ttu-id="1ee6d-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee6d-156">System.Boolean</span></span>

### <span data-ttu-id="1ee6d-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1ee6d-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="1ee6d-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ee6d-158">OUTPUTS</span></span>

### <span data-ttu-id="1ee6d-159">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="1ee6d-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ee6d-160">NOTES</span></span>

## <span data-ttu-id="1ee6d-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ee6d-161">RELATED LINKS</span></span>

[<span data-ttu-id="1ee6d-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="1ee6d-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="1ee6d-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1ee6d-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)

