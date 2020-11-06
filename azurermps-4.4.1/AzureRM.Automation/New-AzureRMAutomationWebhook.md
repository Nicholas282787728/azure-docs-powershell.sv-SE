---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579835"
---
# <span data-ttu-id="a217e-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a217e-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="a217e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a217e-102">SYNOPSIS</span></span>
<span data-ttu-id="a217e-103">Skapar en webhook för en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="a217e-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a217e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a217e-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a217e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a217e-105">DESCRIPTION</span></span>
<span data-ttu-id="a217e-106">Cmdleten **New-AzureRmAutomationWebhook** skapar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="a217e-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="a217e-107">Glöm inte att spara webhook-URL: en som denna cmdlet returnerar eftersom den inte kan hämtas igen.</span><span class="sxs-lookup"><span data-stu-id="a217e-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="a217e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a217e-108">EXAMPLES</span></span>

### <span data-ttu-id="a217e-109">Exempel 1: skapa en webhook</span><span class="sxs-lookup"><span data-stu-id="a217e-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a217e-110">Det här kommandot skapar en webhook med namnet Webhook06 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a217e-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a217e-111">Kommandot lagrar webhooken i $Webhook variabel.</span><span class="sxs-lookup"><span data-stu-id="a217e-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="a217e-112">Webhook är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="a217e-112">The webhook is enabled.</span></span>
<span data-ttu-id="a217e-113">Webhooken upphör vid den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="a217e-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="a217e-114">Det här kommandot ger inga värden för webhook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="a217e-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="a217e-115">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="a217e-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a217e-116">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a217e-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a217e-117">Exempel 2: skapa en webhook med parametrar</span><span class="sxs-lookup"><span data-stu-id="a217e-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a217e-118">Det första kommandot skapar en ord lista med parametrar och lagrar dem i $Params variabeln.</span><span class="sxs-lookup"><span data-stu-id="a217e-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="a217e-119">Det andra kommandot skapar en webhook med namnet Webhook11 för Runbook-flödet som heter ContosoRunbook i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a217e-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a217e-120">Kommandot tilldelar parametrarna i $Params till webhooken.</span><span class="sxs-lookup"><span data-stu-id="a217e-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="a217e-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a217e-121">PARAMETERS</span></span>

### <span data-ttu-id="a217e-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a217e-122">-AutomationAccountName</span></span>
<span data-ttu-id="a217e-123">Anger namnet på ett Automation-konto där denna cmdlet skapar en webhook.</span><span class="sxs-lookup"><span data-stu-id="a217e-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a217e-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a217e-124">-ExpiryTime</span></span>
<span data-ttu-id="a217e-125">Anger förfallo tiden för webhooken som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a217e-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a217e-126">Du kan ange en sträng eller **datum/tid** som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="a217e-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="a217e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="a217e-127">-Force</span></span>
<span data-ttu-id="a217e-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="a217e-128">ps_force</span></span>

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

### <span data-ttu-id="a217e-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a217e-129">-IsEnabled</span></span>
<span data-ttu-id="a217e-130">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="a217e-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="a217e-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="a217e-131">-Name</span></span>
<span data-ttu-id="a217e-132">Anger ett namn för webhooken.</span><span class="sxs-lookup"><span data-stu-id="a217e-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="a217e-133">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="a217e-133">-Parameters</span></span>
<span data-ttu-id="a217e-134">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="a217e-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a217e-135">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="a217e-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a217e-136">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="a217e-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a217e-137">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="a217e-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="a217e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a217e-138">-ResourceGroupName</span></span>
<span data-ttu-id="a217e-139">Anger namnet på den resurs grupp som den här cmdleten skapar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="a217e-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a217e-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a217e-140">-RunbookName</span></span>
<span data-ttu-id="a217e-141">Anger namnet på den Runbook som ska kopplas till webhooken.</span><span class="sxs-lookup"><span data-stu-id="a217e-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="a217e-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="a217e-142">-RunOn</span></span>
<span data-ttu-id="a217e-143">Valfritt namn på Hybrid agenten som ska köra runbook-flödet</span><span class="sxs-lookup"><span data-stu-id="a217e-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="a217e-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a217e-144">-Confirm</span></span>
<span data-ttu-id="a217e-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a217e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a217e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a217e-146">-WhatIf</span></span>
<span data-ttu-id="a217e-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a217e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a217e-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a217e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a217e-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a217e-149">-DefaultProfile</span></span>
<span data-ttu-id="a217e-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a217e-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a217e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a217e-151">CommonParameters</span></span>
<span data-ttu-id="a217e-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a217e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a217e-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a217e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a217e-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a217e-154">INPUTS</span></span>

## <span data-ttu-id="a217e-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a217e-155">OUTPUTS</span></span>

### <span data-ttu-id="a217e-156">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="a217e-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a217e-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a217e-157">NOTES</span></span>

## <span data-ttu-id="a217e-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a217e-158">RELATED LINKS</span></span>

[<span data-ttu-id="a217e-159">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a217e-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a217e-160">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a217e-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a217e-161">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a217e-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


