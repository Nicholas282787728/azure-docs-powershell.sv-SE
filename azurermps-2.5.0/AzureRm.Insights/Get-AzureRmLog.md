---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
ms.openlocfilehash: 2c63efe0d22f1582b0828f595ba8a72cd389b435
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928882"
---
# <span data-ttu-id="a0e7a-101">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="a0e7a-101">Get-AzureRmLog</span></span>

## <span data-ttu-id="a0e7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e7a-103">Hämtar en logg över händelser.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-103">Gets a log of events.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0e7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0e7a-104">SYNTAX</span></span>

### <span data-ttu-id="a0e7a-105">GetByCorrelationId</span><span class="sxs-lookup"><span data-stu-id="a0e7a-105">GetByCorrelationId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0e7a-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0e7a-106">GetByResourceId</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0e7a-107">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0e7a-107">GetByResourceGroup</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0e7a-108">GetByResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a0e7a-108">GetByResourceProvider</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0e7a-109">GetBySubscription</span><span class="sxs-lookup"><span data-stu-id="a0e7a-109">GetBySubscription</span></span>
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0e7a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0e7a-110">DESCRIPTION</span></span>
<span data-ttu-id="a0e7a-111">Cmdleten **Get-AzureRmLog** hämtar en logg över händelser.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-111">The **Get-AzureRmLog** cmdlet gets a log of events.</span></span>
<span data-ttu-id="a0e7a-112">Händelserna kan associeras med aktuellt prenumerations-ID, korrelations-ID, resurs grupp, resurs-ID eller resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-112">The events can be associated with the current subscription ID, correlation ID, resource group, resource ID, or resource provider.</span></span>

## <span data-ttu-id="a0e7a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0e7a-113">EXAMPLES</span></span>

### <span data-ttu-id="a0e7a-114">Exempel 1: Hämta en händelse logg efter abonnemangs-ID</span><span class="sxs-lookup"><span data-stu-id="a0e7a-114">Example 1: Get an event log by subscription ID</span></span>
```
PS C:\>Get-AzureRmLog
```

<span data-ttu-id="a0e7a-115">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-115">This command lists at most 1000 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-116">Exempel 2: Hämta en händelse logg per prenumerations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="a0e7a-116">Example 2: Get an event log by subscription ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

<span data-ttu-id="a0e7a-117">Det här kommandot listar de flesta 100-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-117">This command lists at most 100 events associated with the user's subscription ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-118">Exempel 3: Hämta en händelse logg efter prenumerations-ID med start tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-118">Example 3: Get an event log by subscription ID with a start time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

<span data-ttu-id="a0e7a-119">Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 06-01T10:30 lokal tid om detta datum/tid inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-119">This command lists at most 1000 events associated with the user's subscription ID that took place on or after 2017-06-01T10:30 local time if that date/time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-120">Exempel 4: Hämta en händelse logg efter abonnemangs-ID med start-och slut tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-120">Example 4: Get an event log by subscription ID with a start time and end time.</span></span>
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

<span data-ttu-id="a0e7a-121">Det här kommandot listar de flesta 1000 av de händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 04-01T10:30 lokal tid och tidigare än 2017-04-14T11:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-121">This command lists at most 1000 of the events associated with the user's subscription ID that took place on or after 2017-04-01T10:30 local time, and before 2017-04-14T11:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="a0e7a-122">Exempel 5: Hämta en händelse logg efter ett korrelations-ID</span><span class="sxs-lookup"><span data-stu-id="a0e7a-122">Example 5: Get an event log by correlation ID</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

<span data-ttu-id="a0e7a-123">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-123">This command lists at most 1000 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="a0e7a-124">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-124">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="a0e7a-125">Exempel 6: Hämta en händelse logg efter ett korrelations-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="a0e7a-125">Example 6: Get an event log by correlation ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

<span data-ttu-id="a0e7a-126">Det här kommandot listar de flesta 100-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-126">This command lists at most 100 events associated with the specified correlation ID that took place 7 days from the current date/time.</span></span> 
<span data-ttu-id="a0e7a-127">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-127">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="a0e7a-128">Exempel 7: Hämta en händelse logg genom att använda ett korrelations-ID och start tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-128">Example 7: Get an event log by correlation ID and start time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="a0e7a-129">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 05-22T04.30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-129">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>
<span data-ttu-id="a0e7a-130">**Obs!** detta är vanligt vis bara en händelse.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-130">**NOTE** : this is usually only one event.</span></span>

### <span data-ttu-id="a0e7a-131">Exempel 8: Hämta en händelse logg efter ett korrelations-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-131">Example 8: Get an event log by correlation ID with start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

<span data-ttu-id="a0e7a-132">Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 04-15T04 = 30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-132">This command lists at most 1000 events associated with the specified correlation ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="a0e7a-133">Exempel 9: Hämta en händelse logg för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a0e7a-133">Example 9: Get an event log for a resource group</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

<span data-ttu-id="a0e7a-134">Det här kommandot listar 1000 de händelser som är kopplade till den angivna resurs gruppen som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-134">This command lists at most 1000 the events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-135">Exempel 10: Hämta en händelse logg för en resurs grupp med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="a0e7a-135">Example 10: Get an event log for a resource group with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

<span data-ttu-id="a0e7a-136">Det här kommandot listar högst 100 händelser kopplade till den angivna resurs gruppen som ägde rum 7 dagar efter det aktuella datumet/tiden.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-136">This command lists at most 100 events associated with the specified resource group that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-137">Exempel 11: Hämta en händelse logg för en resurs grupp efter start tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-137">Example 11: Get an event log for a resource group by start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

<span data-ttu-id="a0e7a-138">Det här kommandot listar högst 1000 evetns associerade med den angivna resurs gruppen som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-138">This command lists at most 1000 evetns associated with the specified resource group that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-139">Exempel 12: Hämta en händelse logg för en resurs grupp med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-139">Example 12: Get an event log for a resource group with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="a0e7a-140">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-140">This command lists at most 1000 events associated with the specified resource group that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="a0e7a-141">Exempel 13: Hämta en händelse logg efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="a0e7a-141">Example 13: Get an event log by resource ID</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

<span data-ttu-id="a0e7a-142">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-142">This command lists at most 1000 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-143">Exempel 14: Hämta en händelse logg efter resurs-ID med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="a0e7a-143">Example 14: Get an event log by resource ID with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

<span data-ttu-id="a0e7a-144">Det här kommandot listar de flesta 100-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-144">This command lists at most 100 events associated with the specified resource ID that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-145">Exempel 15: Hämta en händelse logg efter resurs-ID med en start tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-145">Example 15: Get an event log by resource ID with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="a0e7a-146">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-146">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-147">Exempel 16: Hämta en händelse logg efter resurs-ID med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-147">Example 16: Get an event log by resource ID with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="a0e7a-148">Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-148">This command lists at most 1000 events associated with the specified resource ID that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

### <span data-ttu-id="a0e7a-149">Exempel 17: Hämta en händelse logg per resurs leverantör</span><span class="sxs-lookup"><span data-stu-id="a0e7a-149">Example 17: Get an event log by resource provider</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

<span data-ttu-id="a0e7a-150">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-150">This command lists at most 1000 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-151">Exempel 18: Hämta en händelse logg från en resurs leverantör med maximalt antal händelser</span><span class="sxs-lookup"><span data-stu-id="a0e7a-151">Example 18: Get an event log by resource provider with a maximum number of events</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

<span data-ttu-id="a0e7a-152">Det här kommandot listar de flesta 100-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-152">This command lists at most 100 events associated with the specified resource provider that took place 7 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-153">Exempel 19: Hämta en händelse logg från en resurs leverantör med en start tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-153">Example 19: Get an event log by resource provider with a start time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

<span data-ttu-id="a0e7a-154">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-154">This command lists at most 1000 events associated with the specified resource provider that took place on or after  2017-05-22T04:30:00 local time if the start time is not older than 90 days from the current date/time.</span></span>

### <span data-ttu-id="a0e7a-155">Exempel 20: Hämta en händelse logg från en resurs leverantör med start-och slut tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-155">Example 20: Get an event log by resource provider with a start time and end time</span></span>
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

<span data-ttu-id="a0e7a-156">Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-156">This command lists at most 1000 events associated with the specified resource provider that took place on or after 2017-04-15T04:30 local time, but before 2017-04-25T12:30 local time if the whole date/time range is not older than 90 days from the current date/time, i.e.: the retention period.</span></span>

## <span data-ttu-id="a0e7a-157">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0e7a-157">PARAMETERS</span></span>

### <span data-ttu-id="a0e7a-158">-Ringer</span><span class="sxs-lookup"><span data-stu-id="a0e7a-158">-Caller</span></span>
<span data-ttu-id="a0e7a-159">Anger en uppringare.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-159">Specifies a caller.</span></span>

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

### <span data-ttu-id="a0e7a-160">-CorrelationId</span><span class="sxs-lookup"><span data-stu-id="a0e7a-160">-CorrelationId</span></span>
<span data-ttu-id="a0e7a-161">Anger korrelations-ID.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-161">Specifies the correlation ID.</span></span>
<span data-ttu-id="a0e7a-162">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-162">This parameter is required.</span></span>

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

### <span data-ttu-id="a0e7a-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e7a-163">-DefaultProfile</span></span>
<span data-ttu-id="a0e7a-164">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0e7a-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e7a-165">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="a0e7a-165">-DetailedOutput</span></span>
<span data-ttu-id="a0e7a-166">Anger att den här cmdleten visar detaljerade utdata.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-166">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="a0e7a-167">Utdata sammanfattas som standard.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-167">By default, output is summarized.</span></span>

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

### <span data-ttu-id="a0e7a-168">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="a0e7a-168">-EndTime</span></span>
<span data-ttu-id="a0e7a-169">Anger slut tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-169">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="a0e7a-170">Standardvärdet är den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-170">The default value is the current time.</span></span>
<span data-ttu-id="a0e7a-171">Värdet måste vara senare än *StartTime*.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-171">The value must be later than *StartTime*.</span></span>
<span data-ttu-id="a0e7a-172">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-172">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="a0e7a-173">-MaxRecord</span><span class="sxs-lookup"><span data-stu-id="a0e7a-173">-MaxRecord</span></span>
<span data-ttu-id="a0e7a-174">Anger det totala antalet poster som ska hämtas för det angivna filtret.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-174">Specifies the total number of records to fetch for the specified filter.</span></span>
<span data-ttu-id="a0e7a-175">Standardvärdet är 1000 och det högsta tillåtna värdet är 100000.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-175">The default value is 1000 and the maximum value accepted is 100000.</span></span> <span data-ttu-id="a0e7a-176">Negativa värden och 0 ignoreras och standardvärdet används.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-176">Negative values and 0 are ignored and the default value will be used.</span></span>

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

### <span data-ttu-id="a0e7a-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e7a-177">-ResourceGroupName</span></span>
<span data-ttu-id="a0e7a-178">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-178">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a0e7a-179">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0e7a-179">-ResourceId</span></span>
<span data-ttu-id="a0e7a-180">Anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-180">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="a0e7a-181">-ResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a0e7a-181">-ResourceProvider</span></span>
<span data-ttu-id="a0e7a-182">Anger ett filter efter resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-182">Specifies a filter by resource provider.</span></span>

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

### <span data-ttu-id="a0e7a-183">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a0e7a-183">-StartTime</span></span>
<span data-ttu-id="a0e7a-184">Anger start tiden för frågan i lokal tid.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-184">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="a0e7a-185">Standardvärdet är *slut* tid minus sju dagar.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-185">The default value is *EndTime* minus seven days.</span></span>
<span data-ttu-id="a0e7a-186">Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-186">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

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

### <span data-ttu-id="a0e7a-187">-Status</span><span class="sxs-lookup"><span data-stu-id="a0e7a-187">-Status</span></span>
<span data-ttu-id="a0e7a-188">Anger status.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-188">Specifies the status.</span></span>

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

### <span data-ttu-id="a0e7a-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e7a-189">CommonParameters</span></span>
<span data-ttu-id="a0e7a-190">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0e7a-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e7a-191">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0e7a-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e7a-192">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0e7a-192">INPUTS</span></span>

### <span data-ttu-id="a0e7a-193">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a0e7a-193">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a0e7a-194">System. String</span><span class="sxs-lookup"><span data-stu-id="a0e7a-194">System.String</span></span>

### <span data-ttu-id="a0e7a-195">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0e7a-195">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a0e7a-196">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a0e7a-196">System.Int32</span></span>

## <span data-ttu-id="a0e7a-197">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0e7a-197">OUTPUTS</span></span>

### <span data-ttu-id="a0e7a-198">Microsoft. Azure. commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="a0e7a-198">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="a0e7a-199">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0e7a-199">NOTES</span></span>

## <span data-ttu-id="a0e7a-200">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0e7a-200">RELATED LINKS</span></span>
