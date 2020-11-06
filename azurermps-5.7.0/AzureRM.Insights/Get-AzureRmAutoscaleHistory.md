---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 3bd987fe1007ae9f96268225106eb2046e1a4afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573427"
---
# <span data-ttu-id="402e9-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="402e9-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="402e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="402e9-102">SYNOPSIS</span></span>
<span data-ttu-id="402e9-103">Hämtar den automatiska skalnings historiken.</span><span class="sxs-lookup"><span data-stu-id="402e9-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="402e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="402e9-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="402e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="402e9-105">DESCRIPTION</span></span>
<span data-ttu-id="402e9-106">Cmdleten **Get-AzureRmAutoscaleHistory** hämtar historiken för händelser relaterade till en autoskalningsinställning.</span><span class="sxs-lookup"><span data-stu-id="402e9-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="402e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="402e9-107">EXAMPLES</span></span>

### <span data-ttu-id="402e9-108">Exempel 1: Hämta alla händelser som är kopplade till ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="402e9-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="402e9-109">Det här kommandot får alla Autoskala-relaterade händelser som är kopplade till det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="402e9-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="402e9-110">Exempel 2: GetAutoscaleHistory för en viss resurs</span><span class="sxs-lookup"><span data-stu-id="402e9-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="402e9-111">Det här kommandot får alla Autoskala-relaterade händelser som är kopplade till en viss resurs som identifieras av resursens ID (egentligen, ResourceUri).</span><span class="sxs-lookup"><span data-stu-id="402e9-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="402e9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="402e9-112">PARAMETERS</span></span>

### <span data-ttu-id="402e9-113">-Ringer</span><span class="sxs-lookup"><span data-stu-id="402e9-113">-Caller</span></span>
<span data-ttu-id="402e9-114">Anger en uppringare.</span><span class="sxs-lookup"><span data-stu-id="402e9-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="402e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402e9-115">-DefaultProfile</span></span>
<span data-ttu-id="402e9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="402e9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="402e9-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="402e9-117">-DetailedOutput</span></span>
<span data-ttu-id="402e9-118">Anger att den här åtgärden innehöll detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="402e9-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="402e9-119">Om du inte anger den här parametern sammanfattas utdata.</span><span class="sxs-lookup"><span data-stu-id="402e9-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="402e9-120">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="402e9-120">-EndTime</span></span>
<span data-ttu-id="402e9-121">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="402e9-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="402e9-122">Standardinställningen är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="402e9-122">The default is the current time.</span></span>

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

### <span data-ttu-id="402e9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="402e9-123">-ResourceId</span></span>
<span data-ttu-id="402e9-124">Anger det resurs-ID som den autoskalningsinställning är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="402e9-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="402e9-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="402e9-125">-StartTime</span></span>
<span data-ttu-id="402e9-126">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="402e9-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="402e9-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="402e9-127">This parameter is optional.</span></span>
<span data-ttu-id="402e9-128">Standardvärdet är den aktuella lokala tiden minus en timme.</span><span class="sxs-lookup"><span data-stu-id="402e9-128">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="402e9-129">-Status</span><span class="sxs-lookup"><span data-stu-id="402e9-129">-Status</span></span>
<span data-ttu-id="402e9-130">Anger ett filter efter status.</span><span class="sxs-lookup"><span data-stu-id="402e9-130">Specifies a filter by status.</span></span>
<span data-ttu-id="402e9-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="402e9-131">This parameter is optional.</span></span>
<span data-ttu-id="402e9-132">Felet är en tom sträng (det vill säga inga filter)</span><span class="sxs-lookup"><span data-stu-id="402e9-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="402e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402e9-133">CommonParameters</span></span>
<span data-ttu-id="402e9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402e9-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="402e9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402e9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="402e9-136">INPUTS</span></span>

### <span data-ttu-id="402e9-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="402e9-137">None</span></span>
<span data-ttu-id="402e9-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="402e9-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="402e9-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="402e9-139">OUTPUTS</span></span>

### <span data-ttu-id="402e9-140">List<Microsoft. Azure.-kommandon. Insights. OutputClasses. PSEventData></span><span class="sxs-lookup"><span data-stu-id="402e9-140">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData></span></span>

## <span data-ttu-id="402e9-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="402e9-141">NOTES</span></span>

## <span data-ttu-id="402e9-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="402e9-142">RELATED LINKS</span></span>

[<span data-ttu-id="402e9-143">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="402e9-143">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="402e9-144">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="402e9-144">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="402e9-145">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="402e9-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


