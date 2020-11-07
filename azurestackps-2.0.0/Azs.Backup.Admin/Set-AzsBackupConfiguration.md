---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925474"
---
# <span data-ttu-id="dfd9b-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="dfd9b-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="dfd9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfd9b-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd9b-103">Uppdatera en plats för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-103">Update a backup location.</span></span>

## <span data-ttu-id="dfd9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfd9b-104">SYNTAX</span></span>

### <span data-ttu-id="dfd9b-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="dfd9b-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dfd9b-106">Uppdatera</span><span class="sxs-lookup"><span data-stu-id="dfd9b-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="dfd9b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfd9b-107">DESCRIPTION</span></span>
<span data-ttu-id="dfd9b-108">Uppdatera en plats för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-108">Update a backup location.</span></span>

## <span data-ttu-id="dfd9b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfd9b-109">EXAMPLES</span></span>

### <span data-ttu-id="dfd9b-110">Exempel 1: Ange konfiguration för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="dfd9b-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="dfd9b-111">Ange konfiguration för säkerhets kopiering av Azure-Stack.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="dfd9b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfd9b-112">PARAMETERS</span></span>

### <span data-ttu-id="dfd9b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfd9b-113">-AsJob</span></span>
<span data-ttu-id="dfd9b-114">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="dfd9b-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-115">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="dfd9b-115">-Backup</span></span>
<span data-ttu-id="dfd9b-116">Information om platsen för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-116">Information about the backup location.</span></span>
<span data-ttu-id="dfd9b-117">För att konstruera, se avsnittet anteckningar för säkerhets kopierings egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="dfd9b-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="dfd9b-119">Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="dfd9b-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="dfd9b-121">Logg perioden, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd9b-122">-DefaultProfile</span></span>
<span data-ttu-id="dfd9b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="dfd9b-124">-EncryptionCertPath</span></span>
<span data-ttu-id="dfd9b-125">Sökväg till krypterings certifikat filen med offentlig nyckel (. cer).</span><span class="sxs-lookup"><span data-stu-id="dfd9b-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="dfd9b-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="dfd9b-127">Sant om Schemaläggaren för säkerhets kopiering är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="dfd9b-128">-Location</span></span>
<span data-ttu-id="dfd9b-129">Namn på platsen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="dfd9b-130">-NoWait</span></span>
<span data-ttu-id="dfd9b-131">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="dfd9b-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-132">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="dfd9b-132">-Password</span></span>
<span data-ttu-id="dfd9b-133">Lösen ord för att komma åt platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-134">-Path</span><span class="sxs-lookup"><span data-stu-id="dfd9b-134">-Path</span></span>
<span data-ttu-id="dfd9b-135">Sökvägen till uppdaterings platsen</span><span class="sxs-lookup"><span data-stu-id="dfd9b-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd9b-136">-ResourceGroupName</span></span>
<span data-ttu-id="dfd9b-137">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfd9b-138">-SubscriptionId</span></span>
<span data-ttu-id="dfd9b-139">Autentiseringsuppgifter som unikt identifierar Microsoft Azure-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfd9b-140">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-141">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dfd9b-141">-Tag</span></span>
<span data-ttu-id="dfd9b-142">Lista över värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="dfd9b-143">-UserName</span></span>
<span data-ttu-id="dfd9b-144">Användar namn för att komma åt platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfd9b-145">-Confirm</span></span>
<span data-ttu-id="dfd9b-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd9b-147">-WhatIf</span></span>
<span data-ttu-id="dfd9b-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd9b-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfd9b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd9b-150">CommonParameters</span></span>
<span data-ttu-id="dfd9b-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd9b-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfd9b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd9b-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfd9b-153">INPUTS</span></span>

### <span data-ttu-id="dfd9b-154">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="dfd9b-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="dfd9b-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfd9b-155">OUTPUTS</span></span>

### <span data-ttu-id="dfd9b-156">Microsoft. Azure. PowerShell. cmdletar. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="dfd9b-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="dfd9b-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfd9b-157">NOTES</span></span>

<span data-ttu-id="dfd9b-158">KOMPLEXA PARAMETER egenskaper för att skapa de parametrar som beskrivs nedan skapar du en hash-tabell med lämpliga egenskaper.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfd9b-159">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dfd9b-160">Säkerhetskopiera <IBackupLocation> : information om platsen för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="dfd9b-161">`[Location <String>]`: Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dfd9b-162">`[Tag <IResourceTags>]`: Lista med värde par för nycklar.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="dfd9b-163">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dfd9b-164">`[BackupFrequencyInHours <Int32?>]`: Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="dfd9b-165">`[BackupRetentionPeriodInDays <Int32?>]`: Logg perioden, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="dfd9b-166">`[EncryptionCertBase64 <String>]`: Base64 RAW-data för säkerhets kopierings krypterings certifikatet.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="dfd9b-167">`[IsBackupSchedulerEnabled <Boolean?>]`: Sant om Schemaläggaren för säkerhets kopiering är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="dfd9b-168">`[Password <String>]`: Lösen ord för att komma åt platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="dfd9b-169">`[Path <String>]`: Sökväg till uppdaterings platsen</span><span class="sxs-lookup"><span data-stu-id="dfd9b-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="dfd9b-170">`[UserName <String>]`: Username för att komma åt platsen.</span><span class="sxs-lookup"><span data-stu-id="dfd9b-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="dfd9b-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfd9b-171">RELATED LINKS</span></span>

