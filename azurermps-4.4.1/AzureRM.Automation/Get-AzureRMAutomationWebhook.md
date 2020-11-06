---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: 1868f7995a8e3f426f8e4657f9e6df638f06662e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581543"
---
# <span data-ttu-id="23136-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="23136-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="23136-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23136-102">SYNOPSIS</span></span>
<span data-ttu-id="23136-103">Hämtar webhookar från Automation.</span><span class="sxs-lookup"><span data-stu-id="23136-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23136-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23136-104">SYNTAX</span></span>

### <span data-ttu-id="23136-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="23136-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23136-106">ByName</span><span class="sxs-lookup"><span data-stu-id="23136-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23136-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="23136-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23136-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23136-108">DESCRIPTION</span></span>
<span data-ttu-id="23136-109">Cmdleten **Get-AzureRmAutomationWebhook** hämtar webhookar.</span><span class="sxs-lookup"><span data-stu-id="23136-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="23136-110">För att få specifika webhookar, ange ett webhook-namn eller ange namnet på en Azure Automation-Runbook för att få webhookarna anslutna.</span><span class="sxs-lookup"><span data-stu-id="23136-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="23136-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23136-111">EXAMPLES</span></span>

### <span data-ttu-id="23136-112">Exempel 1: Hämta alla webhookar för en Runbook</span><span class="sxs-lookup"><span data-stu-id="23136-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="23136-113">Det här kommandot får alla Webhooks för en Runbook med namnet Runbook03 i Automation-kontot med namnet AutomationAccount01 i resurs gruppen som heter ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="23136-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="23136-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23136-114">PARAMETERS</span></span>

### <span data-ttu-id="23136-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23136-115">-AutomationAccountName</span></span>
<span data-ttu-id="23136-116">Anger namnet på ett Automation-konto där denna cmdlet får en webhook.</span><span class="sxs-lookup"><span data-stu-id="23136-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="23136-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="23136-117">-Name</span></span>
<span data-ttu-id="23136-118">Anger namnet på den webhook som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="23136-118">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="23136-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23136-119">-ResourceGroupName</span></span>
<span data-ttu-id="23136-120">Anger namnet på den resurs grupp som den här cmdleten får till webhookar för.</span><span class="sxs-lookup"><span data-stu-id="23136-120">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="23136-121">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="23136-121">-RunbookName</span></span>
<span data-ttu-id="23136-122">Anger namnet på en Runbook som denna cmdlet hämtar webhookar för.</span><span class="sxs-lookup"><span data-stu-id="23136-122">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="23136-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23136-123">-DefaultProfile</span></span>
<span data-ttu-id="23136-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23136-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23136-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23136-125">CommonParameters</span></span>
<span data-ttu-id="23136-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23136-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23136-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23136-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23136-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23136-128">INPUTS</span></span>

## <span data-ttu-id="23136-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23136-129">OUTPUTS</span></span>

### <span data-ttu-id="23136-130">Microsoft. Azure. commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="23136-130">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="23136-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23136-131">NOTES</span></span>

## <span data-ttu-id="23136-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23136-132">RELATED LINKS</span></span>

[<span data-ttu-id="23136-133">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="23136-133">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="23136-134">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="23136-134">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="23136-135">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="23136-135">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


