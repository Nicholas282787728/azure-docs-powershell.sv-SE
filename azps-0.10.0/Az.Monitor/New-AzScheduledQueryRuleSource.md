---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922529"
---
# <span data-ttu-id="73cc5-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="73cc5-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="73cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="73cc5-103">Skapar ett objekt av typen source</span><span class="sxs-lookup"><span data-stu-id="73cc5-103">Creates an object of type Source</span></span>

## <span data-ttu-id="73cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73cc5-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73cc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="73cc5-106">Skapar ett objekt av typen Source.</span><span class="sxs-lookup"><span data-stu-id="73cc5-106">Creates an object of type Source.</span></span>
<span data-ttu-id="73cc5-107">Det här objektet måste skickas till det kommando som skapar en varnings regel för loggning</span><span class="sxs-lookup"><span data-stu-id="73cc5-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="73cc5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73cc5-108">EXAMPLES</span></span>

### <span data-ttu-id="73cc5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73cc5-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="73cc5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73cc5-110">PARAMETERS</span></span>

### <span data-ttu-id="73cc5-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="73cc5-111">-AuthorizedResource</span></span>
<span data-ttu-id="73cc5-112">Listan över godkända resurser för denna avisering</span><span class="sxs-lookup"><span data-stu-id="73cc5-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc5-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="73cc5-113">-DataSourceId</span></span>
<span data-ttu-id="73cc5-114">Data källan som den här aviseringen skapas för</span><span class="sxs-lookup"><span data-stu-id="73cc5-114">The data source on which this alert is created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73cc5-115">-DefaultProfile</span></span>
<span data-ttu-id="73cc5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73cc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73cc5-117">-Fråga</span><span class="sxs-lookup"><span data-stu-id="73cc5-117">-Query</span></span>
<span data-ttu-id="73cc5-118">Varnings frågan</span><span class="sxs-lookup"><span data-stu-id="73cc5-118">The alert query</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc5-119">-Frågetyp</span><span class="sxs-lookup"><span data-stu-id="73cc5-119">-QueryType</span></span>
<span data-ttu-id="73cc5-120">Typ av fråga – för närvarande stöds värden: ResultCount</span><span class="sxs-lookup"><span data-stu-id="73cc5-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73cc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73cc5-121">CommonParameters</span></span>
<span data-ttu-id="73cc5-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73cc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73cc5-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73cc5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73cc5-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73cc5-124">INPUTS</span></span>

### <span data-ttu-id="73cc5-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="73cc5-125">None</span></span>

## <span data-ttu-id="73cc5-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73cc5-126">OUTPUTS</span></span>

### <span data-ttu-id="73cc5-127">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="73cc5-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="73cc5-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73cc5-128">NOTES</span></span>

## <span data-ttu-id="73cc5-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73cc5-129">RELATED LINKS</span></span>
