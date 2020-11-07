---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93921291"
---
# <span data-ttu-id="a4608-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4608-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="a4608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4608-102">SYNOPSIS</span></span>
<span data-ttu-id="a4608-103">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="a4608-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="a4608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4608-104">SYNTAX</span></span>

### <span data-ttu-id="a4608-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="a4608-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4608-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4608-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4608-107">ID</span><span class="sxs-lookup"><span data-stu-id="a4608-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4608-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4608-108">DESCRIPTION</span></span>
<span data-ttu-id="a4608-109">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="a4608-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="a4608-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4608-110">EXAMPLES</span></span>

### <span data-ttu-id="a4608-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a4608-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="a4608-112">Ange konfiguration för säkerhets kopiering av Azure-Stack.</span><span class="sxs-lookup"><span data-stu-id="a4608-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="a4608-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4608-113">PARAMETERS</span></span>

### <span data-ttu-id="a4608-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4608-114">-AsJob</span></span>
<span data-ttu-id="a4608-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="a4608-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="a4608-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a4608-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="a4608-117">Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="a4608-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="a4608-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a4608-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="a4608-119">Logg period, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="a4608-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="a4608-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a4608-120">-EncryptionKey</span></span>
<span data-ttu-id="a4608-121">Krypterings nycklar som används för att kryptera säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="a4608-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="a4608-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4608-122">-InputObject</span></span>
<span data-ttu-id="a4608-123">Plats konfiguration för säkerhets kopian returnerades av Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4608-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="a4608-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="a4608-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="a4608-125">Om Schemaläggaren för säkerhets kopior ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="a4608-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="a4608-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="a4608-126">-Location</span></span>
<span data-ttu-id="a4608-127">Plats att konfigurera.</span><span class="sxs-lookup"><span data-stu-id="a4608-127">Location to configure.</span></span>

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

### <span data-ttu-id="a4608-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="a4608-128">-Password</span></span>
<span data-ttu-id="a4608-129">Lösen ord krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="a4608-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="a4608-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a4608-130">-Path</span></span>
<span data-ttu-id="a4608-131">Plats där säkerhets kopior ska sparas.</span><span class="sxs-lookup"><span data-stu-id="a4608-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="a4608-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4608-132">-ResourceGroupName</span></span>
<span data-ttu-id="a4608-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4608-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="a4608-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4608-134">-ResourceId</span></span>
<span data-ttu-id="a4608-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a4608-135">The resource id.</span></span>

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

### <span data-ttu-id="a4608-136">-Username</span><span class="sxs-lookup"><span data-stu-id="a4608-136">-Username</span></span>
<span data-ttu-id="a4608-137">Username krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="a4608-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="a4608-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4608-138">-Confirm</span></span>
<span data-ttu-id="a4608-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4608-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4608-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4608-140">-WhatIf</span></span>
<span data-ttu-id="a4608-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4608-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4608-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4608-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4608-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4608-143">CommonParameters</span></span>
<span data-ttu-id="a4608-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4608-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4608-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4608-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4608-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4608-146">INPUTS</span></span>

## <span data-ttu-id="a4608-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4608-147">OUTPUTS</span></span>

### <span data-ttu-id="a4608-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="a4608-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="a4608-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4608-149">NOTES</span></span>

## <span data-ttu-id="a4608-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4608-150">RELATED LINKS</span></span>

