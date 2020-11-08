---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099006"
---
# <span data-ttu-id="d6113-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d6113-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="d6113-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6113-102">SYNOPSIS</span></span>
<span data-ttu-id="d6113-103">Initierar en failover-åtgärd för volym behållar grupper.</span><span class="sxs-lookup"><span data-stu-id="d6113-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="d6113-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6113-104">SYNTAX</span></span>

### <span data-ttu-id="d6113-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="d6113-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d6113-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d6113-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d6113-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="d6113-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d6113-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6113-108">DESCRIPTION</span></span>
<span data-ttu-id="d6113-109">Cmdleten **Start-AzureStorSimpleDeviceFailoverJob** initierar en redundansväxling av en eller flera volym behållar grupper från en enhet till en annan.</span><span class="sxs-lookup"><span data-stu-id="d6113-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="d6113-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6113-110">EXAMPLES</span></span>

### <span data-ttu-id="d6113-111">Exempel 1: starta ett failover-jobb för en namngiven enhet och en namngiven mål enhet</span><span class="sxs-lookup"><span data-stu-id="d6113-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="d6113-112">Det här kommandot får volym containrarna för enheten som heter ChewD_App7 genom att använda cmdleten **Get-AzureStorSimpleFailoverVolumeContainers** .</span><span class="sxs-lookup"><span data-stu-id="d6113-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="d6113-113">Kommandot skickar resultaten till cmdleten **Where-Object** , som avslutar de behållare som har ett annat värde än $True för egenskapen **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="d6113-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="d6113-114">Om du vill ha mer information skriver du `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="d6113-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="d6113-115">Den aktuella cmdleten startar failover-jobb för återstående enheter med växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="d6113-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="d6113-116">Kommandot anger enhetens namn och mål enhetens namn.</span><span class="sxs-lookup"><span data-stu-id="d6113-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="d6113-117">Kommandot returnerar instans-ID för jobbet som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="d6113-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="d6113-118">Exempel 2: starta ett failover-jobb för en enhet och en måldator som anges av ID</span><span class="sxs-lookup"><span data-stu-id="d6113-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="d6113-119">Det här kommandot får volym containrarna för enheten med namn ChewD_App7 genom att använda **Get-AzureStorSimpleFailoverVolumeContainers**.</span><span class="sxs-lookup"><span data-stu-id="d6113-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="d6113-120">Kommandot skickar resultaten till **WHERE-objekt** , som ignorerar dem som har ett annat värde än $True för egenskapen **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="d6113-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="d6113-121">Cmdleten skickar resultaten till cmdleten **Select-Object** , som markerar det första objektet för överföring till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6113-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="d6113-122">Om du vill ha mer information skriver du `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="d6113-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="d6113-123">Den aktuella cmdleten startar redundans för den valda volymen.</span><span class="sxs-lookup"><span data-stu-id="d6113-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="d6113-124">Kommandot anger enhets-ID och Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="d6113-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="d6113-125">Kommandot returnerar instans-ID för jobbet som cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="d6113-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="d6113-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6113-126">PARAMETERS</span></span>

### <span data-ttu-id="d6113-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d6113-127">-DeviceId</span></span>
<span data-ttu-id="d6113-128">Anger instans-ID för den StorSimple-enhet som volym behållar gruppen finns på.</span><span class="sxs-lookup"><span data-stu-id="d6113-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-129">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="d6113-129">-DeviceName</span></span>
<span data-ttu-id="d6113-130">Anger namnet på den StorSimple-enhet som volym behållar grupper finns på.</span><span class="sxs-lookup"><span data-stu-id="d6113-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-131">-Force</span><span class="sxs-lookup"><span data-stu-id="d6113-131">-Force</span></span>
<span data-ttu-id="d6113-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d6113-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="d6113-133">-Profile</span></span>
<span data-ttu-id="d6113-134">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="d6113-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d6113-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="d6113-135">-TargetDeviceId</span></span>
<span data-ttu-id="d6113-136">Anger instans-ID för den StorSimple-enhet som cmdleten växlar till över volym behållar grupperna.</span><span class="sxs-lookup"><span data-stu-id="d6113-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="d6113-137">-TargetDeviceName</span></span>
<span data-ttu-id="d6113-138">Anger namnet på den StorSimple-enhet som cmdleten växlar till över volym behållar grupperna.</span><span class="sxs-lookup"><span data-stu-id="d6113-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="d6113-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="d6113-140">Anger listan över volym behållar grupper som denna cmdlet växlar över till en annan enhet.</span><span class="sxs-lookup"><span data-stu-id="d6113-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6113-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6113-141">CommonParameters</span></span>
<span data-ttu-id="d6113-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6113-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6113-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6113-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6113-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6113-144">INPUTS</span></span>

### <span data-ttu-id="d6113-145">Förteckning\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="d6113-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="d6113-146">Du kan visa en lista med volym behållar grupper för denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6113-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="d6113-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6113-147">OUTPUTS</span></span>

### <span data-ttu-id="d6113-148">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d6113-148">String</span></span>

## <span data-ttu-id="d6113-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6113-149">NOTES</span></span>

## <span data-ttu-id="d6113-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6113-150">RELATED LINKS</span></span>

[<span data-ttu-id="d6113-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="d6113-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


