---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2DimensionSelection.md
ms.openlocfilehash: 33e1b8fe5ae88666ffacf8849b9e2700f7066151
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922553"
---
# <span data-ttu-id="2e5de-101">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2e5de-101">New-AzMetricAlertRuleV2DimensionSelection</span></span>

## <span data-ttu-id="2e5de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e5de-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5de-103">Skapar ett lokalt dimensions urvals objekt som kan användas för att konstruera ett villkor för metriska meddelanden.</span><span class="sxs-lookup"><span data-stu-id="2e5de-103">Creates a local dimension selection object that can be used to construct a metric alert criteria.</span></span>

## <span data-ttu-id="2e5de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e5de-104">SYNTAX</span></span>

```
New-AzMetricAlertRuleV2DimensionSelection -DimensionName <String> -ValuesToInclude <String[]>
 [-ValuesToExclude <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e5de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e5de-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5de-106">Med **New-AzMetricAlertRuleV2DimensionSelection-** cmdleten skapas ett lokalt dimensions urvals objekt som hjälper dig att skapa ett mått för metriska meddelanden med hjälp av **New-AzMetricAlertRuleV2Criteria** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e5de-106">The **New-AzMetricAlertRuleV2DimensionSelection** cmdlet creates a local dimension selection object to help with the construction of metric alert criteria using **New-AzMetricAlertRuleV2Criteria** cmdlet.</span></span>

## <span data-ttu-id="2e5de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e5de-107">EXAMPLES</span></span>

### <span data-ttu-id="2e5de-108">Exempel 1: skapa ett dimensions markerings objekt</span><span class="sxs-lookup"><span data-stu-id="2e5de-108">Example 1 : Create a dimension selection object</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2DimensionSelection -DimensionName LUN -ValuesToInclude 1,3,4

Dimension IncludeValues ExcludeValues
--------- ------------- -------------
LUN       {1, 3, 4}
```

<span data-ttu-id="2e5de-109">Det här kommandot skapar ett mått markerings objekt som anger att värden {1,3,4} måste markeras för dimension "LUN"</span><span class="sxs-lookup"><span data-stu-id="2e5de-109">This command creates a dimension selection object that specifies that values {1,3,4} need to be selected for Dimension "LUN"</span></span>

## <span data-ttu-id="2e5de-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e5de-110">PARAMETERS</span></span>

### <span data-ttu-id="2e5de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5de-111">-DefaultProfile</span></span>
<span data-ttu-id="2e5de-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5de-113">-DimensionName</span><span class="sxs-lookup"><span data-stu-id="2e5de-113">-DimensionName</span></span>
<span data-ttu-id="2e5de-114">Dimensions namnet</span><span class="sxs-lookup"><span data-stu-id="2e5de-114">The Dimension name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5de-115">-ValuesToExclude</span><span class="sxs-lookup"><span data-stu-id="2e5de-115">-ValuesToExclude</span></span>
<span data-ttu-id="2e5de-116">ExcludeValues</span><span class="sxs-lookup"><span data-stu-id="2e5de-116">The ExcludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5de-117">-ValuesToInclude</span><span class="sxs-lookup"><span data-stu-id="2e5de-117">-ValuesToInclude</span></span>
<span data-ttu-id="2e5de-118">IncludeValues</span><span class="sxs-lookup"><span data-stu-id="2e5de-118">The IncludeValues</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5de-119">CommonParameters</span></span>
<span data-ttu-id="2e5de-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5de-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e5de-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5de-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e5de-122">INPUTS</span></span>

### <span data-ttu-id="2e5de-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2e5de-123">System.String</span></span>

### <span data-ttu-id="2e5de-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="2e5de-124">System.String[]</span></span>

## <span data-ttu-id="2e5de-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e5de-125">OUTPUTS</span></span>

### <span data-ttu-id="2e5de-126">Microsoft. Azure. commands. Insights. OutputClasses. PSMetricDimension</span><span class="sxs-lookup"><span data-stu-id="2e5de-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension</span></span>

## <span data-ttu-id="2e5de-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e5de-127">NOTES</span></span>

## <span data-ttu-id="2e5de-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e5de-128">RELATED LINKS</span></span>
