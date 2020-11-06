---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 271426278c561ede4778e0ad69cf9ee4e6c0607e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572275"
---
# <span data-ttu-id="5a651-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a651-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="5a651-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a651-102">SYNOPSIS</span></span>
<span data-ttu-id="5a651-103">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="5a651-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="5a651-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a651-104">SYNTAX</span></span>

### <span data-ttu-id="5a651-105">Uppdatering (standard)</span><span class="sxs-lookup"><span data-stu-id="5a651-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a651-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a651-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a651-107">ID</span><span class="sxs-lookup"><span data-stu-id="5a651-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a651-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a651-108">DESCRIPTION</span></span>
<span data-ttu-id="5a651-109">Ange konfigurationen för säkerhets kopiering på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="5a651-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="5a651-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a651-110">EXAMPLES</span></span>

### <span data-ttu-id="5a651-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a651-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="5a651-112">Ange konfiguration för säkerhets kopiering av Azure-Stack.</span><span class="sxs-lookup"><span data-stu-id="5a651-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="5a651-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a651-113">PARAMETERS</span></span>

### <span data-ttu-id="5a651-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a651-114">-AsJob</span></span>
<span data-ttu-id="5a651-115">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="5a651-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5a651-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="5a651-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="5a651-117">Intervallet i timmar, under den frekvens som Schemaläggaren tar en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="5a651-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="5a651-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5a651-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="5a651-119">Logg period, i dagar, för säkerhets kopior på lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="5a651-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="5a651-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5a651-120">-EncryptionKey</span></span>
<span data-ttu-id="5a651-121">Krypterings nycklar som används för att kryptera säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="5a651-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="5a651-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a651-122">-InputObject</span></span>
<span data-ttu-id="5a651-123">Plats konfiguration för säkerhets kopian returnerades av Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a651-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="5a651-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="5a651-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="5a651-125">Om Schemaläggaren för säkerhets kopior ska vara aktive rad.</span><span class="sxs-lookup"><span data-stu-id="5a651-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="5a651-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a651-126">-Location</span></span>
<span data-ttu-id="5a651-127">Plats att konfigurera.</span><span class="sxs-lookup"><span data-stu-id="5a651-127">Location to configure.</span></span>

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

### <span data-ttu-id="5a651-128">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="5a651-128">-Password</span></span>
<span data-ttu-id="5a651-129">Lösen ord krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="5a651-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="5a651-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5a651-130">-Path</span></span>
<span data-ttu-id="5a651-131">Plats där säkerhets kopior ska sparas.</span><span class="sxs-lookup"><span data-stu-id="5a651-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="5a651-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a651-132">-ResourceGroupName</span></span>
<span data-ttu-id="5a651-133">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a651-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="5a651-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a651-134">-ResourceId</span></span>
<span data-ttu-id="5a651-135">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5a651-135">The resource id.</span></span>

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

### <span data-ttu-id="5a651-136">-Username</span><span class="sxs-lookup"><span data-stu-id="5a651-136">-Username</span></span>
<span data-ttu-id="5a651-137">Username krävs för att komma åt plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="5a651-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="5a651-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a651-138">-Confirm</span></span>
<span data-ttu-id="5a651-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a651-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a651-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a651-140">-WhatIf</span></span>
<span data-ttu-id="5a651-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a651-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a651-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a651-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a651-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a651-143">CommonParameters</span></span>
<span data-ttu-id="5a651-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a651-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a651-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a651-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a651-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a651-146">INPUTS</span></span>

## <span data-ttu-id="5a651-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a651-147">OUTPUTS</span></span>

### <span data-ttu-id="5a651-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="5a651-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="5a651-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a651-149">NOTES</span></span>

## <span data-ttu-id="5a651-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a651-150">RELATED LINKS</span></span>

