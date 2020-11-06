---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585184"
---
# <span data-ttu-id="e451f-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e451f-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="e451f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e451f-102">SYNOPSIS</span></span>
<span data-ttu-id="e451f-103">Skapar en webhook för en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="e451f-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e451f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e451f-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e451f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e451f-105">DESCRIPTION</span></span>
<span data-ttu-id="e451f-106">Cmdleten **New-AzureRmAutomationWebhook** skapar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="e451f-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="e451f-107">Glöm inte att spara webhook-URL: en som denna cmdlet returnerar eftersom den inte kan hämtas igen.</span><span class="sxs-lookup"><span data-stu-id="e451f-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="e451f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e451f-108">EXAMPLES</span></span>

### <span data-ttu-id="e451f-109">Exempel 1: skapa en webhook</span><span class="sxs-lookup"><span data-stu-id="e451f-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e451f-110">Det här kommandot skapar en webhook med namnet Webhook06 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e451f-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e451f-111">Kommandot lagrar webhooken i $Webhook variabel.</span><span class="sxs-lookup"><span data-stu-id="e451f-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="e451f-112">Webhook är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="e451f-112">The webhook is enabled.</span></span>
<span data-ttu-id="e451f-113">Webhooken upphör vid den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="e451f-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="e451f-114">Det här kommandot ger inga värden för webhook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="e451f-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="e451f-115">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="e451f-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e451f-116">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e451f-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e451f-117">Exempel 2: skapa en webhook med parametrar</span><span class="sxs-lookup"><span data-stu-id="e451f-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="e451f-118">Det första kommandot skapar en ord lista med parametrar och lagrar dem i $Params variabeln.</span><span class="sxs-lookup"><span data-stu-id="e451f-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="e451f-119">Det andra kommandot skapar en webhook med namnet Webhook11 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="e451f-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="e451f-120">Kommandot tilldelar parametrarna i $Params till webhooken.</span><span class="sxs-lookup"><span data-stu-id="e451f-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="e451f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e451f-121">PARAMETERS</span></span>

### <span data-ttu-id="e451f-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e451f-122">-AutomationAccountName</span></span>
<span data-ttu-id="e451f-123">Anger namnet på ett Automation-konto där denna cmdlet skapar en webhook.</span><span class="sxs-lookup"><span data-stu-id="e451f-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e451f-124">-DefaultProfile</span></span>
<span data-ttu-id="e451f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e451f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e451f-126">-ExpiryTime</span></span>
<span data-ttu-id="e451f-127">Anger förfallo tiden för webhooken som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e451f-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="e451f-128">Du kan ange en sträng eller **datum/tid** som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="e451f-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e451f-129">-Force</span></span>
<span data-ttu-id="e451f-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="e451f-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e451f-131">-IsEnabled</span></span>
<span data-ttu-id="e451f-132">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="e451f-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="e451f-133">-Name</span></span>
<span data-ttu-id="e451f-134">Anger ett namn för webhooken.</span><span class="sxs-lookup"><span data-stu-id="e451f-134">Specifies a name for the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-135">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="e451f-135">-Parameters</span></span>
<span data-ttu-id="e451f-136">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="e451f-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e451f-137">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="e451f-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e451f-138">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="e451f-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e451f-139">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="e451f-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e451f-140">-ResourceGroupName</span></span>
<span data-ttu-id="e451f-141">Anger namnet på den resurs grupp som den här cmdleten skapar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="e451f-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e451f-142">-RunbookName</span></span>
<span data-ttu-id="e451f-143">Anger namnet på den Runbook som ska kopplas till webhooken.</span><span class="sxs-lookup"><span data-stu-id="e451f-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e451f-144">-RunOn</span></span>
<span data-ttu-id="e451f-145">Valfritt namn på Hybrid Worker-gruppen som ska köra runbook-flödet</span><span class="sxs-lookup"><span data-stu-id="e451f-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e451f-146">-Confirm</span></span>
<span data-ttu-id="e451f-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e451f-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e451f-148">-WhatIf</span></span>
<span data-ttu-id="e451f-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e451f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e451f-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e451f-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e451f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e451f-151">CommonParameters</span></span>
<span data-ttu-id="e451f-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e451f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e451f-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e451f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e451f-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e451f-154">INPUTS</span></span>

### <span data-ttu-id="e451f-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="e451f-155">None</span></span>
<span data-ttu-id="e451f-156">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e451f-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e451f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e451f-157">OUTPUTS</span></span>

### <span data-ttu-id="e451f-158">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="e451f-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e451f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e451f-159">NOTES</span></span>

## <span data-ttu-id="e451f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e451f-160">RELATED LINKS</span></span>

[<span data-ttu-id="e451f-161">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e451f-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e451f-162">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e451f-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="e451f-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e451f-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


