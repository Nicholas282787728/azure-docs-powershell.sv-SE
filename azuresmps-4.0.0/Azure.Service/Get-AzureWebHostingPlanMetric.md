---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2DEF8B3A-4E91-4D39-AD39-1871F9FECE10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a59c93c9de0d2445f2839d9a66f4750751c987f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099740"
---
# <span data-ttu-id="358d0-101">Get-AzureWebHostingPlanMetric</span><span class="sxs-lookup"><span data-stu-id="358d0-101">Get-AzureWebHostingPlanMetric</span></span>

## <span data-ttu-id="358d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="358d0-102">SYNOPSIS</span></span>
<span data-ttu-id="358d0-103">Hämtar mått för Azure hosting-abonnemang.</span><span class="sxs-lookup"><span data-stu-id="358d0-103">Gets metrics for Azure website hosting plans.</span></span>

## <span data-ttu-id="358d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="358d0-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlanMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="358d0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="358d0-105">DESCRIPTION</span></span>
<span data-ttu-id="358d0-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="358d0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="358d0-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="358d0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="358d0-108">Cmdleten **Get-AzureWebHostingPlanMetric** tar emot mått för Azure Web Hosting-abonnemang i en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="358d0-108">The **Get-AzureWebHostingPlanMetric** cmdlet gets metrics for Azure web hosting plans in a subscription.</span></span>

## <span data-ttu-id="358d0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="358d0-109">EXAMPLES</span></span>

### <span data-ttu-id="358d0-110">Exempel 1: få mått för de senaste tre timmarna på per förekomst nivå</span><span class="sxs-lookup"><span data-stu-id="358d0-110">Example 1: Get metrics for the last three hours at a per-instance level</span></span>
```
PS C:\> Get-AzureWebHostingPlanMetric -WebSpaceName "eastuswebspace" -StartDate (get-date).AddHours(-3) -InstanceDetails $Metrics[1].Data 

Name : CpuPercentage 
Unit : Percent 
StartTime : 8/11/2014 7:00:00 AM 
EndTime : 8/11/2014 5:00:23 PM 
TimeGrain : PT1H 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 8:00:00 AM, Total:2, Min:9, Max:0, 
Time:8/11/2014 9:00:00 AM, Total:2, Min:9, Max:0, Time:8/11/2014 10:00:00 AM, Total:2, Min:8, Max:0...} $metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName
 ----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 8:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 9:00:00 AM 2 9 0 1 RD00155DC24579 
8/11/2014 10:00:00 AM 2 8 0 1 RD00155DC24599 
8/11/2014 11:00:00 AM 2 9 0 1 RD00155DC24599 
8/11/2014 12:00:00 PM 2 6 0 1 RD00155DC24599 
8/11/2014 1:00:00 PM 2 15 0 1 RD00155DC24599 
8/11/2014 2:00:00 PM 3 21 0 1 RD00155DC24599 
8/11/2014 3:00:00 PM 2 13 0 1 RD00155DC24599 
8/11/2014 4:00:00 PM 2 14 0 1 RD00155DC24599
```

<span data-ttu-id="358d0-111">Det här kommandot hämtar mått för webb värd abonnemang för de senaste tre timmarna per förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="358d0-111">This command gets web hosting plan metrics for last three hours on per-instance level.</span></span>

## <span data-ttu-id="358d0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="358d0-112">PARAMETERS</span></span>

### <span data-ttu-id="358d0-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="358d0-113">-EndDate</span></span>
<span data-ttu-id="358d0-114">Anger slut tiden, som ett **datetime** -objekt, som du returnerar måtten från.</span><span class="sxs-lookup"><span data-stu-id="358d0-114">Specifies the end time, as a **DateTime** object, from which to return metrics.</span></span>
<span data-ttu-id="358d0-115">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="358d0-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="358d0-116">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="358d0-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="358d0-117">-InstanceDetails</span></span>
<span data-ttu-id="358d0-118">Anger att denna cmdlet innehåller information om en viss nivå.</span><span class="sxs-lookup"><span data-stu-id="358d0-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="358d0-119">Om webbplats värds planen körs på två eller fler datorer returnerar den här cmdleten information för varje dator.</span><span class="sxs-lookup"><span data-stu-id="358d0-119">If the website hosting plan runs on two or more machines, this cmdlet returns details metrics for each machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="358d0-120">-MetricNames</span></span>
<span data-ttu-id="358d0-121">Arter en matris med mät värden att få.</span><span class="sxs-lookup"><span data-stu-id="358d0-121">Species an array of metrics to get.</span></span>
<span data-ttu-id="358d0-122">Om du inte anger ett värde för den här parametern får denna cmdlet alla mät värden.</span><span class="sxs-lookup"><span data-stu-id="358d0-122">If you do not specify a value for this parameter, this cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="358d0-123">-Name</span></span>
<span data-ttu-id="358d0-124">Anger namnet på en plan i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="358d0-124">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="358d0-125">Som standard får **Get-AzureWebHostingPlanMetric** alla webbplatser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="358d0-125">By default, **Get-AzureWebHostingPlanMetric** gets all websites in the current subscription.</span></span>
<span data-ttu-id="358d0-126">Den här parametern stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="358d0-126">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="358d0-127">-Profile</span></span>
<span data-ttu-id="358d0-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="358d0-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="358d0-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="358d0-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-130">-StartDate</span><span class="sxs-lookup"><span data-stu-id="358d0-130">-StartDate</span></span>
<span data-ttu-id="358d0-131">Anger start tiden, som ett **datetime** -objekt, som du kan använda för att få mått.</span><span class="sxs-lookup"><span data-stu-id="358d0-131">Specifies the start time, as a **DateTime** object, for which to get metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-132">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="358d0-132">-TimeGrain</span></span>
<span data-ttu-id="358d0-133">Anger tidsenheten som du vill få Mät värden för.</span><span class="sxs-lookup"><span data-stu-id="358d0-133">Specifies the time unit for which to get metrics.</span></span>
<span data-ttu-id="358d0-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="358d0-134">Valid values are:</span></span> 

- <span data-ttu-id="358d0-135">PT1M (minut)</span><span class="sxs-lookup"><span data-stu-id="358d0-135">PT1M (Minute)</span></span> 
- <span data-ttu-id="358d0-136">PT1H (timme)</span><span class="sxs-lookup"><span data-stu-id="358d0-136">PT1H (Hour)</span></span> 
- <span data-ttu-id="358d0-137">P1D (dag)</span><span class="sxs-lookup"><span data-stu-id="358d0-137">P1D (Day)</span></span>

<span data-ttu-id="358d0-138">Standardvärdet är PT1H.</span><span class="sxs-lookup"><span data-stu-id="358d0-138">The default value is PT1H.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-139">-WebSpaceName</span><span class="sxs-lookup"><span data-stu-id="358d0-139">-WebSpaceName</span></span>
<span data-ttu-id="358d0-140">Anger namnet på ett webbområde i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="358d0-140">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="358d0-141">Som standard får **Get-AzureWebHostingPlanMetric** alla planer i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="358d0-141">By default, **Get-AzureWebHostingPlanMetric** gets all plans in the current subscription.</span></span>
<span data-ttu-id="358d0-142">Den här parametern stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="358d0-142">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358d0-143">CommonParameters</span></span>
<span data-ttu-id="358d0-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358d0-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358d0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358d0-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="358d0-146">INPUTS</span></span>

###  
<span data-ttu-id="358d0-147">Du kan skicka data till denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="358d0-147">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="358d0-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="358d0-148">OUTPUTS</span></span>

###  
<span data-ttu-id="358d0-149">Microsoft. WindowsAzure. commands. Utilities. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="358d0-149">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>

<span data-ttu-id="358d0-150">Som standard returnerar **Get-AzureWebHostingPlanMetric** en matris med **MetricResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="358d0-150">By default, **Get-AzureWebHostingPlanMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="358d0-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="358d0-151">NOTES</span></span>

## <span data-ttu-id="358d0-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="358d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="358d0-153">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="358d0-153">Get-AzureWebHostingPlan</span></span>](./Get-AzureWebHostingPlan.md)


