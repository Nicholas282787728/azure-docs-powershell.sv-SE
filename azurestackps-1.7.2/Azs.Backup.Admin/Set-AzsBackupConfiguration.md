---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921238"
---
# <span data-ttu-id="4bf5c-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bf5c-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="4bf5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf5c-103">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="4bf5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bf5c-104">SYNTAX</span></span>

### <span data-ttu-id="4bf5c-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="4bf5c-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf5c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4bf5c-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bf5c-107">ID</span><span class="sxs-lookup"><span data-stu-id="4bf5c-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bf5c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bf5c-108">DESCRIPTION</span></span>
<span data-ttu-id="4bf5c-109">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="4bf5c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bf5c-110">EXAMPLES</span></span>

### <span data-ttu-id="4bf5c-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="4bf5c-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="4bf5c-112">Ange konfiguration för säkerhets kopiering av Azure-Stack.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="4bf5c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bf5c-113">PARAMETERS</span></span>

### <span data-ttu-id="4bf5c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bf5c-114">-AsJob</span></span>
<span data-ttu-id="4bf5c-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="4bf5c-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="4bf5c-117">Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4bf5c-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="4bf5c-119">Logg period, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="4bf5c-120">-EncryptionCertPath</span></span>
<span data-ttu-id="4bf5c-121">Sökväg till krypterings certifikat filen med offentlig nyckel (. cer).</span><span class="sxs-lookup"><span data-stu-id="4bf5c-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bf5c-122">-InputObject</span></span>
<span data-ttu-id="4bf5c-123">Plats konfiguration för säkerhets kopian returnerades av Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="4bf5c-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="4bf5c-125">Om Schemaläggaren för säkerhets kopior ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="4bf5c-126">-Location</span></span>
<span data-ttu-id="4bf5c-127">Plats att konfigurera.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="4bf5c-128">-Password</span></span>
<span data-ttu-id="4bf5c-129">Lösen ord krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-130">-Path</span><span class="sxs-lookup"><span data-stu-id="4bf5c-130">-Path</span></span>
<span data-ttu-id="4bf5c-131">Plats där säkerhets kopior ska sparas.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf5c-132">-ResourceGroupName</span></span>
<span data-ttu-id="4bf5c-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bf5c-134">-ResourceId</span></span>
<span data-ttu-id="4bf5c-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-136">-Username</span><span class="sxs-lookup"><span data-stu-id="4bf5c-136">-Username</span></span>
<span data-ttu-id="4bf5c-137">Username krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf5c-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bf5c-138">-Confirm</span></span>
<span data-ttu-id="4bf5c-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bf5c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf5c-140">-WhatIf</span></span>
<span data-ttu-id="4bf5c-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf5c-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bf5c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf5c-143">CommonParameters</span></span>
<span data-ttu-id="4bf5c-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf5c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf5c-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf5c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf5c-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bf5c-146">INPUTS</span></span>

## <span data-ttu-id="4bf5c-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bf5c-147">OUTPUTS</span></span>

### <span data-ttu-id="4bf5c-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="4bf5c-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="4bf5c-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bf5c-149">NOTES</span></span>

## <span data-ttu-id="4bf5c-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bf5c-150">RELATED LINKS</span></span>
