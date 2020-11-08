---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099429"
---
# <span data-ttu-id="33b22-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="33b22-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="33b22-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33b22-102">SYNOPSIS</span></span>
<span data-ttu-id="33b22-103">Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="33b22-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="33b22-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33b22-104">SYNTAX</span></span>

### <span data-ttu-id="33b22-105">StorageUriSqlServerAutoBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="33b22-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="33b22-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="33b22-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="33b22-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33b22-107">DESCRIPTION</span></span>
<span data-ttu-id="33b22-108">Cmdleten **New-AzureVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="33b22-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="33b22-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33b22-109">EXAMPLES</span></span>

### <span data-ttu-id="33b22-110">Exempel 1: skapa en konfiguration för automatisk säkerhets kopiering med lagrings-URI och konto nycklar</span><span class="sxs-lookup"><span data-stu-id="33b22-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="33b22-111">Det här kommandot skapar ett konfigurations objekt för automatisk säkerhets kopiering genom att ange lagrings-URL och konto.</span><span class="sxs-lookup"><span data-stu-id="33b22-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="33b22-112">Exempel 2: skapa en konfiguration för automatisk säkerhets kopiering med lagrings kontext</span><span class="sxs-lookup"><span data-stu-id="33b22-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="33b22-113">Det här kommandot skapar ett konfigurations objekt för automatisk säkerhets kopiering genom att ange lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="33b22-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="33b22-114">Exempel 3: skapa en konfiguration för automatisk säkerhets kopiering med lagrings kontext med kryptering och lösen ord</span><span class="sxs-lookup"><span data-stu-id="33b22-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="33b22-115">Det här kommandot skapar ett konfigurations objekt för automatisk säkerhets kopiering genom att ange lagrings kontext och aktivera krypterings alternativ med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="33b22-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="33b22-116">Certificatepassword-istn som lagras i variabeln som heter $CertPasswd.</span><span class="sxs-lookup"><span data-stu-id="33b22-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="33b22-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33b22-117">PARAMETERS</span></span>

### <span data-ttu-id="33b22-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="33b22-118">-BackupScheduleType</span></span>
<span data-ttu-id="33b22-119">Schema typ för säkerhets kopiering, manuell eller automatisk</span><span class="sxs-lookup"><span data-stu-id="33b22-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="33b22-120">-BackupSystemDbs</span></span>
<span data-ttu-id="33b22-121">Säkerhetskopiera system databaser</span><span class="sxs-lookup"><span data-stu-id="33b22-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="33b22-122">-CertificatePassword</span></span>
<span data-ttu-id="33b22-123">Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="33b22-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-124">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="33b22-124">-Enable</span></span>
<span data-ttu-id="33b22-125">Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="33b22-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="33b22-126">Om du använder den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.</span><span class="sxs-lookup"><span data-stu-id="33b22-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="33b22-127">Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.</span><span class="sxs-lookup"><span data-stu-id="33b22-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="33b22-128">-EnableEncryption</span></span>
<span data-ttu-id="33b22-129">Anger att kryptering är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="33b22-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="33b22-130">-FullBackupFrequency</span></span>
<span data-ttu-id="33b22-131">Frekvens för fullständig säkerhets kopiering av SQL Server, dag eller vecka</span><span class="sxs-lookup"><span data-stu-id="33b22-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="33b22-132">-FullBackupStartHour</span></span>
<span data-ttu-id="33b22-133">Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar</span><span class="sxs-lookup"><span data-stu-id="33b22-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="33b22-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="33b22-135">Fönstret full säkerhets kopiering i timmar i SQL Server</span><span class="sxs-lookup"><span data-stu-id="33b22-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="33b22-136">-InformationAction</span></span>
<span data-ttu-id="33b22-137">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="33b22-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="33b22-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="33b22-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33b22-139">Vidare</span><span class="sxs-lookup"><span data-stu-id="33b22-139">Continue</span></span>
- <span data-ttu-id="33b22-140">Över</span><span class="sxs-lookup"><span data-stu-id="33b22-140">Ignore</span></span>
- <span data-ttu-id="33b22-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="33b22-141">Inquire</span></span>
- <span data-ttu-id="33b22-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="33b22-142">SilentlyContinue</span></span>
- <span data-ttu-id="33b22-143">Stanna</span><span class="sxs-lookup"><span data-stu-id="33b22-143">Stop</span></span>
- <span data-ttu-id="33b22-144">Avbryt</span><span class="sxs-lookup"><span data-stu-id="33b22-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="33b22-145">-InformationVariable</span></span>
<span data-ttu-id="33b22-146">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="33b22-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="33b22-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="33b22-148">Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter</span><span class="sxs-lookup"><span data-stu-id="33b22-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-149">-Profil</span><span class="sxs-lookup"><span data-stu-id="33b22-149">-Profile</span></span>
<span data-ttu-id="33b22-150">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="33b22-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33b22-151">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="33b22-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33b22-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="33b22-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="33b22-153">Anger längden för tids perioden i dagar.</span><span class="sxs-lookup"><span data-stu-id="33b22-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="33b22-154">-StorageContext</span></span>
<span data-ttu-id="33b22-155">Anger det lagrings konto som ska användas för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="33b22-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="33b22-156">Standard är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.</span><span class="sxs-lookup"><span data-stu-id="33b22-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="33b22-157">-StorageKey</span></span>
<span data-ttu-id="33b22-158">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="33b22-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="33b22-159">-StorageUri</span></span>
<span data-ttu-id="33b22-160">Anger en URI till Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="33b22-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b22-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b22-161">CommonParameters</span></span>
<span data-ttu-id="33b22-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b22-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b22-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b22-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b22-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33b22-164">INPUTS</span></span>

## <span data-ttu-id="33b22-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33b22-165">OUTPUTS</span></span>

## <span data-ttu-id="33b22-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33b22-166">NOTES</span></span>

## <span data-ttu-id="33b22-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33b22-167">RELATED LINKS</span></span>

[<span data-ttu-id="33b22-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="33b22-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


