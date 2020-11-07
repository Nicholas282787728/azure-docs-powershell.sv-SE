---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0AC0C4F9-4138-49EA-88CB-DC220DE7E9F4
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplanmetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlanMetrics.md
ms.openlocfilehash: c08ae63999582fd220005dde84316a2f4421d7b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923385"
---
# <span data-ttu-id="5f18f-101">Get-AzAppServicePlanMetrics</span><span class="sxs-lookup"><span data-stu-id="5f18f-101">Get-AzAppServicePlanMetrics</span></span>

## <span data-ttu-id="5f18f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f18f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f18f-103">Hämtar mått för Azure Web Service-abonnemang.</span><span class="sxs-lookup"><span data-stu-id="5f18f-103">Gets Azure Web service plan metrics.</span></span>

## <span data-ttu-id="5f18f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f18f-104">SYNTAX</span></span>

### <span data-ttu-id="5f18f-105">S</span><span class="sxs-lookup"><span data-stu-id="5f18f-105">S1</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f18f-106">S2</span><span class="sxs-lookup"><span data-stu-id="5f18f-106">S2</span></span>
```
Get-AzAppServicePlanMetrics [-Metrics] <String[]> [-StartTime] <DateTime> [[-EndTime] <DateTime>]
 [-Granularity] <String> [-InstanceDetails] [-AppServicePlan] <AppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f18f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f18f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f18f-108">**AzAppServicePlanMetrics** får App Service-planens mått.</span><span class="sxs-lookup"><span data-stu-id="5f18f-108">The **Get-AzAppServicePlanMetrics** gets App Service Plan metrics.</span></span>

## <span data-ttu-id="5f18f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f18f-109">EXAMPLES</span></span>

### <span data-ttu-id="5f18f-110">9.1</span><span class="sxs-lookup"><span data-stu-id="5f18f-110">1:</span></span>
```
PS C:\>Get-AzAppServicePlanMetrics -ResourceGroupName "Default-Web-WestUS" -Name "ContosoAppServPlan" -StartTime 2016-11-30T22:00:00Z -EndTime 2016-11-30T22:30:00Z -Granularity PT1M -Metrics ["CPU Percentage"]
```

<span data-ttu-id="5f18f-111">Det här kommandot får CPU-procent för App Service-planen per minut (PT1M-avsöknings tid 1 minut) mellan StartTime och slut värde</span><span class="sxs-lookup"><span data-stu-id="5f18f-111">This command gets CPU percentage of the App Service Plan per minute(PT1M - Poll Time 1 minute) between StartTime and EndTime</span></span>

## <span data-ttu-id="5f18f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f18f-112">PARAMETERS</span></span>

### <span data-ttu-id="5f18f-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5f18f-113">-AppServicePlan</span></span>
<span data-ttu-id="5f18f-114">App Service plan-objekt</span><span class="sxs-lookup"><span data-stu-id="5f18f-114">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f18f-115">-DefaultProfile</span></span>
<span data-ttu-id="5f18f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f18f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-117">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="5f18f-117">-EndTime</span></span>
<span data-ttu-id="5f18f-118">Slut tid i UTC</span><span class="sxs-lookup"><span data-stu-id="5f18f-118">End Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-119">-Granularitet</span><span class="sxs-lookup"><span data-stu-id="5f18f-119">-Granularity</span></span>
<span data-ttu-id="5f18f-120">Granularitet</span><span class="sxs-lookup"><span data-stu-id="5f18f-120">Granularity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PT1M, PT1H, P1D

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-121">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="5f18f-121">-InstanceDetails</span></span>
<span data-ttu-id="5f18f-122">Instans Detaljer</span><span class="sxs-lookup"><span data-stu-id="5f18f-122">Instance Details</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-123">-Mått</span><span class="sxs-lookup"><span data-stu-id="5f18f-123">-Metrics</span></span>
<span data-ttu-id="5f18f-124">Mått</span><span class="sxs-lookup"><span data-stu-id="5f18f-124">Metrics</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f18f-125">-Name</span></span>
<span data-ttu-id="5f18f-126">Namn på App Service-abonnemang</span><span class="sxs-lookup"><span data-stu-id="5f18f-126">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f18f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f18f-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5f18f-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5f18f-129">-StartTime</span></span>
<span data-ttu-id="5f18f-130">Start tid i UTC</span><span class="sxs-lookup"><span data-stu-id="5f18f-130">Start Time in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f18f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f18f-131">CommonParameters</span></span>
<span data-ttu-id="5f18f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f18f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f18f-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f18f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f18f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f18f-134">INPUTS</span></span>

### <span data-ttu-id="5f18f-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="5f18f-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="5f18f-136">Parametern ' AppServicePlan ' godkänner värdet av typen ' ServerFarmWithRichSku ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5f18f-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="5f18f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f18f-137">OUTPUTS</span></span>

## <span data-ttu-id="5f18f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f18f-138">NOTES</span></span>

## <span data-ttu-id="5f18f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f18f-139">RELATED LINKS</span></span>

