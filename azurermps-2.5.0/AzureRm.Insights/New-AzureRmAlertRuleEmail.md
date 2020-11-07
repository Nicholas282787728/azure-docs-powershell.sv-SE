---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931406"
---
# <span data-ttu-id="57d75-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="57d75-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="57d75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57d75-102">SYNOPSIS</span></span>
<span data-ttu-id="57d75-103">Skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="57d75-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57d75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57d75-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d75-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57d75-105">DESCRIPTION</span></span>
<span data-ttu-id="57d75-106">Cmdleten **New-AzureRmAlertRuleEmail** skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="57d75-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="57d75-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57d75-107">EXAMPLES</span></span>

### <span data-ttu-id="57d75-108">Exempel 1: skapa en e-poståtgärd för aviserings regeln för tjänst ägare</span><span class="sxs-lookup"><span data-stu-id="57d75-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="57d75-109">Det här kommandot skapar en e-poståtgärd för aviserings regeln för att skicka till sina tjänst ägare när en notifieringsregel utlöses.</span><span class="sxs-lookup"><span data-stu-id="57d75-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="57d75-110">Exempel 2: skapa en e-poståtgärd för aviserings regeln för icke-tjänste ägare</span><span class="sxs-lookup"><span data-stu-id="57d75-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="57d75-111">Det här kommandot skapar en e-poståtgärd för aviserings regeln för de angivna e-postadresserna, men inte för tjänste ägarna.</span><span class="sxs-lookup"><span data-stu-id="57d75-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="57d75-112">Exempel 3: skapa en e-poståtgärd för tjänste ägare och ägare som inte tillhör en aviserings regel</span><span class="sxs-lookup"><span data-stu-id="57d75-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="57d75-113">Det här kommandot skapar en e-poståtgärd för aviserings regeln för den angivna adressen och dess tjänste ägare.</span><span class="sxs-lookup"><span data-stu-id="57d75-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="57d75-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57d75-114">PARAMETERS</span></span>

### <span data-ttu-id="57d75-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="57d75-115">-CustomEmail</span></span>
<span data-ttu-id="57d75-116">Anger en lista med kommaavgränsade e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="57d75-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="57d75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d75-117">-DefaultProfile</span></span>
<span data-ttu-id="57d75-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57d75-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57d75-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="57d75-119">-SendToServiceOwner</span></span>
<span data-ttu-id="57d75-120">Anger att den här åtgärden skickar ett e-postmeddelande till tjänste ägarna när regeln utlöses.</span><span class="sxs-lookup"><span data-stu-id="57d75-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="57d75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d75-121">CommonParameters</span></span>
<span data-ttu-id="57d75-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57d75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d75-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d75-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d75-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57d75-124">INPUTS</span></span>

### <span data-ttu-id="57d75-125">System. string []</span><span class="sxs-lookup"><span data-stu-id="57d75-125">System.String[]</span></span>

### <span data-ttu-id="57d75-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="57d75-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="57d75-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57d75-127">OUTPUTS</span></span>

### <span data-ttu-id="57d75-128">Microsoft. Azure. Management. Monitoring. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="57d75-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="57d75-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57d75-129">NOTES</span></span>

## <span data-ttu-id="57d75-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57d75-130">RELATED LINKS</span></span>



[<span data-ttu-id="57d75-131">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="57d75-131">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="57d75-132">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="57d75-132">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="57d75-133">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="57d75-133">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


