---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 23c32ae1520ac750aa91db3a5924b2a4d292417a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918911"
---
# <span data-ttu-id="0f837-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0f837-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="0f837-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f837-102">SYNOPSIS</span></span>
<span data-ttu-id="0f837-103">Skapar ett objekt av typen source</span><span class="sxs-lookup"><span data-stu-id="0f837-103">Creates an object of type Source</span></span>

## <span data-ttu-id="0f837-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f837-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f837-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f837-105">DESCRIPTION</span></span>
<span data-ttu-id="0f837-106">Skapar ett objekt av typen Source.</span><span class="sxs-lookup"><span data-stu-id="0f837-106">Creates an object of type Source.</span></span>
<span data-ttu-id="0f837-107">Det här objektet måste skickas till det kommando som skapar en varnings regel för loggning</span><span class="sxs-lookup"><span data-stu-id="0f837-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="0f837-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f837-108">EXAMPLES</span></span>

### <span data-ttu-id="0f837-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0f837-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="0f837-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f837-110">PARAMETERS</span></span>

### <span data-ttu-id="0f837-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="0f837-111">-AuthorizedResource</span></span>
<span data-ttu-id="0f837-112">Listan över godkända resurser för denna avisering</span><span class="sxs-lookup"><span data-stu-id="0f837-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="0f837-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="0f837-113">-DataSourceId</span></span>
<span data-ttu-id="0f837-114">Data källan som den här aviseringen skapas för</span><span class="sxs-lookup"><span data-stu-id="0f837-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="0f837-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f837-115">-DefaultProfile</span></span>
<span data-ttu-id="0f837-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f837-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f837-117">-Fråga</span><span class="sxs-lookup"><span data-stu-id="0f837-117">-Query</span></span>
<span data-ttu-id="0f837-118">Varnings frågan</span><span class="sxs-lookup"><span data-stu-id="0f837-118">The alert query</span></span>

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

### <span data-ttu-id="0f837-119">-Frågetyp</span><span class="sxs-lookup"><span data-stu-id="0f837-119">-QueryType</span></span>
<span data-ttu-id="0f837-120">Typ av fråga – för närvarande stöds värden: ResultCount</span><span class="sxs-lookup"><span data-stu-id="0f837-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="0f837-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f837-121">CommonParameters</span></span>
<span data-ttu-id="0f837-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f837-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f837-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f837-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f837-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f837-124">INPUTS</span></span>

### <span data-ttu-id="0f837-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="0f837-125">None</span></span>

## <span data-ttu-id="0f837-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f837-126">OUTPUTS</span></span>

### <span data-ttu-id="0f837-127">Microsoft. Azure. commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0f837-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="0f837-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f837-128">NOTES</span></span>

## <span data-ttu-id="0f837-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f837-129">RELATED LINKS</span></span>
