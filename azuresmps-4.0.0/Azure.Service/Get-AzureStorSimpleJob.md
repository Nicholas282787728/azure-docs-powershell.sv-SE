---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093284"
---
# <span data-ttu-id="4d187-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="4d187-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="4d187-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d187-102">SYNOPSIS</span></span>
<span data-ttu-id="4d187-103">Hämtar StorSimple-jobb.</span><span class="sxs-lookup"><span data-stu-id="4d187-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="4d187-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d187-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d187-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d187-105">DESCRIPTION</span></span>
<span data-ttu-id="4d187-106">Cmdleten **Get-AzureStorSimpleJob** får Azure StorSimple-jobb.</span><span class="sxs-lookup"><span data-stu-id="4d187-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="4d187-107">Ange ett instans-ID för att hämta ett specifikt jobb.</span><span class="sxs-lookup"><span data-stu-id="4d187-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="4d187-108">Ange andra parametrar för att begränsa vilka jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="4d187-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="4d187-109">Denna cmdlet returnerar maximalt 200-jobb.</span><span class="sxs-lookup"><span data-stu-id="4d187-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="4d187-110">Om det finns fler än 200 jobb kan du hämta de återstående utskrifterna med hjälp av parametrarna *First* och *Skip* .</span><span class="sxs-lookup"><span data-stu-id="4d187-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="4d187-111">Om du anger ett värde på 100 för *Skip* och 50 för *First* returnerar denna cmdlet inte de första 100-resultaten.</span><span class="sxs-lookup"><span data-stu-id="4d187-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="4d187-112">Den returnerar nästföljande 50-resultat efter 100.</span><span class="sxs-lookup"><span data-stu-id="4d187-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="4d187-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d187-113">EXAMPLES</span></span>

### <span data-ttu-id="4d187-114">Exempel 1: Hämta ett jobb genom att använda ett ID</span><span class="sxs-lookup"><span data-stu-id="4d187-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="4d187-115">Med det här kommandot får du information om det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="4d187-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="4d187-116">Exempel 2: Hämta jobb genom att använda ett enhets namn</span><span class="sxs-lookup"><span data-stu-id="4d187-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="4d187-117">Med det här kommandot får du information om jobben för enheten som heter 8600-Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="4d187-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="4d187-118">Kommandot får de två första jobben för enheten.</span><span class="sxs-lookup"><span data-stu-id="4d187-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="4d187-119">Exempel 3: Hämta färdiga jobb</span><span class="sxs-lookup"><span data-stu-id="4d187-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="4d187-120">Det här kommandot får färdiga jobb.</span><span class="sxs-lookup"><span data-stu-id="4d187-120">This command gets completed jobs.</span></span>
<span data-ttu-id="4d187-121">Kommandot får bara de två första jobben när de hoppat över de tio första jobben.</span><span class="sxs-lookup"><span data-stu-id="4d187-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="4d187-122">Exempel 4: Hämta manuella säkerhets kopierings jobb</span><span class="sxs-lookup"><span data-stu-id="4d187-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="4d187-123">Det här kommandot hämtar utskrifts typen manuell säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="4d187-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="4d187-124">Exempel 5: Hämta jobb mellan angivna tider</span><span class="sxs-lookup"><span data-stu-id="4d187-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="4d187-125">De två första kommandona skapar **datetime** -objekt med hjälp av Get-Date cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d187-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="4d187-126">I kommandona lagras de nya tiderna i $StartTime och $EndTime variabler.</span><span class="sxs-lookup"><span data-stu-id="4d187-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="4d187-127">Om du vill ha mer information skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4d187-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="4d187-128">Med kommandot slut hämtas jobb för enheten som heter Device07 mellan tiderna som lagras i $StartTime och $EndTime.</span><span class="sxs-lookup"><span data-stu-id="4d187-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="4d187-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d187-129">PARAMETERS</span></span>

### <span data-ttu-id="4d187-130">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="4d187-130">-DeviceName</span></span>
<span data-ttu-id="4d187-131">Anger namnet på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="4d187-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="4d187-132">-Först</span><span class="sxs-lookup"><span data-stu-id="4d187-132">-First</span></span>
<span data-ttu-id="4d187-133">Hämtar bara angivet antal objekt.</span><span class="sxs-lookup"><span data-stu-id="4d187-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="4d187-134">Ange antalet objekt som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4d187-134">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="4d187-135">-Från</span><span class="sxs-lookup"><span data-stu-id="4d187-135">-From</span></span>
<span data-ttu-id="4d187-136">Anger start datum och-tid för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="4d187-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d187-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4d187-137">-InstanceId</span></span>
<span data-ttu-id="4d187-138">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="4d187-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="4d187-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="4d187-139">-Profile</span></span>
<span data-ttu-id="4d187-140">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4d187-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d187-141">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4d187-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d187-142">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="4d187-142">-Skip</span></span>
<span data-ttu-id="4d187-143">Ignorerar angivet antal objekt och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="4d187-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="4d187-144">Ange antalet objekt som ska hoppas över.</span><span class="sxs-lookup"><span data-stu-id="4d187-144">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="4d187-145">-Status</span><span class="sxs-lookup"><span data-stu-id="4d187-145">-Status</span></span>
<span data-ttu-id="4d187-146">Anger status.</span><span class="sxs-lookup"><span data-stu-id="4d187-146">Specifies the status.</span></span>
<span data-ttu-id="4d187-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4d187-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d187-148">Aktiv</span><span class="sxs-lookup"><span data-stu-id="4d187-148">Running</span></span>
- <span data-ttu-id="4d187-149">Rätta</span><span class="sxs-lookup"><span data-stu-id="4d187-149">Completed</span></span>
- <span data-ttu-id="4d187-150">Annullerats</span><span class="sxs-lookup"><span data-stu-id="4d187-150">Cancelled</span></span>
- <span data-ttu-id="4d187-151">Startade</span><span class="sxs-lookup"><span data-stu-id="4d187-151">Failed</span></span>
- <span data-ttu-id="4d187-152">Avbryta</span><span class="sxs-lookup"><span data-stu-id="4d187-152">Canceling</span></span>
- <span data-ttu-id="4d187-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="4d187-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="4d187-154">-För att</span><span class="sxs-lookup"><span data-stu-id="4d187-154">-To</span></span>
<span data-ttu-id="4d187-155">Anger slutdatum och slut tid för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="4d187-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d187-156">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4d187-156">-Type</span></span>
<span data-ttu-id="4d187-157">Anger jobb typen.</span><span class="sxs-lookup"><span data-stu-id="4d187-157">Specifies the job type.</span></span>
<span data-ttu-id="4d187-158">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4d187-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d187-159">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="4d187-159">Backup</span></span>
- <span data-ttu-id="4d187-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="4d187-160">ManualBackup</span></span>
- <span data-ttu-id="4d187-161">Terställa</span><span class="sxs-lookup"><span data-stu-id="4d187-161">Restore</span></span>
- <span data-ttu-id="4d187-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="4d187-162">CloneWorkflow</span></span>
- <span data-ttu-id="4d187-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="4d187-163">DeviceRestore</span></span>
- <span data-ttu-id="4d187-164">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="4d187-164">Update</span></span>
- <span data-ttu-id="4d187-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="4d187-165">SupportPackage</span></span>
- <span data-ttu-id="4d187-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="4d187-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="4d187-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d187-167">CommonParameters</span></span>
<span data-ttu-id="4d187-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d187-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d187-169">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d187-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d187-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d187-170">INPUTS</span></span>

### <span data-ttu-id="4d187-171">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d187-171">None</span></span>
<span data-ttu-id="4d187-172">Det går inte att pipe in i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d187-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="4d187-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d187-173">OUTPUTS</span></span>

### <span data-ttu-id="4d187-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="4d187-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="4d187-175">Denna cmdlet returnerar en lista med jobb informations objekt, eller om du anger *InstanceID* -parametern, returnerar den ett enskilt jobb informations objekt.</span><span class="sxs-lookup"><span data-stu-id="4d187-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="4d187-176">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d187-176">NOTES</span></span>

## <span data-ttu-id="4d187-177">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d187-177">RELATED LINKS</span></span>

[<span data-ttu-id="4d187-178">Stopp-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="4d187-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


