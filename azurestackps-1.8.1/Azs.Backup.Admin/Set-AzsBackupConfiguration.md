---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921880"
---
# <span data-ttu-id="03849-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="03849-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="03849-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03849-102">SYNOPSIS</span></span>
<span data-ttu-id="03849-103">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="03849-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="03849-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03849-104">SYNTAX</span></span>

### <span data-ttu-id="03849-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="03849-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03849-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="03849-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03849-107">ID</span><span class="sxs-lookup"><span data-stu-id="03849-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03849-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03849-108">DESCRIPTION</span></span>
<span data-ttu-id="03849-109">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="03849-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="03849-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03849-110">EXAMPLES</span></span>

### <span data-ttu-id="03849-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03849-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="03849-112">Ange konfiguration för säkerhets kopiering av Azure-Stack.</span><span class="sxs-lookup"><span data-stu-id="03849-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="03849-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03849-113">PARAMETERS</span></span>

### <span data-ttu-id="03849-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03849-114">-AsJob</span></span>
<span data-ttu-id="03849-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="03849-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="03849-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="03849-117">Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="03849-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="03849-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="03849-119">Logg period, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="03849-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="03849-120">-EncryptionKey</span></span>
<span data-ttu-id="03849-121">Krypterings nycklar som används för att kryptera säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="03849-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03849-122">-InputObject</span></span>
<span data-ttu-id="03849-123">Plats konfiguration för säkerhets kopian returnerades av Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="03849-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03849-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="03849-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="03849-125">Om Schemaläggaren för säkerhets kopior ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="03849-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="03849-126">-Location</span></span>
<span data-ttu-id="03849-127">Plats att konfigurera.</span><span class="sxs-lookup"><span data-stu-id="03849-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="03849-128">-Password</span></span>
<span data-ttu-id="03849-129">Lösen ord krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="03849-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-130">-Path</span><span class="sxs-lookup"><span data-stu-id="03849-130">-Path</span></span>
<span data-ttu-id="03849-131">Plats där säkerhets kopior ska sparas.</span><span class="sxs-lookup"><span data-stu-id="03849-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03849-132">-ResourceGroupName</span></span>
<span data-ttu-id="03849-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="03849-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03849-134">-ResourceId</span></span>
<span data-ttu-id="03849-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="03849-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03849-136">-Username</span><span class="sxs-lookup"><span data-stu-id="03849-136">-Username</span></span>
<span data-ttu-id="03849-137">Username krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="03849-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="03849-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03849-138">-Confirm</span></span>
<span data-ttu-id="03849-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03849-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03849-140">-WhatIf</span></span>
<span data-ttu-id="03849-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03849-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03849-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03849-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03849-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03849-143">CommonParameters</span></span>
<span data-ttu-id="03849-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03849-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03849-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03849-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03849-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03849-146">INPUTS</span></span>

## <span data-ttu-id="03849-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03849-147">OUTPUTS</span></span>

### <span data-ttu-id="03849-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="03849-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="03849-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03849-149">NOTES</span></span>

## <span data-ttu-id="03849-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03849-150">RELATED LINKS</span></span>

