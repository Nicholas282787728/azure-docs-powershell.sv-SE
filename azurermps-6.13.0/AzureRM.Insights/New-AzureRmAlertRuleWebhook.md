---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 619219a300bb1b7317ea4c8c5fce442d43b74ff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576265"
---
# <span data-ttu-id="44eab-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="44eab-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="44eab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44eab-102">SYNOPSIS</span></span>
<span data-ttu-id="44eab-103">Skapar en aviserings regel med webhook.</span><span class="sxs-lookup"><span data-stu-id="44eab-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44eab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44eab-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44eab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44eab-105">DESCRIPTION</span></span>
<span data-ttu-id="44eab-106">Cmdleten **New-AzureRmAlertRuleWebhook** skapar en notifieringsregel för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="44eab-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="44eab-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44eab-107">EXAMPLES</span></span>

### <span data-ttu-id="44eab-108">Exempel 1: skapa en notifieringsregel för aviseringar</span><span class="sxs-lookup"><span data-stu-id="44eab-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="44eab-109">Det här kommandot skapar en aviserings regel webhook genom att bara ange tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="44eab-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="44eab-110">Exempel 2: skapa en webhook med en egenskap</span><span class="sxs-lookup"><span data-stu-id="44eab-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="44eab-111">Det här kommandot skapar en notifieringsregel för Contoso.com med en egenskap och lagrar den sedan i $Actual variabel.</span><span class="sxs-lookup"><span data-stu-id="44eab-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="44eab-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44eab-112">PARAMETERS</span></span>

### <span data-ttu-id="44eab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44eab-113">-DefaultProfile</span></span>
<span data-ttu-id="44eab-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="44eab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44eab-115">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="44eab-115">-Property</span></span>
<span data-ttu-id="44eab-116">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="44eab-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="44eab-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="44eab-117">-ServiceUri</span></span>
<span data-ttu-id="44eab-118">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="44eab-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="44eab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44eab-119">CommonParameters</span></span>
<span data-ttu-id="44eab-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44eab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44eab-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44eab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44eab-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44eab-122">INPUTS</span></span>

### <span data-ttu-id="44eab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="44eab-123">System.String</span></span>

### <span data-ttu-id="44eab-124">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="44eab-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="44eab-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44eab-125">OUTPUTS</span></span>

### <span data-ttu-id="44eab-126">Microsoft. Azure. Management. Monitoring. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="44eab-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="44eab-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44eab-127">NOTES</span></span>

## <span data-ttu-id="44eab-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44eab-128">RELATED LINKS</span></span>

[<span data-ttu-id="44eab-129">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="44eab-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="44eab-130">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="44eab-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="44eab-131">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="44eab-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="44eab-132">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="44eab-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="44eab-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="44eab-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


