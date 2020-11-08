---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099520"
---
# <span data-ttu-id="3cb60-101">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="3cb60-101">Get-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="3cb60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cb60-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb60-103">Hämtar säkerhets kopior från en enhet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-103">Gets backups from a device.</span></span>

## <span data-ttu-id="3cb60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cb60-104">SYNTAX</span></span>

### <span data-ttu-id="3cb60-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="3cb60-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cb60-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="3cb60-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cb60-107">IdentifyById2</span><span class="sxs-lookup"><span data-stu-id="3cb60-107">IdentifyById2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cb60-108">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="3cb60-108">IdentifyByObject</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3cb60-109">IdentifyByObject2</span><span class="sxs-lookup"><span data-stu-id="3cb60-109">IdentifyByObject2</span></span>
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3cb60-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cb60-110">DESCRIPTION</span></span>
<span data-ttu-id="3cb60-111">Cmdleten **Get-AzureStorSimpleDeviceBackup** hämtar säkerhets kopior från en enhet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-111">The **Get-AzureStorSimpleDeviceBackup** cmdlet gets backups from a device.</span></span>
<span data-ttu-id="3cb60-112">Du kan ange säkerhets kopierings princip, volym och skapelse tid för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="3cb60-112">You can specify the backup policy, volume, and creation time for backups.</span></span>

<span data-ttu-id="3cb60-113">Denna cmdlet kan returnera högst 100 säkerhets kopior på den första sidan.</span><span class="sxs-lookup"><span data-stu-id="3cb60-113">This cmdlet can return a maximum of 100 backups in the first page.</span></span>
<span data-ttu-id="3cb60-114">Om det finns fler än 100 säkerhets kopior kan du hämta efterföljande sidor med hjälp av parametrarna *First* och *Skip* .</span><span class="sxs-lookup"><span data-stu-id="3cb60-114">If more than 100 backups exist, retrieve subsequent pages by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="3cb60-115">Om du anger ett värde på 100 för *Skip* och 50 för *First* returnerar denna cmdlet inte de första 100-resultaten.</span><span class="sxs-lookup"><span data-stu-id="3cb60-115">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="3cb60-116">Den returnerar nästföljande 50-resultat efter 100.</span><span class="sxs-lookup"><span data-stu-id="3cb60-116">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="3cb60-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cb60-117">EXAMPLES</span></span>

### <span data-ttu-id="3cb60-118">Exempel 1: Hämta alla säkerhets kopior på en enhet</span><span class="sxs-lookup"><span data-stu-id="3cb60-118">Example 1: Get all backups on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

<span data-ttu-id="3cb60-119">Det här kommandot får alla säkerhets kopior som finns på enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="3cb60-119">This command gets all backups that exist on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="3cb60-120">Om det finns fler än det högsta tillåtna antalet säkerhets kopior för 100 för den första sidan kan du använda parametrarna *First* och *Skip* för att visa fler resultat.</span><span class="sxs-lookup"><span data-stu-id="3cb60-120">If there are more than the maximum of 100 backups allowed for the first page, use the *First* and *Skip* parameters to view additional results.</span></span>

### <span data-ttu-id="3cb60-121">Exempel 2: Hämta säkerhets kopior som skapats mellan två datum</span><span class="sxs-lookup"><span data-stu-id="3cb60-121">Example 2: Get backups created between two dates</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

<span data-ttu-id="3cb60-122">Med det här kommandot får du säkerhets kopior på enheten Contoso63-AppVm som skapades på eller efter 10/7/2014 och på eller före 10/8/2014.</span><span class="sxs-lookup"><span data-stu-id="3cb60-122">This command gets backups on the device named Contoso63-AppVm that were created on or after 10/7/2014 and on or before 10/8/2014.</span></span>
<span data-ttu-id="3cb60-123">Den här cmdleten hoppar över det första resultatet och returnerar de två första resultaten efter det första resultatet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-123">This cmdlet skips the first result and returns the first two results after that first result.</span></span>
<span data-ttu-id="3cb60-124">Ändra värdena för *första* och *hoppa över* om du vill visa andra resultat.</span><span class="sxs-lookup"><span data-stu-id="3cb60-124">Modify values for *First* and *Skip* to view other results.</span></span>

### <span data-ttu-id="3cb60-125">Exempel 3: Hämta säkerhets kopior för ett säkerhets kopierings princip-ID</span><span class="sxs-lookup"><span data-stu-id="3cb60-125">Example 3: Get backups for a backup policy ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="3cb60-126">Med det här kommandot får du säkerhets kopior på den enhet som heter Contoso63-AppVm skapad på eller före angivet datum.</span><span class="sxs-lookup"><span data-stu-id="3cb60-126">This command gets backups on the device named Contoso63-AppVm created on or before the specified date.</span></span>
<span data-ttu-id="3cb60-127">Kommandot hämtar säkerhets kopior som skapades med den säkerhets kopierings princip som har det angivna ID: t.</span><span class="sxs-lookup"><span data-stu-id="3cb60-127">The command gets backups that were created by using the backup policy that has the specified ID.</span></span>
<span data-ttu-id="3cb60-128">Det här kommandot anger den *första* parametern, så att den endast returnerar de första 10 resultaten.</span><span class="sxs-lookup"><span data-stu-id="3cb60-128">This command specifies the *First* parameter, so it returns only the first 10 results.</span></span>

### <span data-ttu-id="3cb60-129">Exempel 4: Hämta säkerhets kopior för ett säkerhets kopierings princip objekt</span><span class="sxs-lookup"><span data-stu-id="3cb60-129">Example 4: Get backups for a backup policy object</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

<span data-ttu-id="3cb60-130">Det här kommandot får ett **BackupPolicyDetails** -objekt med cmdleten **Get-AzureStorSimpleDeviceBackupPolicy** och skickar sedan objektet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3cb60-130">This command gets a **BackupPolicyDetails** object by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3cb60-131">Denna cmdlet hämtar säkerhets kopior för enheten som heter Contoso63-AppVm skapad genom att använda säkerhets kopierings principen från den första delen av kommandot.</span><span class="sxs-lookup"><span data-stu-id="3cb60-131">That cmdlet gets backups for the device named Contoso63-AppVm created by using the backup policy from the first part of the command.</span></span>
<span data-ttu-id="3cb60-132">Kommandot får säkerhets kopior som skapats på eller före det angivna datumet, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="3cb60-132">The command gets backups created on or before the specified date, just as in the previous example.</span></span>
<span data-ttu-id="3cb60-133">Det här kommandot returnerar endast de 10 första resultaten.</span><span class="sxs-lookup"><span data-stu-id="3cb60-133">This command returns only the first 10 results.</span></span>

### <span data-ttu-id="3cb60-134">Exempel 5: skaffa en säkerhets kopia för ett volym-ID</span><span class="sxs-lookup"><span data-stu-id="3cb60-134">Example 5: Get a backup for a volume ID</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="3cb60-135">Med det här kommandot får du en säkerhets kopia på den enhet som skapas på den volym som har angivet instans-ID.</span><span class="sxs-lookup"><span data-stu-id="3cb60-135">This command gets a backup on the device that is created on the volume that has the specified instance ID.</span></span>
<span data-ttu-id="3cb60-136">Det här kommandot anger den *första* parametern, så att den endast returnerar det första resultatet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-136">This command specifies the *First* parameter, so it returns only the first one result.</span></span>

### <span data-ttu-id="3cb60-137">Exempel 6: skaffa en säkerhets kopia för ett volym namn</span><span class="sxs-lookup"><span data-stu-id="3cb60-137">Example 6: Get a backup for a volume name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

<span data-ttu-id="3cb60-138">Det här kommandot får ett **VirtualDisk** -objekt med cmdleten **Get-AzureStorSimpleDeviceVolume** och skickar sedan objektet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3cb60-138">This command gets a **VirtualDisk** object by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3cb60-139">Denna cmdlet hämtar säkerhets kopior för den enhet som heter Contoso63-AppVm skapad på volymen från den första delen av kommandot.</span><span class="sxs-lookup"><span data-stu-id="3cb60-139">That cmdlet gets backups for the device named Contoso63-AppVm created on the volume from the first part of the command.</span></span>
<span data-ttu-id="3cb60-140">Det här kommandot returnerar bara det första resultatet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-140">This command returns only the first result.</span></span>

## <span data-ttu-id="3cb60-141">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cb60-141">PARAMETERS</span></span>

### <span data-ttu-id="3cb60-142">-BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3cb60-142">-BackupPolicy</span></span>
<span data-ttu-id="3cb60-143">Anger ett **BackupPolicyDetails** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-143">Specifies a **BackupPolicyDetails** object.</span></span>
<span data-ttu-id="3cb60-144">Denna cmdlet använder **InstanceID** för detta objekt för att avgöra vilka säkerhets kopior som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="3cb60-144">This cmdlet uses the **InstanceId** of this object to determine which backups to get.</span></span>
<span data-ttu-id="3cb60-145">Om du vill hämta ett **BackupPolicyDetails** -objekt använder du cmdleten **Get-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="3cb60-145">To obtain a **BackupPolicyDetails** object, use the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-146">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="3cb60-146">-BackupPolicyId</span></span>
<span data-ttu-id="3cb60-147">Anger ett instans-ID för en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="3cb60-147">Specifies an instance ID of a backup policy.</span></span>
<span data-ttu-id="3cb60-148">Denna cmdlet hämtar säkerhets kopiering av enheter för den princip som anges.</span><span class="sxs-lookup"><span data-stu-id="3cb60-148">This cmdlet gets device backups for policy that this parameter specifies.</span></span>

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

### <span data-ttu-id="3cb60-149">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="3cb60-149">-DeviceName</span></span>
<span data-ttu-id="3cb60-150">Anger namnet på den StorSimple-enhet som du vill säkerhetskopiera.</span><span class="sxs-lookup"><span data-stu-id="3cb60-150">Specifies the name of the StorSimple device for which to get backups.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-151">-Först</span><span class="sxs-lookup"><span data-stu-id="3cb60-151">-First</span></span>
<span data-ttu-id="3cb60-152">Hämtar bara angivet antal objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-152">Gets only the specified number of objects.</span></span>
<span data-ttu-id="3cb60-153">Ange antalet objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="3cb60-153">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-154">-Från</span><span class="sxs-lookup"><span data-stu-id="3cb60-154">-From</span></span>
<span data-ttu-id="3cb60-155">Anger start datum och-tid för de säkerhets kopior som ska hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-155">Specifies the start date and time for the backups that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-156">-Profil</span><span class="sxs-lookup"><span data-stu-id="3cb60-156">-Profile</span></span>
<span data-ttu-id="3cb60-157">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="3cb60-157">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3cb60-158">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="3cb60-158">-Skip</span></span>
<span data-ttu-id="3cb60-159">Ignorerar angivet antal objekt och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-159">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="3cb60-160">Ange antalet objekt som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="3cb60-160">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-161">-För att</span><span class="sxs-lookup"><span data-stu-id="3cb60-161">-To</span></span>
<span data-ttu-id="3cb60-162">Anger slutdatum och-tid för de säkerhets kopior som ska hämtas av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb60-162">Specifies the end date and time for the backups that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-163">-Volym</span><span class="sxs-lookup"><span data-stu-id="3cb60-163">-Volume</span></span>
<span data-ttu-id="3cb60-164">Anger ett **VirtualDisk** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-164">Specifies a **VirtualDisk** object.</span></span>
<span data-ttu-id="3cb60-165">Denna cmdlet använder **InstanceID** för detta objekt för att avgöra vilken volym säkerhets kopior finns på.</span><span class="sxs-lookup"><span data-stu-id="3cb60-165">This cmdlet uses the **InstanceId** of this object to determine the volume in which backups exist.</span></span>
<span data-ttu-id="3cb60-166">Använd parametern **Get-AzureStorSimpleDeviceVolume** för att hämta ett **VirtualDisk** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-166">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolume** parameter.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-167">-VolumeId</span><span class="sxs-lookup"><span data-stu-id="3cb60-167">-VolumeId</span></span>
<span data-ttu-id="3cb60-168">Anger instans-ID för volymen som säkerhets kopior finns på.</span><span class="sxs-lookup"><span data-stu-id="3cb60-168">Specifies the instance ID of the volume in which backups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb60-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb60-169">CommonParameters</span></span>
<span data-ttu-id="3cb60-170">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb60-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb60-171">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb60-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb60-172">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cb60-172">INPUTS</span></span>

### <span data-ttu-id="3cb60-173">BackupPolicyDetails, VirtualDisk</span><span class="sxs-lookup"><span data-stu-id="3cb60-173">BackupPolicyDetails, VirtualDisk</span></span>
<span data-ttu-id="3cb60-174">Denna cmdlet accepterar **BackupPolicyDetails** -och **VirtualDisk** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-174">This cmdlet accepts **BackupPolicyDetails** and **VirtualDisk** objects.</span></span>

## <span data-ttu-id="3cb60-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cb60-175">OUTPUTS</span></span>

### <span data-ttu-id="3cb60-176">IList\<Backup\></span><span class="sxs-lookup"><span data-stu-id="3cb60-176">IList\<Backup\></span></span>
<span data-ttu-id="3cb60-177">Denna cmdlet returnerar en lista över **säkerhets kopie** objekt.</span><span class="sxs-lookup"><span data-stu-id="3cb60-177">This cmdlet returns a list of **Backup** objects.</span></span>

## <span data-ttu-id="3cb60-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cb60-178">NOTES</span></span>

## <span data-ttu-id="3cb60-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cb60-179">RELATED LINKS</span></span>

[<span data-ttu-id="3cb60-180">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="3cb60-180">Remove-AzureStorSimpleDeviceBackup</span></span>](./Remove-AzureStorSimpleDeviceBackup.md)

[<span data-ttu-id="3cb60-181">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="3cb60-181">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="3cb60-182">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="3cb60-182">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)


