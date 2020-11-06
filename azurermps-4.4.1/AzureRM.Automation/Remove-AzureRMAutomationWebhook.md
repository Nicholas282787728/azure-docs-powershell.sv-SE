---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: f191176433a5ac12507d2b29a6d52c73a1d61e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579807"
---
# <span data-ttu-id="57e72-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="57e72-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="57e72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57e72-102">SYNOPSIS</span></span>
<span data-ttu-id="57e72-103">Tar bort en webhook från en Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="57e72-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57e72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57e72-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57e72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57e72-105">DESCRIPTION</span></span>
<span data-ttu-id="57e72-106">Cmdleten **Remove-AzureRmAutomationWebhook** tar bort en webhook från en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="57e72-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="57e72-107">Webhooken tas bort.</span><span class="sxs-lookup"><span data-stu-id="57e72-107">The webhook is deleted.</span></span>

## <span data-ttu-id="57e72-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57e72-108">EXAMPLES</span></span>

### <span data-ttu-id="57e72-109">Exempel 1: ta bort en webhook</span><span class="sxs-lookup"><span data-stu-id="57e72-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="57e72-110">Det här kommandot tar bort en webhook med namnet Webhook11 i Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="57e72-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="57e72-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="57e72-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="57e72-112">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="57e72-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="57e72-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57e72-113">PARAMETERS</span></span>

### <span data-ttu-id="57e72-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57e72-114">-AutomationAccountName</span></span>
<span data-ttu-id="57e72-115">Anger namnet på ett Automation-konto som den här cmdleten tar bort en webhook från.</span><span class="sxs-lookup"><span data-stu-id="57e72-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="57e72-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="57e72-116">-Name</span></span>
<span data-ttu-id="57e72-117">Anger namnet på den webhook som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="57e72-117">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="57e72-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e72-118">-ResourceGroupName</span></span>
<span data-ttu-id="57e72-119">Anger namnet på den resurs grupp som denna cmdlet tar bort en webhook för.</span><span class="sxs-lookup"><span data-stu-id="57e72-119">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="57e72-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57e72-120">-Confirm</span></span>
<span data-ttu-id="57e72-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57e72-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e72-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e72-122">-WhatIf</span></span>
<span data-ttu-id="57e72-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57e72-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57e72-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57e72-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e72-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e72-125">-DefaultProfile</span></span>
<span data-ttu-id="57e72-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57e72-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e72-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e72-127">CommonParameters</span></span>
<span data-ttu-id="57e72-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e72-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e72-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e72-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e72-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57e72-130">INPUTS</span></span>

## <span data-ttu-id="57e72-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57e72-131">OUTPUTS</span></span>

## <span data-ttu-id="57e72-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57e72-132">NOTES</span></span>

## <span data-ttu-id="57e72-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57e72-133">RELATED LINKS</span></span>

[<span data-ttu-id="57e72-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="57e72-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="57e72-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="57e72-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="57e72-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="57e72-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


