---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: aa287095405e48550153e58049f750d78a9ed877
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918607"
---
# <span data-ttu-id="e3b06-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e3b06-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="e3b06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3b06-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b06-103">Skapar en aviserings regel med webhook.</span><span class="sxs-lookup"><span data-stu-id="e3b06-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="e3b06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3b06-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3b06-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b06-106">Cmdleten **New-AzAlertRuleWebhook** skapar en notifieringsregel för aviserings regler.</span><span class="sxs-lookup"><span data-stu-id="e3b06-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="e3b06-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3b06-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b06-108">Exempel 1: skapa en notifieringsregel för aviseringar</span><span class="sxs-lookup"><span data-stu-id="e3b06-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="e3b06-109">Det här kommandot skapar en aviserings regel webhook genom att bara ange tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="e3b06-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="e3b06-110">Exempel 2: skapa en webhook med en egenskap</span><span class="sxs-lookup"><span data-stu-id="e3b06-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="e3b06-111">Det här kommandot skapar en notifieringsregel för Contoso.com med en egenskap och lagrar den sedan i $Actual variabel.</span><span class="sxs-lookup"><span data-stu-id="e3b06-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="e3b06-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3b06-112">PARAMETERS</span></span>

### <span data-ttu-id="e3b06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b06-113">-DefaultProfile</span></span>
<span data-ttu-id="e3b06-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3b06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3b06-115">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="e3b06-115">-Property</span></span>
<span data-ttu-id="e3b06-116">Anger listan över egenskaper i formatet @ (property1 = ' värde1 ',....).</span><span class="sxs-lookup"><span data-stu-id="e3b06-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="e3b06-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e3b06-117">-ServiceUri</span></span>
<span data-ttu-id="e3b06-118">Anger tjänste-URI.</span><span class="sxs-lookup"><span data-stu-id="e3b06-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="e3b06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b06-119">CommonParameters</span></span>
<span data-ttu-id="e3b06-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b06-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3b06-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b06-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3b06-122">INPUTS</span></span>

### <span data-ttu-id="e3b06-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b06-123">System.String</span></span>

### <span data-ttu-id="e3b06-124">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="e3b06-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3b06-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3b06-125">OUTPUTS</span></span>

### <span data-ttu-id="e3b06-126">Microsoft. Azure. Management. Monitoring. Management. Models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="e3b06-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="e3b06-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3b06-127">NOTES</span></span>

## <span data-ttu-id="e3b06-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3b06-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3b06-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3b06-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="e3b06-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3b06-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e3b06-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e3b06-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e3b06-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e3b06-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="e3b06-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e3b06-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


