---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580596"
---
# <span data-ttu-id="0c5b1-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="0c5b1-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="0c5b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5b1-103">Skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c5b1-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5b1-106">Cmdleten **New-AzureRmAlertRuleEmail** skapar en e-poståtgärd för en notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="0c5b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c5b1-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5b1-108">Exempel 1: skapa en e-poståtgärd för aviserings regeln för tjänst ägare</span><span class="sxs-lookup"><span data-stu-id="0c5b1-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="0c5b1-109">Det här kommandot skapar en e-poståtgärd för aviserings regeln för att skicka till sina tjänst ägare när en notifieringsregel utlöses.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="0c5b1-110">Exempel 2: skapa en e-poståtgärd för aviserings regeln för icke-tjänste ägare</span><span class="sxs-lookup"><span data-stu-id="0c5b1-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="0c5b1-111">Det här kommandot skapar en e-poståtgärd för aviserings regeln för de angivna e-postadresserna, men inte för tjänste ägarna.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="0c5b1-112">Exempel 3: skapa en e-poståtgärd för tjänste ägare och ägare som inte tillhör en aviserings regel</span><span class="sxs-lookup"><span data-stu-id="0c5b1-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="0c5b1-113">Det här kommandot skapar en e-poståtgärd för aviserings regeln för den angivna adressen och dess tjänste ägare.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="0c5b1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c5b1-114">PARAMETERS</span></span>

### <span data-ttu-id="0c5b1-115">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="0c5b1-115">-CustomEmails</span></span>
<span data-ttu-id="0c5b1-116">Anger en lista med kommaavgränsade e-postadresser.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="0c5b1-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="0c5b1-117">-SendToServiceOwners</span></span>
<span data-ttu-id="0c5b1-118">Anger att den här åtgärden skickar ett e-postmeddelande till tjänste ägarna när regeln utlöses.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="0c5b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5b1-119">-DefaultProfile</span></span>
<span data-ttu-id="0c5b1-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5b1-121">CommonParameters</span></span>
<span data-ttu-id="0c5b1-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5b1-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5b1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5b1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c5b1-124">INPUTS</span></span>

## <span data-ttu-id="0c5b1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c5b1-125">OUTPUTS</span></span>

### <span data-ttu-id="0c5b1-126">Microsoft. Azure. Management. Monitoring. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="0c5b1-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="0c5b1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c5b1-127">NOTES</span></span>

## <span data-ttu-id="0c5b1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c5b1-128">RELATED LINKS</span></span>

[<span data-ttu-id="0c5b1-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c5b1-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="0c5b1-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c5b1-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0c5b1-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0c5b1-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0c5b1-132">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0c5b1-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


