---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLog.md
ms.openlocfilehash: f6d0181562d9d43c12fbcfd046350e9d930f2320
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925705"
---
# <span data-ttu-id="5b3ac-101">Get-AzLog</span><span class="sxs-lookup"><span data-stu-id="5b3ac-101">Get-AzLog</span></span>

## <span data-ttu-id="5b3ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3ac-103">Hämta händelser för aktivitets loggen.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-103">Retrieve Activity Log events.</span></span>

## <span data-ttu-id="5b3ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b3ac-104">SYNTAX</span></span>

### <span data-ttu-id="5b3ac-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-105">GetByCorrelationId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-106">GetByResourceId</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b3ac-107">GetByResourceGroup</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceGroupName] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5b3ac-108">GetByResourceProvider</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="5b3ac-109">GetBySubscription</span></span>
```
Get-AzLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>] [-DetailedOutput]
 [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b3ac-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b3ac-110">DESCRIPTION</span></span>
<span data-ttu-id="5b3ac-111">Cmdleten **Get-AzLog** .</span><span class="sxs-lookup"><span data-stu-id="5b3ac-111">The **Get-AzLog** cmdlet retrieve Activity Log events.</span></span>
<span data-ttu-id="5b3ac-112">Händelserna kan associeras med aktuellt prenumerations-ID, korrelations-ID, resurs grupp, resurs-ID eller resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="5b3ac-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b3ac-113">EXAMPLES</span></span>

### <span data-ttu-id="5b3ac-114">Exempel 1: Hämta en händelse logg efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="5b3ac-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzLog
```

<span data-ttu-id="5b3ac-115">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-116">Exempel 2: Hämta en händelse logg per prenumerations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="5b3ac-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -MaxRecord 100
```

<span data-ttu-id="5b3ac-117">Det här kommandot listar de flesta 100-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-118">Exempel 3: Hämta en händelse logg efter prenumerations-ID med start tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="5b3ac-119">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 06-01T10:30 lokal tid om detta datum/tid inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-120">Exempel 4: Hämta en händelse logg efter abonnemangs-ID med start-och slut tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="5b3ac-121">Det här kommandot listar de flesta 1000 av de händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 04-01T10:30 lokal tid och tidigare än 2017-04-14T11:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5b3ac-122">Exempel 5: Hämta en händelse logg efter ett korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="5b3ac-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="5b3ac-123">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5b3ac-124">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="5b3ac-125">Exempel 6: Hämta en händelse logg efter ett korrelations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="5b3ac-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

<span data-ttu-id="5b3ac-126">Det här kommandot listar de flesta 100-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="5b3ac-127">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="5b3ac-128">Exempel 7: Hämta en händelse logg genom att använda ett korrelations-ID och start tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5b3ac-129">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 05-22T04.30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="5b3ac-130">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="5b3ac-131">Exempel 8: Hämta en händelse logg efter ett korrelations-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="5b3ac-132">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 04-15T04 = 30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5b3ac-133">Exempel 9: Hämta en händelse logg för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5b3ac-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="5b3ac-134">Det här kommandot listar 1000 de händelser som är kopplade till den angivna resurs gruppen som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-135">Exempel 10: Hämta en händelse logg för en resurs grupp med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="5b3ac-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

<span data-ttu-id="5b3ac-136">Det här kommandot listar högst 100 händelser kopplade till den angivna resurs gruppen som ägde rum 7 dagar efter det aktuella datumet/tiden.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-137">Exempel 11: Hämta en händelse logg för en resurs grupp efter start tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="5b3ac-138">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-138">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-139">Exempel 12: Hämta en händelse logg för en resurs grupp med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5b3ac-140">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5b3ac-141">Exempel 13: Hämta en händelse logg efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="5b3ac-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="5b3ac-142">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-143">Exempel 14: Hämta en händelse logg efter resurs-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="5b3ac-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

<span data-ttu-id="5b3ac-144">Det här kommandot listar de flesta 100-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-145">Exempel 15: Hämta en händelse logg efter resurs-ID med en start tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5b3ac-146">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-147">Exempel 16: Hämta en händelse logg efter resurs-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5b3ac-148">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="5b3ac-149">Exempel 17: Hämta en händelse logg per resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="5b3ac-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="5b3ac-150">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-151">Exempel 18: Hämta en händelse logg från en resurs leverantör med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="5b3ac-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

<span data-ttu-id="5b3ac-152">Det här kommandot listar de flesta 100-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-153">Exempel 19: Hämta en händelse logg från en resurs leverantör med en start tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="5b3ac-154">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="5b3ac-155">Exempel 20: Hämta en händelse logg från en resurs leverantör med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="5b3ac-156">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="5b3ac-157">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b3ac-157">PARAMETERS</span></span>

### <span data-ttu-id="5b3ac-158">-Ringer</span><span class="sxs-lookup"><span data-stu-id="5b3ac-158">-Caller</span></span>
<span data-ttu-id="5b3ac-159">Anger en uppringare.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="5b3ac-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-160">-CorrelationId</span></span>
<span data-ttu-id="5b3ac-161">Anger korrelations-ID.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="5b3ac-162">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-162">This parameter is required.</span></span>

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

### <span data-ttu-id="5b3ac-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3ac-163">-DefaultProfile</span></span>
<span data-ttu-id="5b3ac-164">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5b3ac-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b3ac-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="5b3ac-165">-DetailedOutput</span></span>
<span data-ttu-id="5b3ac-166">Anger att den här cmdleten visar detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="5b3ac-167">Utdata sammanfattas som standard.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-167">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3ac-168">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="5b3ac-168">-EndTime</span></span>
<span data-ttu-id="5b3ac-169">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="5b3ac-170">Standardvärdet är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-170">The default value is the current time.</span></span>
<span data-ttu-id="5b3ac-171">Värdet måste vara senare än *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="5b3ac-172">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3ac-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="5b3ac-173">-MaxRecord</span></span>
<span data-ttu-id="5b3ac-174">Anger det totala antalet poster som ska hämtas för det angivna filtret.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="5b3ac-175">Standardvärdet är 1000 och det högsta tillåtna värdet är 100000.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="5b3ac-176">Negativa värden och 0 ignoreras och standardvärdet används.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-176">Negative values and 0 are ignored and the default value will be used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3ac-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3ac-177">-ResourceGroupName</span></span>
<span data-ttu-id="5b3ac-178">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5b3ac-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-179">-ResourceId</span></span>
<span data-ttu-id="5b3ac-180">Anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="5b3ac-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5b3ac-181">-ResourceProvider</span></span>
<span data-ttu-id="5b3ac-182">Anger ett filter efter resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="5b3ac-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5b3ac-183">-StartTime</span></span>
<span data-ttu-id="5b3ac-184">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="5b3ac-185">Standardvärdet är *slut* tid minus sju dagar.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="5b3ac-186">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b3ac-187">-Status</span><span class="sxs-lookup"><span data-stu-id="5b3ac-187">-Status</span></span>
<span data-ttu-id="5b3ac-188">Anger status.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-188">Specifies the status.</span></span>

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

### <span data-ttu-id="5b3ac-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3ac-189">CommonParameters</span></span>
<span data-ttu-id="5b3ac-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3ac-191">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b3ac-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3ac-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b3ac-192">INPUTS</span></span>

### <span data-ttu-id="5b3ac-193">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b3ac-193">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5b3ac-194">System. String</span><span class="sxs-lookup"><span data-stu-id="5b3ac-194">System.String</span></span>

### <span data-ttu-id="5b3ac-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b3ac-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5b3ac-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5b3ac-196">System.Int32</span></span>

## <span data-ttu-id="5b3ac-197">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b3ac-197">OUTPUTS</span></span>

### <span data-ttu-id="5b3ac-198">Microsoft. Azure. commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="5b3ac-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="5b3ac-199">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b3ac-199">NOTES</span></span>

## <span data-ttu-id="5b3ac-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b3ac-200">RELATED LINKS</span></span>
