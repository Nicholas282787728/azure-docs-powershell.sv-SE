---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758192"
---
# <span data-ttu-id="2ee9e-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="2ee9e-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="2ee9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ee9e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee9e-103">Skapar ett metriskt mått filter som kan användas för att fråga efter mått.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ee9e-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ee9e-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee9e-106">Cmdleten **New-AzureRmMetricFilter** skapar ett mått för metriska dimensioner som kan användas för att fråga efter mått.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="2ee9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ee9e-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee9e-108">Exempel 1: skapa ett mått för metriska dimensioner</span><span class="sxs-lookup"><span data-stu-id="2ee9e-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="2ee9e-109">Det här kommandot skapar mått måttet filter för formatet "City EQ" Stockholm "eller City EQ" New York ".</span><span class="sxs-lookup"><span data-stu-id="2ee9e-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="2ee9e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ee9e-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee9e-111">-DefaultProfile</span></span>
<span data-ttu-id="2ee9e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ee9e-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="2ee9e-113">-Dimension</span></span>
<span data-ttu-id="2ee9e-114">Namnet på mått dimensionen.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="2ee9e-115">-Operatör</span><span class="sxs-lookup"><span data-stu-id="2ee9e-115">-Operator</span></span>
<span data-ttu-id="2ee9e-116">Anger den operator som används för att välja mått dimensionen.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="2ee9e-117">-Värde</span><span class="sxs-lookup"><span data-stu-id="2ee9e-117">-Value</span></span>
<span data-ttu-id="2ee9e-118">Anger matrisen med mått dimensions värden.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="2ee9e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee9e-119">CommonParameters</span></span>
<span data-ttu-id="2ee9e-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee9e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee9e-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee9e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee9e-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ee9e-122">INPUTS</span></span>

### <span data-ttu-id="2ee9e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee9e-123">System.String</span></span>

### <span data-ttu-id="2ee9e-124">System. string []</span><span class="sxs-lookup"><span data-stu-id="2ee9e-124">System.String[]</span></span>

## <span data-ttu-id="2ee9e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ee9e-125">OUTPUTS</span></span>

### <span data-ttu-id="2ee9e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee9e-126">System.String</span></span>

## <span data-ttu-id="2ee9e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ee9e-127">NOTES</span></span>

## <span data-ttu-id="2ee9e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ee9e-128">RELATED LINKS</span></span>

<span data-ttu-id="2ee9e-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="2ee9e-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

