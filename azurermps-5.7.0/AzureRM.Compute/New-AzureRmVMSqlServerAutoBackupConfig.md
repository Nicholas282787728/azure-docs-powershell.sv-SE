---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573535"
---
# <span data-ttu-id="4195e-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="4195e-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="4195e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4195e-102">SYNOPSIS</span></span>
<span data-ttu-id="4195e-103">Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4195e-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4195e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4195e-104">SYNTAX</span></span>

### <span data-ttu-id="4195e-105">StorageUriSqlServerAutoBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="4195e-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4195e-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="4195e-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4195e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4195e-107">DESCRIPTION</span></span>
<span data-ttu-id="4195e-108">Cmdleten **New-AzureVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4195e-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="4195e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4195e-109">EXAMPLES</span></span>

### <span data-ttu-id="4195e-110">Exempel 1: skapa en automatisk säkerhets kopierings konfiguration med lagrings-URI och konto nycklar</span><span class="sxs-lookup"><span data-stu-id="4195e-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="4195e-111">Det här kommandot skapar ett automatiskt konfigurations objekt för säkerhets kopior genom att ange lagrings-URI och konto nycklar.</span><span class="sxs-lookup"><span data-stu-id="4195e-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="4195e-112">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="4195e-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="4195e-113">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="4195e-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="4195e-114">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzureRmVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4195e-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="4195e-115">Exempel 2: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext</span><span class="sxs-lookup"><span data-stu-id="4195e-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="4195e-116">Det första kommandot skapar en lagrings kontext och lagrar den sedan i $StorageContext variabel.</span><span class="sxs-lookup"><span data-stu-id="4195e-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="4195e-117">Mer information finns i New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4195e-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="4195e-118">Det andra kommandot skapar ett automatiskt konfigurations objekt genom att ange lagrings kontexten i $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="4195e-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="4195e-119">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="4195e-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="4195e-120">Exempel 3: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext med kryptering och lösen ord</span><span class="sxs-lookup"><span data-stu-id="4195e-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="4195e-121">Det här kommandot skapar och lagrar ett automatiskt konfigurations objekt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="4195e-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="4195e-122">Kommandot anger den lagrings kontext som skapades i ett tidigare exempel.</span><span class="sxs-lookup"><span data-stu-id="4195e-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="4195e-123">Kommandot aktiverar kryptering med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="4195e-123">The command enables encryption with password.</span></span>
<span data-ttu-id="4195e-124">Lösen ordet har sparats som en säker sträng i $CertificatePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="4195e-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="4195e-125">Om du vill skapa en skyddad sträng använder du ConvertTo-SecureString cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4195e-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="4195e-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4195e-126">PARAMETERS</span></span>

### <span data-ttu-id="4195e-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="4195e-127">-BackupScheduleType</span></span>
<span data-ttu-id="4195e-128">Schema typ för säkerhets kopiering, manuell eller automatisk</span><span class="sxs-lookup"><span data-stu-id="4195e-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="4195e-129">-BackupSystemDbs</span></span>
<span data-ttu-id="4195e-130">Säkerhetskopiera system databaser</span><span class="sxs-lookup"><span data-stu-id="4195e-130">Backup system databases</span></span>

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

### <span data-ttu-id="4195e-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4195e-131">-CertificatePassword</span></span>
<span data-ttu-id="4195e-132">Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="4195e-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-133">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="4195e-133">-Enable</span></span>
<span data-ttu-id="4195e-134">Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4195e-134">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="4195e-135">Om du anger den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.</span><span class="sxs-lookup"><span data-stu-id="4195e-135">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="4195e-136">Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.</span><span class="sxs-lookup"><span data-stu-id="4195e-136">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-137">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="4195e-137">-EnableEncryption</span></span>
<span data-ttu-id="4195e-138">Anger att denna cmdlet aktiverar kryptering.</span><span class="sxs-lookup"><span data-stu-id="4195e-138">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-139">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="4195e-139">-FullBackupFrequency</span></span>
<span data-ttu-id="4195e-140">Frekvens för fullständig säkerhets kopiering av SQL Server, varje dag eller varje vecka</span><span class="sxs-lookup"><span data-stu-id="4195e-140">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-141">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="4195e-141">-FullBackupStartHour</span></span>
<span data-ttu-id="4195e-142">Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar</span><span class="sxs-lookup"><span data-stu-id="4195e-142">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="4195e-143">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="4195e-143">-FullBackupWindowInHours</span></span>
<span data-ttu-id="4195e-144">Fönstret full säkerhets kopiering i timmar i SQL Server</span><span class="sxs-lookup"><span data-stu-id="4195e-144">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="4195e-145">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="4195e-145">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="4195e-146">Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter</span><span class="sxs-lookup"><span data-stu-id="4195e-146">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="4195e-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4195e-147">-ResourceGroupName</span></span>
<span data-ttu-id="4195e-148">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4195e-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-149">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="4195e-149">-RetentionPeriodInDays</span></span>
<span data-ttu-id="4195e-150">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="4195e-150">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-151">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4195e-151">-StorageContext</span></span>
<span data-ttu-id="4195e-152">Anger det lagrings konto som ska användas för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="4195e-152">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="4195e-153">Använd New-AzureStorageContext cmdlet för att få ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4195e-153">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="4195e-154">Standardvärdet är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.</span><span class="sxs-lookup"><span data-stu-id="4195e-154">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4195e-155">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="4195e-155">-StorageKey</span></span>
<span data-ttu-id="4195e-156">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="4195e-156">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="4195e-157">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="4195e-157">-StorageUri</span></span>
<span data-ttu-id="4195e-158">Anger URI (Uniform Resource Identifier) för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="4195e-158">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="4195e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4195e-159">CommonParameters</span></span>
<span data-ttu-id="4195e-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4195e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4195e-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4195e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4195e-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4195e-162">INPUTS</span></span>

### <span data-ttu-id="4195e-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="4195e-163">None</span></span>
<span data-ttu-id="4195e-164">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4195e-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4195e-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4195e-165">OUTPUTS</span></span>

## <span data-ttu-id="4195e-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4195e-166">NOTES</span></span>

## <span data-ttu-id="4195e-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4195e-167">RELATED LINKS</span></span>

[<span data-ttu-id="4195e-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="4195e-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="4195e-169">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="4195e-169">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


