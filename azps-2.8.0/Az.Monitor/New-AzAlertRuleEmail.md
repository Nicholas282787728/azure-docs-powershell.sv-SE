---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 30447992cd8159f56ae08d6cb2baf659c9ed7bb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918611"
---
# <span data-ttu-id="b299a-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b299a-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="b299a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b299a-102">SYNOPSIS</span></span>
<span data-ttu-id="b299a-103">Skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="b299a-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="b299a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b299a-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b299a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b299a-105">DESCRIPTION</span></span>
<span data-ttu-id="b299a-106">Cmdleten **New-AzAlertRuleEmail** skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="b299a-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="b299a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b299a-107">EXAMPLES</span></span>

### <span data-ttu-id="b299a-108">Exempel 1: skapa en e-poståtgärd för aviserings regeln för tjänst ägare</span><span class="sxs-lookup"><span data-stu-id="b299a-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="b299a-109">Det här kommandot skapar en e-poståtgärd för aviserings regeln för att skicka till sina tjänst ägare när en notifieringsregel utlöses.</span><span class="sxs-lookup"><span data-stu-id="b299a-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="b299a-110">Exempel 2: skapa en e-poståtgärd för aviserings regeln för icke-tjänste ägare</span><span class="sxs-lookup"><span data-stu-id="b299a-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="b299a-111">Det här kommandot skapar en e-poståtgärd för aviserings regeln för de angivna e-postadresserna, men inte för tjänste ägarna.</span><span class="sxs-lookup"><span data-stu-id="b299a-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="b299a-112">Exempel 3: skapa en e-poståtgärd för tjänste ägare och ägare som inte tillhör en aviserings regel</span><span class="sxs-lookup"><span data-stu-id="b299a-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="b299a-113">Det här kommandot skapar en e-poståtgärd för aviserings regeln för den angivna adressen och dess tjänste ägare.</span><span class="sxs-lookup"><span data-stu-id="b299a-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="b299a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b299a-114">PARAMETERS</span></span>

### <span data-ttu-id="b299a-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="b299a-115">-CustomEmail</span></span>
<span data-ttu-id="b299a-116">Anger en lista med kommaavgränsade e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="b299a-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b299a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b299a-117">-DefaultProfile</span></span>
<span data-ttu-id="b299a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b299a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b299a-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="b299a-119">-SendToServiceOwner</span></span>
<span data-ttu-id="b299a-120">Anger att den här åtgärden skickar ett e-postmeddelande till tjänste ägarna när regeln utlöses.</span><span class="sxs-lookup"><span data-stu-id="b299a-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b299a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b299a-121">CommonParameters</span></span>
<span data-ttu-id="b299a-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b299a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b299a-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b299a-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b299a-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b299a-124">INPUTS</span></span>

### <span data-ttu-id="b299a-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="b299a-125">System.String[]</span></span>

### <span data-ttu-id="b299a-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b299a-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b299a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b299a-127">OUTPUTS</span></span>

### <span data-ttu-id="b299a-128">Microsoft. Azure. Management. Monitoring. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="b299a-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="b299a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b299a-129">NOTES</span></span>

## <span data-ttu-id="b299a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b299a-130">RELATED LINKS</span></span>

[<span data-ttu-id="b299a-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b299a-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="b299a-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b299a-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b299a-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b299a-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b299a-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b299a-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


