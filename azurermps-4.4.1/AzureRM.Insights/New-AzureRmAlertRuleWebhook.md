---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584739"
---
# <span data-ttu-id="e8896-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e8896-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="e8896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8896-102">SYNOPSIS</span></span>
<span data-ttu-id="e8896-103">Skapar en aviserings regel med webhook.</span><span class="sxs-lookup"><span data-stu-id="e8896-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8896-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8896-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8896-105">DESCRIPTION</span></span>
<span data-ttu-id="e8896-106">Cmdleten **New-AzureRmAlertRuleWebhook** skapar en notifieringsregel för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="e8896-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="e8896-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8896-107">EXAMPLES</span></span>

### <span data-ttu-id="e8896-108">Exempel 1: skapa en notifieringsregel för aviseringar</span><span class="sxs-lookup"><span data-stu-id="e8896-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="e8896-109">Det här kommandot skapar en aviserings regel webhook genom att bara ange tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="e8896-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="e8896-110">Exempel 2: skapa en webhook med en egenskap</span><span class="sxs-lookup"><span data-stu-id="e8896-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="e8896-111">Det här kommandot skapar en notifieringsregel för Contoso.com med en egenskap och lagrar den sedan i $Actual variabel.</span><span class="sxs-lookup"><span data-stu-id="e8896-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="e8896-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8896-112">PARAMETERS</span></span>

### <span data-ttu-id="e8896-113">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="e8896-113">-Properties</span></span>
<span data-ttu-id="e8896-114">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="e8896-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8896-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e8896-115">-ServiceUri</span></span>
<span data-ttu-id="e8896-116">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="e8896-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="e8896-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8896-117">-DefaultProfile</span></span>
<span data-ttu-id="e8896-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8896-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8896-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8896-119">CommonParameters</span></span>
<span data-ttu-id="e8896-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8896-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8896-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8896-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8896-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8896-122">INPUTS</span></span>

## <span data-ttu-id="e8896-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8896-123">OUTPUTS</span></span>

### <span data-ttu-id="e8896-124">Microsoft. Azure. Management. Monitoring. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="e8896-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="e8896-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8896-125">NOTES</span></span>

## <span data-ttu-id="e8896-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8896-126">RELATED LINKS</span></span>

[<span data-ttu-id="e8896-127">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e8896-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e8896-128">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e8896-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e8896-129">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e8896-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e8896-130">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e8896-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="e8896-131">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e8896-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


