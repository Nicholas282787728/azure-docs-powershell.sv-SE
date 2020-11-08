---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: 479d31afca4bb21fdad10a594917bd8eb51706b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915605"
---
# <span data-ttu-id="7d844-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="7d844-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="7d844-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d844-102">SYNOPSIS</span></span>
<span data-ttu-id="7d844-103">Skapar ett metriskt mått filter som kan användas för att fråga efter mått.</span><span class="sxs-lookup"><span data-stu-id="7d844-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7d844-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d844-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d844-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d844-105">DESCRIPTION</span></span>
<span data-ttu-id="7d844-106">Cmdleten **New-AzMetricFilter** skapar ett mått för metriska dimensioner som kan användas för att fråga efter mått.</span><span class="sxs-lookup"><span data-stu-id="7d844-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="7d844-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d844-107">EXAMPLES</span></span>

### <span data-ttu-id="7d844-108">Exempel 1: skapa ett mått för metriska dimensioner</span><span class="sxs-lookup"><span data-stu-id="7d844-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="7d844-109">Det här kommandot skapar mått måttet filter för formatet "City EQ" Stockholm "eller City EQ" New York ".</span><span class="sxs-lookup"><span data-stu-id="7d844-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="7d844-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d844-110">PARAMETERS</span></span>

### <span data-ttu-id="7d844-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d844-111">-DefaultProfile</span></span>
<span data-ttu-id="7d844-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d844-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d844-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="7d844-113">-Dimension</span></span>
<span data-ttu-id="7d844-114">Namnet på mått dimensionen.</span><span class="sxs-lookup"><span data-stu-id="7d844-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="7d844-115">-Operatör</span><span class="sxs-lookup"><span data-stu-id="7d844-115">-Operator</span></span>
<span data-ttu-id="7d844-116">Anger den operator som används för att välja mått dimensionen.</span><span class="sxs-lookup"><span data-stu-id="7d844-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d844-117">-Värde</span><span class="sxs-lookup"><span data-stu-id="7d844-117">-Value</span></span>
<span data-ttu-id="7d844-118">Anger matrisen med mått dimensions värden.</span><span class="sxs-lookup"><span data-stu-id="7d844-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d844-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d844-119">CommonParameters</span></span>
<span data-ttu-id="7d844-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d844-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d844-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d844-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d844-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d844-122">INPUTS</span></span>

### <span data-ttu-id="7d844-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7d844-123">System.String</span></span>

### <span data-ttu-id="7d844-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="7d844-124">System.String[]</span></span>

## <span data-ttu-id="7d844-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d844-125">OUTPUTS</span></span>

### <span data-ttu-id="7d844-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7d844-126">System.String</span></span>

## <span data-ttu-id="7d844-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d844-127">NOTES</span></span>

## <span data-ttu-id="7d844-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d844-128">RELATED LINKS</span></span>

<span data-ttu-id="7d844-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="7d844-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>
