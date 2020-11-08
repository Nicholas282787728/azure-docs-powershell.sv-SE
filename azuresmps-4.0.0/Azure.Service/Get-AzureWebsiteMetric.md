---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099501"
---
# <span data-ttu-id="44a2f-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="44a2f-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="44a2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="44a2f-103">Hämtar mått för Azure-webbplatsen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="44a2f-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="44a2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44a2f-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44a2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="44a2f-106">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="44a2f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="44a2f-107">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="44a2f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="44a2f-108">Cmdleten **Get-AzureWebsiteMetric** hämtar Mät värden för Azure-webbplatsen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="44a2f-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="44a2f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44a2f-109">EXAMPLES</span></span>

### <span data-ttu-id="44a2f-110">Exempel 1: få mått för de senaste tre timmarna på en webbplats nivå</span><span class="sxs-lookup"><span data-stu-id="44a2f-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="44a2f-111">Det här kommandot får Mät värden för de senaste tre timmarna på en webbplats nivå per instans.</span><span class="sxs-lookup"><span data-stu-id="44a2f-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="44a2f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44a2f-112">PARAMETERS</span></span>

### <span data-ttu-id="44a2f-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="44a2f-113">-EndDate</span></span>
<span data-ttu-id="44a2f-114">Anger tiden, som ett **datetime** -objekt, för att sluta få mått.</span><span class="sxs-lookup"><span data-stu-id="44a2f-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="44a2f-115">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="44a2f-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="44a2f-116">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="44a2f-116">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="44a2f-117">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="44a2f-117">-InstanceDetails</span></span>
<span data-ttu-id="44a2f-118">Anger att denna cmdlet innehåller information om en viss nivå.</span><span class="sxs-lookup"><span data-stu-id="44a2f-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="44a2f-119">Om webb värds planen körs på två eller fler datorer returnerar denna cmdlet Mät värden för varje dator.</span><span class="sxs-lookup"><span data-stu-id="44a2f-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

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

### <span data-ttu-id="44a2f-120">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="44a2f-120">-MetricNames</span></span>
<span data-ttu-id="44a2f-121">Anger en matris med mät värden som ska visas.</span><span class="sxs-lookup"><span data-stu-id="44a2f-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="44a2f-122">Om du inte anger den här parametern får cmdleten alla mät värden.</span><span class="sxs-lookup"><span data-stu-id="44a2f-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

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

### <span data-ttu-id="44a2f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="44a2f-123">-Name</span></span>
<span data-ttu-id="44a2f-124">Anger namnet på en webbplats i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="44a2f-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="44a2f-125">Den här parametern stöder inte jokertecken.</span><span class="sxs-lookup"><span data-stu-id="44a2f-125">This parameter does not support wildcard characters.</span></span>

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

### <span data-ttu-id="44a2f-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="44a2f-126">-Profile</span></span>
<span data-ttu-id="44a2f-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="44a2f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44a2f-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="44a2f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44a2f-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="44a2f-129">-Slot</span></span>
<span data-ttu-id="44a2f-130">Anger miljön för en distribution av moln tjänster.</span><span class="sxs-lookup"><span data-stu-id="44a2f-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="44a2f-131">Giltiga värden är: produktion och mellanlagring.</span><span class="sxs-lookup"><span data-stu-id="44a2f-131">Valid values are: Production and Staging.</span></span>

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

### <span data-ttu-id="44a2f-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="44a2f-132">-SlotView</span></span>
<span data-ttu-id="44a2f-133">Anger att denna cmdlet får Mät värden för värd namnen som tar emot trafik på den aktuella platsen.</span><span class="sxs-lookup"><span data-stu-id="44a2f-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="44a2f-134">Om en byte inträffar under tids perioden slås måtten samman.</span><span class="sxs-lookup"><span data-stu-id="44a2f-134">If a swap occurs during the time period, the metrics are merged.</span></span>

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

### <span data-ttu-id="44a2f-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="44a2f-135">-StartDate</span></span>
<span data-ttu-id="44a2f-136">Anger tiden, som ett **datetime** -objekt, för att börja få mått.</span><span class="sxs-lookup"><span data-stu-id="44a2f-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

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

### <span data-ttu-id="44a2f-137">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="44a2f-137">-TimeGrain</span></span>
<span data-ttu-id="44a2f-138">Anger tidsenhet för mått.</span><span class="sxs-lookup"><span data-stu-id="44a2f-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="44a2f-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="44a2f-139">Valid values are:</span></span> 

- <span data-ttu-id="44a2f-140">PT1M (minut)</span><span class="sxs-lookup"><span data-stu-id="44a2f-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="44a2f-141">PT1H (timme)</span><span class="sxs-lookup"><span data-stu-id="44a2f-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="44a2f-142">P1D (dag)</span><span class="sxs-lookup"><span data-stu-id="44a2f-142">P1D (Day)</span></span>

<span data-ttu-id="44a2f-143">Standardvärdet är PT1H.</span><span class="sxs-lookup"><span data-stu-id="44a2f-143">The default value is PT1H.</span></span>

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

### <span data-ttu-id="44a2f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a2f-144">CommonParameters</span></span>
<span data-ttu-id="44a2f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a2f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a2f-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a2f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a2f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44a2f-147">INPUTS</span></span>

###  
<span data-ttu-id="44a2f-148">Du kan skicka data till denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="44a2f-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="44a2f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44a2f-149">OUTPUTS</span></span>

### <span data-ttu-id="44a2f-150">Microsoft. WindowsAzure. commands. Utilities. webentities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="44a2f-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="44a2f-151">Som standard returnerar **Get-AzureWebsiteMetric** en matris med **MetricResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="44a2f-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="44a2f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44a2f-152">NOTES</span></span>

## <span data-ttu-id="44a2f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44a2f-153">RELATED LINKS</span></span>

[<span data-ttu-id="44a2f-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="44a2f-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


