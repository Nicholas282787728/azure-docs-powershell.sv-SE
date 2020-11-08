---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271842"
---
# <span data-ttu-id="74f32-101">Get-AzActivityLog</span><span class="sxs-lookup"><span data-stu-id="74f32-101">Get-AzActivityLog</span></span>

## <span data-ttu-id="74f32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74f32-102">SYNOPSIS</span></span>
<span data-ttu-id="74f32-103">Hämta händelser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="74f32-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="74f32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74f32-104">SYNTAX</span></span>

### <span data-ttu-id="74f32-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="74f32-105">GetByCorrelationId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74f32-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74f32-106">GetByResourceId</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74f32-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="74f32-107">GetByResourceGroup</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74f32-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="74f32-108">GetByResourceProvider</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74f32-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="74f32-109">GetBySubscription</span></span>
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f32-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74f32-110">DESCRIPTION</span></span>
<span data-ttu-id="74f32-111">Get-AzActivityLog cmdlet hämtar händelser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="74f32-111">The Get-AzActivityLog cmdlet retrieve Activity Log events.</span></span> <span data-ttu-id="74f32-112">Händelserna kan associeras med aktuellt prenumerations-ID, korrelations-ID, resurs grupp, resurs-ID eller resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="74f32-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="74f32-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74f32-113">EXAMPLES</span></span>

### <span data-ttu-id="74f32-114">Exempel 1: Hämta en händelse logg efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="74f32-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-ActivityAzLog
```

<span data-ttu-id="74f32-115">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-116">Exempel 2: Hämta en händelse logg per prenumerations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="74f32-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

<span data-ttu-id="74f32-117">Det här kommandot listar de flesta 100-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-118">Exempel 3: Hämta en händelse logg efter prenumerations-ID med start tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="74f32-119">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 06-01T10:30 lokal tid om detta datum/tid inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-120">Exempel 4: Hämta en händelse logg efter abonnemangs-ID med start-och slut tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="74f32-121">Det här kommandot listar de flesta 1000 av de händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 04-01T10:30 lokal tid och tidigare än 2017-04-14T11:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.</span><span class="sxs-lookup"><span data-stu-id="74f32-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="74f32-122">Exempel 5: Hämta en händelse logg efter ett korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="74f32-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="74f32-123">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="74f32-124">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="74f32-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="74f32-125">Exempel 6: Hämta en händelse logg efter ett korrelations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="74f32-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="74f32-126">Det här kommandot listar de flesta 100-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="74f32-127">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="74f32-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="74f32-128">Exempel 7: Hämta en händelse logg genom att använda ett korrelations-ID och start tid</span><span class="sxs-lookup"><span data-stu-id="74f32-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="74f32-129">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 05-22T04.30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="74f32-130">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="74f32-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="74f32-131">Exempel 8: Hämta en händelse logg efter ett korrelations-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="74f32-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="74f32-132">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 04-15T04 = 30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="74f32-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="74f32-133">Exempel 9: Hämta en händelse logg för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="74f32-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="74f32-134">Det här kommandot listar 1000 de händelser som är kopplade till den angivna resurs gruppen som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-135">Exempel 10: Hämta en händelse logg för en resurs grupp med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="74f32-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="74f32-136">Det här kommandot listar högst 100 händelser kopplade till den angivna resurs gruppen som ägde rum 7 dagar efter det aktuella datumet/tiden.</span><span class="sxs-lookup"><span data-stu-id="74f32-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-137">Exempel 11: Hämta en händelse logg för en resurs grupp efter start tid</span><span class="sxs-lookup"><span data-stu-id="74f32-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="74f32-138">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-139">Exempel 12: Hämta en händelse logg för en resurs grupp med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="74f32-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="74f32-140">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="74f32-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="74f32-141">Exempel 13: Hämta en händelse logg efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="74f32-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="74f32-142">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-143">Exempel 14: Hämta en händelse logg efter resurs-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="74f32-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="74f32-144">Det här kommandot listar de flesta 100-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-145">Exempel 15: Hämta en händelse logg efter resurs-ID med en start tid</span><span class="sxs-lookup"><span data-stu-id="74f32-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="74f32-146">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-147">Exempel 16: Hämta en händelse logg efter resurs-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="74f32-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="74f32-148">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="74f32-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="74f32-149">Exempel 17: Hämta en händelse logg per resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="74f32-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="74f32-150">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-151">Exempel 18: Hämta en händelse logg från en resurs leverantör med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="74f32-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="74f32-152">Det här kommandot listar de flesta 100-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-153">Exempel 19: Hämta en händelse logg från en resurs leverantör med en start tid</span><span class="sxs-lookup"><span data-stu-id="74f32-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="74f32-154">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="74f32-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="74f32-155">Exempel 20: Hämta en händelse logg från en resurs leverantör med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="74f32-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="74f32-156">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="74f32-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="74f32-157">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74f32-157">PARAMETERS</span></span>

### <span data-ttu-id="74f32-158">-Ringer</span><span class="sxs-lookup"><span data-stu-id="74f32-158">-Caller</span></span>
<span data-ttu-id="74f32-159">Uppringarens händelser som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="74f32-159">The caller of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="74f32-160">-CorrelationId</span></span>
<span data-ttu-id="74f32-161">CorrelationId</span><span class="sxs-lookup"><span data-stu-id="74f32-161">The CorrelationId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f32-162">-DefaultProfile</span></span>
<span data-ttu-id="74f32-163">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74f32-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f32-164">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="74f32-164">-DetailedOutput</span></span>
<span data-ttu-id="74f32-165">Returnera objekt med all information om händelserna (Standardinställningen är att endast returnera vissa attribut, dvs. ingen detalj)</span><span class="sxs-lookup"><span data-stu-id="74f32-165">Return object with all the details of the events (the default is to return only some attributes, i.e. no detail)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-166">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="74f32-166">-EndTime</span></span>
<span data-ttu-id="74f32-167">Slut tid för frågan</span><span class="sxs-lookup"><span data-stu-id="74f32-167">The endTime of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-168">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="74f32-168">-MaxRecord</span></span>
<span data-ttu-id="74f32-169">Det maximala antalet poster som hämtas.</span><span class="sxs-lookup"><span data-stu-id="74f32-169">The maximum number of records to fetch.</span></span>
<span data-ttu-id="74f32-170">Alias: MaxRecords, MaxEvents</span><span class="sxs-lookup"><span data-stu-id="74f32-170">Alias: MaxRecords, MaxEvents</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f32-171">-ResourceGroupName</span></span>
<span data-ttu-id="74f32-172">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="74f32-172">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f32-173">-ResourceId</span></span>
<span data-ttu-id="74f32-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="74f32-174">The ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-175">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="74f32-175">-ResourceProvider</span></span>
<span data-ttu-id="74f32-176">ResourceProvider namn</span><span class="sxs-lookup"><span data-stu-id="74f32-176">The ResourceProvider name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-177">-StartTime</span><span class="sxs-lookup"><span data-stu-id="74f32-177">-StartTime</span></span>
<span data-ttu-id="74f32-178">Ett correlationId för frågan</span><span class="sxs-lookup"><span data-stu-id="74f32-178">The correlationId of the query</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-179">-Status</span><span class="sxs-lookup"><span data-stu-id="74f32-179">-Status</span></span>
<span data-ttu-id="74f32-180">Status för de händelser som ska hämtas</span><span class="sxs-lookup"><span data-stu-id="74f32-180">The status of the events to fetch</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74f32-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f32-181">CommonParameters</span></span>
<span data-ttu-id="74f32-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f32-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f32-183">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74f32-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f32-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74f32-184">INPUTS</span></span>

### <span data-ttu-id="74f32-185">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74f32-185">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74f32-186">System. String</span><span class="sxs-lookup"><span data-stu-id="74f32-186">System.String</span></span>

### <span data-ttu-id="74f32-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74f32-187">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="74f32-188">System. Int32</span><span class="sxs-lookup"><span data-stu-id="74f32-188">System.Int32</span></span>

## <span data-ttu-id="74f32-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74f32-189">OUTPUTS</span></span>

### <span data-ttu-id="74f32-190">Microsoft. Azure. commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="74f32-190">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="74f32-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74f32-191">NOTES</span></span>

## <span data-ttu-id="74f32-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74f32-192">RELATED LINKS</span></span>
