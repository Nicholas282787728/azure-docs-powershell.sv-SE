---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758342"
---
# <span data-ttu-id="cdb6e-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cdb6e-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="cdb6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb6e-103">Tar bort en webhook från en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdb6e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb6e-106">Cmdleten **Remove-AzureRmAutomationWebhook** tar bort en webhook från en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="cdb6e-107">Webhooken tas bort.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-107">The webhook is deleted.</span></span>

## <span data-ttu-id="cdb6e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdb6e-108">EXAMPLES</span></span>

### <span data-ttu-id="cdb6e-109">Exempel 1: ta bort en webhook</span><span class="sxs-lookup"><span data-stu-id="cdb6e-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="cdb6e-110">Det här kommandot tar bort en webhook med namnet Webhook11 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="cdb6e-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="cdb6e-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cdb6e-112">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cdb6e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdb6e-113">PARAMETERS</span></span>

### <span data-ttu-id="cdb6e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cdb6e-114">-AutomationAccountName</span></span>
<span data-ttu-id="cdb6e-115">Anger namnet på ett Automation-konto som den här cmdleten tar bort en webhook från.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="cdb6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb6e-116">-DefaultProfile</span></span>
<span data-ttu-id="cdb6e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cdb6e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdb6e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="cdb6e-118">-Name</span></span>
<span data-ttu-id="cdb6e-119">Anger namnet på den webhook som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cdb6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="cdb6e-121">Anger namnet på den resurs grupp som denna cmdlet tar bort en webhook för.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="cdb6e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdb6e-122">-Confirm</span></span>
<span data-ttu-id="cdb6e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb6e-124">-WhatIf</span></span>
<span data-ttu-id="cdb6e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb6e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb6e-127">CommonParameters</span></span>
<span data-ttu-id="cdb6e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb6e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb6e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb6e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdb6e-130">INPUTS</span></span>

### <span data-ttu-id="cdb6e-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="cdb6e-131">None</span></span>
<span data-ttu-id="cdb6e-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cdb6e-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdb6e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdb6e-133">OUTPUTS</span></span>

## <span data-ttu-id="cdb6e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdb6e-134">NOTES</span></span>

## <span data-ttu-id="cdb6e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdb6e-135">RELATED LINKS</span></span>

[<span data-ttu-id="cdb6e-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cdb6e-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="cdb6e-137">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cdb6e-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="cdb6e-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cdb6e-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


