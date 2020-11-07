---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931402"
---
# <span data-ttu-id="ace30-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ace30-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="ace30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ace30-102">SYNOPSIS</span></span>
<span data-ttu-id="ace30-103">Skapar en aviserings regel med webhook.</span><span class="sxs-lookup"><span data-stu-id="ace30-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ace30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ace30-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ace30-105">DESCRIPTION</span></span>
<span data-ttu-id="ace30-106">Cmdleten **New-AzureRmAlertRuleWebhook** skapar en notifieringsregel för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="ace30-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="ace30-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ace30-107">EXAMPLES</span></span>

### <span data-ttu-id="ace30-108">Exempel 1: skapa en notifieringsregel för aviseringar</span><span class="sxs-lookup"><span data-stu-id="ace30-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="ace30-109">Det här kommandot skapar en aviserings regel webhook genom att bara ange tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="ace30-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="ace30-110">Exempel 2: skapa en webhook med en egenskap</span><span class="sxs-lookup"><span data-stu-id="ace30-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="ace30-111">Det här kommandot skapar en notifieringsregel för Contoso.com med en egenskap och lagrar den sedan i $Actual variabel.</span><span class="sxs-lookup"><span data-stu-id="ace30-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="ace30-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ace30-112">PARAMETERS</span></span>

### <span data-ttu-id="ace30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace30-113">-DefaultProfile</span></span>
<span data-ttu-id="ace30-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ace30-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ace30-115">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="ace30-115">-Property</span></span>
<span data-ttu-id="ace30-116">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="ace30-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="ace30-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="ace30-117">-ServiceUri</span></span>
<span data-ttu-id="ace30-118">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="ace30-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="ace30-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace30-119">CommonParameters</span></span>
<span data-ttu-id="ace30-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace30-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace30-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace30-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace30-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ace30-122">INPUTS</span></span>

### <span data-ttu-id="ace30-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ace30-123">System.String</span></span>

### <span data-ttu-id="ace30-124">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="ace30-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ace30-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ace30-125">OUTPUTS</span></span>

### <span data-ttu-id="ace30-126">Microsoft. Azure. Management. Monitoring. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="ace30-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="ace30-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ace30-127">NOTES</span></span>

## <span data-ttu-id="ace30-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ace30-128">RELATED LINKS</span></span>



[<span data-ttu-id="ace30-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ace30-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ace30-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ace30-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="ace30-131">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="ace30-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="ace30-132">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="ace30-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


