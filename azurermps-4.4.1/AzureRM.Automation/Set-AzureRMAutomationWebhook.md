---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575038"
---
# <span data-ttu-id="7f3e9-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="7f3e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7f3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3e9-103">Ändrar en webhook för en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f3e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7f3e9-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f3e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7f3e9-105">DESCRIPTION</span></span>
<span data-ttu-id="7f3e9-106">Cmdleten **set-AzureRmAutomationWebhook** ändrar en webhook för en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="7f3e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7f3e9-107">EXAMPLES</span></span>

### <span data-ttu-id="7f3e9-108">Exempel 1: inaktivera en webhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="7f3e9-109">Det här kommandot inaktiverar en webhook med namnet Webhook01 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="7f3e9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7f3e9-110">PARAMETERS</span></span>

### <span data-ttu-id="7f3e9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7f3e9-111">-AutomationAccountName</span></span>
<span data-ttu-id="7f3e9-112">Anger namnet på ett Automation-konto där denna cmdlet ändrar en webhook.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="7f3e9-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="7f3e9-113">-IsEnabled</span></span>
<span data-ttu-id="7f3e9-114">Anger om webhooken är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="7f3e9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="7f3e9-115">-Name</span></span>
<span data-ttu-id="7f3e9-116">Anger namnet på den webhook som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7f3e9-117">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="7f3e9-117">-Parameters</span></span>
<span data-ttu-id="7f3e9-118">Anger en ord lista med viktiga par.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="7f3e9-119">Nycklarna är namnen på Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="7f3e9-120">Värdena är värden för Runbook-parametrar.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="7f3e9-121">När Runbook startar som svar på en webhook skickas dessa parametrar till Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="7f3e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f3e9-123">Anger namnet på den resurs grupp som den här cmdleten ändrar en webhook för.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="7f3e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3e9-124">-DefaultProfile</span></span>
<span data-ttu-id="7f3e9-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3e9-126">CommonParameters</span></span>
<span data-ttu-id="7f3e9-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3e9-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f3e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3e9-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7f3e9-129">INPUTS</span></span>

## <span data-ttu-id="7f3e9-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7f3e9-130">OUTPUTS</span></span>

### <span data-ttu-id="7f3e9-131">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="7f3e9-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7f3e9-132">NOTES</span></span>

## <span data-ttu-id="7f3e9-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7f3e9-133">RELATED LINKS</span></span>

[<span data-ttu-id="7f3e9-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="7f3e9-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="7f3e9-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7f3e9-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


