---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758128"
---
# <span data-ttu-id="e7bf5-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf5-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="e7bf5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="e7bf5-103">Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7bf5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7bf5-104">SYNTAX</span></span>

### <span data-ttu-id="e7bf5-105">StorageUriSqlServerAutoBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="e7bf5-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7bf5-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="e7bf5-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7bf5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="e7bf5-108">Cmdleten **New-AzureVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="e7bf5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="e7bf5-110">Exempel 1: skapa en automatisk säkerhets kopierings konfiguration med lagrings-URI och konto nycklar</span><span class="sxs-lookup"><span data-stu-id="e7bf5-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e7bf5-111">Det här kommandot skapar ett automatiskt konfigurations objekt för säkerhets kopior genom att ange lagrings-URI och konto nycklar.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="e7bf5-112">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="e7bf5-113">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e7bf5-114">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzureRmVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="e7bf5-115">Exempel 2: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext</span><span class="sxs-lookup"><span data-stu-id="e7bf5-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="e7bf5-116">Det första kommandot skapar en lagrings kontext och lagrar den sedan i $StorageContext variabel.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="e7bf5-117">Mer information finns i New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="e7bf5-118">Det andra kommandot skapar ett automatiskt konfigurations objekt genom att ange lagrings kontexten i $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="e7bf5-119">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="e7bf5-120">Exempel 3: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext med kryptering och lösen ord</span><span class="sxs-lookup"><span data-stu-id="e7bf5-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="e7bf5-121">Det här kommandot skapar och lagrar ett automatiskt konfigurations objekt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="e7bf5-122">Kommandot anger den lagrings kontext som skapades i ett tidigare exempel.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="e7bf5-123">Kommandot aktiverar kryptering med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-123">The command enables encryption with password.</span></span>
<span data-ttu-id="e7bf5-124">Lösen ordet har sparats som en säker sträng i $CertificatePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="e7bf5-125">Om du vill skapa en skyddad sträng använder du ConvertTo-SecureString cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="e7bf5-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7bf5-126">PARAMETERS</span></span>

### <span data-ttu-id="e7bf5-127">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="e7bf5-127">-Enable</span></span>
<span data-ttu-id="e7bf5-128">Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="e7bf5-129">Om du anger den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="e7bf5-130">Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="e7bf5-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="e7bf5-132">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="e7bf5-133">-EnableEncryption</span></span>
<span data-ttu-id="e7bf5-134">Anger att denna cmdlet aktiverar kryptering.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e7bf5-135">-CertificatePassword</span></span>
<span data-ttu-id="e7bf5-136">Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="e7bf5-137">-StorageUri</span></span>
<span data-ttu-id="e7bf5-138">Anger URI (Uniform Resource Identifier) för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="e7bf5-139">-StorageKey</span></span>
<span data-ttu-id="e7bf5-140">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7bf5-141">-Profile</span></span>
<span data-ttu-id="e7bf5-142">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e7bf5-143">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7bf5-144">-InformationAction</span></span>
<span data-ttu-id="e7bf5-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="e7bf5-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7bf5-146">-InformationVariable</span></span>
<span data-ttu-id="e7bf5-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="e7bf5-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="e7bf5-148">-StorageContext</span></span>
<span data-ttu-id="e7bf5-149">Anger det lagrings konto som ska användas för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="e7bf5-150">Använd New-AzureStorageContext cmdlet för att få ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="e7bf5-151">Standardvärdet är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="e7bf5-152">-BackupScheduleType</span></span>
<span data-ttu-id="e7bf5-153">Schema typ för säkerhets kopiering, manuell eller automatisk</span><span class="sxs-lookup"><span data-stu-id="e7bf5-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="e7bf5-154">-BackupSystemDbs</span></span>
<span data-ttu-id="e7bf5-155">Säkerhetskopiera system databaser</span><span class="sxs-lookup"><span data-stu-id="e7bf5-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="e7bf5-156">-FullBackupFrequency</span></span>
<span data-ttu-id="e7bf5-157">Frekvens för fullständig säkerhets kopiering av SQL Server, dag eller vecka</span><span class="sxs-lookup"><span data-stu-id="e7bf5-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="e7bf5-158">-FullBackupStartHour</span></span>
<span data-ttu-id="e7bf5-159">Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar</span><span class="sxs-lookup"><span data-stu-id="e7bf5-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="e7bf5-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="e7bf5-161">Fönstret full säkerhets kopiering i timmar i SQL Server</span><span class="sxs-lookup"><span data-stu-id="e7bf5-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7bf5-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="e7bf5-163">Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter</span><span class="sxs-lookup"><span data-stu-id="e7bf5-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7bf5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7bf5-164">CommonParameters</span></span>
<span data-ttu-id="e7bf5-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7bf5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7bf5-166">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7bf5-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7bf5-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7bf5-167">INPUTS</span></span>

## <span data-ttu-id="e7bf5-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7bf5-168">OUTPUTS</span></span>

## <span data-ttu-id="e7bf5-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7bf5-169">NOTES</span></span>

## <span data-ttu-id="e7bf5-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7bf5-170">RELATED LINKS</span></span>

[<span data-ttu-id="e7bf5-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e7bf5-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="e7bf5-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e7bf5-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


