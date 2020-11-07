---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 30ecb11822e622457600eb2a126171d431372f07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754815"
---
# <span data-ttu-id="78494-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="78494-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="78494-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="78494-102">SYNOPSIS</span></span>
<span data-ttu-id="78494-103">Hämtar webhookar från Automation.</span><span class="sxs-lookup"><span data-stu-id="78494-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="78494-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="78494-104">SYNTAX</span></span>

### <span data-ttu-id="78494-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="78494-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78494-106">ByName</span><span class="sxs-lookup"><span data-stu-id="78494-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78494-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="78494-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78494-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="78494-108">DESCRIPTION</span></span>
<span data-ttu-id="78494-109">Cmdleten **Get-AzAutomationWebhook** hämtar webhookar.</span><span class="sxs-lookup"><span data-stu-id="78494-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="78494-110">För att få specifika webhookar, ange ett webhook-namn eller ange namnet på en Azure Automation-Runbook för att få webhookarna anslutna.</span><span class="sxs-lookup"><span data-stu-id="78494-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="78494-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="78494-111">EXAMPLES</span></span>

### <span data-ttu-id="78494-112">Exempel 1: Hämta alla webhookar för en Runbook</span><span class="sxs-lookup"><span data-stu-id="78494-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="78494-113">Det här kommandot får alla Webhooks för en Runbook med namnet Runbook03 i Automation-kontot med namnet AutomationAccount01 i resurs gruppen som heter ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="78494-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="78494-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="78494-114">PARAMETERS</span></span>

### <span data-ttu-id="78494-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="78494-115">-AutomationAccountName</span></span>
<span data-ttu-id="78494-116">Anger namnet på ett Automation-konto där denna cmdlet får en webhook.</span><span class="sxs-lookup"><span data-stu-id="78494-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="78494-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78494-117">-DefaultProfile</span></span>
<span data-ttu-id="78494-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="78494-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78494-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="78494-119">-Name</span></span>
<span data-ttu-id="78494-120">Anger namnet på den webhook som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="78494-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78494-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78494-121">-ResourceGroupName</span></span>
<span data-ttu-id="78494-122">Anger namnet på den resurs grupp som den här cmdleten får till webhookar för.</span><span class="sxs-lookup"><span data-stu-id="78494-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="78494-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="78494-123">-RunbookName</span></span>
<span data-ttu-id="78494-124">Anger namnet på en Runbook som denna cmdlet hämtar webhookar för.</span><span class="sxs-lookup"><span data-stu-id="78494-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78494-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78494-125">CommonParameters</span></span>
<span data-ttu-id="78494-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78494-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78494-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78494-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78494-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="78494-128">INPUTS</span></span>

### <span data-ttu-id="78494-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78494-129">System.String</span></span>

## <span data-ttu-id="78494-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="78494-130">OUTPUTS</span></span>

### <span data-ttu-id="78494-131">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="78494-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="78494-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="78494-132">NOTES</span></span>

## <span data-ttu-id="78494-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="78494-133">RELATED LINKS</span></span>

[<span data-ttu-id="78494-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="78494-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="78494-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="78494-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="78494-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="78494-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


