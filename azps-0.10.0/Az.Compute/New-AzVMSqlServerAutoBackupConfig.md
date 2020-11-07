---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 1ff53a29fa26ebe7ac78cac5140a9105b43bb27d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925045"
---
# <span data-ttu-id="58b88-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="58b88-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="58b88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58b88-102">SYNOPSIS</span></span>
<span data-ttu-id="58b88-103">Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="58b88-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="58b88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58b88-104">SYNTAX</span></span>

### <span data-ttu-id="58b88-105">StorageUriSqlServerAutoBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="58b88-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58b88-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="58b88-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b88-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58b88-107">DESCRIPTION</span></span>
<span data-ttu-id="58b88-108">Cmdleten **New-AzVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="58b88-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="58b88-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58b88-109">EXAMPLES</span></span>

### <span data-ttu-id="58b88-110">Exempel 1: skapa en automatisk säkerhets kopierings konfiguration med lagrings-URI och konto nycklar</span><span class="sxs-lookup"><span data-stu-id="58b88-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="58b88-111">Det här kommandot skapar ett automatiskt konfigurations objekt för säkerhets kopior genom att ange lagrings-URI och konto nycklar.</span><span class="sxs-lookup"><span data-stu-id="58b88-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="58b88-112">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="58b88-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="58b88-113">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="58b88-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="58b88-114">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58b88-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="58b88-115">Exempel 2: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext</span><span class="sxs-lookup"><span data-stu-id="58b88-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="58b88-116">Det första kommandot skapar en lagrings kontext och lagrar den sedan i $StorageContext variabel.</span><span class="sxs-lookup"><span data-stu-id="58b88-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="58b88-117">Mer information finns i New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="58b88-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="58b88-118">Det andra kommandot skapar ett automatiskt konfigurations objekt genom att ange lagrings kontexten i $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="58b88-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="58b88-119">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="58b88-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="58b88-120">Exempel 3: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext med kryptering och lösen ord</span><span class="sxs-lookup"><span data-stu-id="58b88-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="58b88-121">Det här kommandot skapar och lagrar ett automatiskt konfigurations objekt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="58b88-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="58b88-122">Kommandot anger den lagrings kontext som skapades i ett tidigare exempel.</span><span class="sxs-lookup"><span data-stu-id="58b88-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="58b88-123">Kommandot aktiverar kryptering med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="58b88-123">The command enables encryption with password.</span></span>
<span data-ttu-id="58b88-124">Lösen ordet har sparats som en säker sträng i $CertificatePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="58b88-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="58b88-125">Om du vill skapa en skyddad sträng använder du ConvertTo-SecureString cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58b88-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="58b88-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58b88-126">PARAMETERS</span></span>

### <span data-ttu-id="58b88-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="58b88-127">-BackupScheduleType</span></span>
<span data-ttu-id="58b88-128">Schema typ för säkerhets kopiering, manuell eller automatisk</span><span class="sxs-lookup"><span data-stu-id="58b88-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="58b88-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="58b88-129">-BackupSystemDbs</span></span>
<span data-ttu-id="58b88-130">Säkerhetskopiera system databaser</span><span class="sxs-lookup"><span data-stu-id="58b88-130">Backup system databases</span></span>

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

### <span data-ttu-id="58b88-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="58b88-131">-CertificatePassword</span></span>
<span data-ttu-id="58b88-132">Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="58b88-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="58b88-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b88-133">-DefaultProfile</span></span>
<span data-ttu-id="58b88-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58b88-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58b88-135">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="58b88-135">-Enable</span></span>
<span data-ttu-id="58b88-136">Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="58b88-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="58b88-137">Om du anger den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.</span><span class="sxs-lookup"><span data-stu-id="58b88-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="58b88-138">Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.</span><span class="sxs-lookup"><span data-stu-id="58b88-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="58b88-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="58b88-139">-EnableEncryption</span></span>
<span data-ttu-id="58b88-140">Anger att denna cmdlet aktiverar kryptering.</span><span class="sxs-lookup"><span data-stu-id="58b88-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="58b88-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="58b88-141">-FullBackupFrequency</span></span>
<span data-ttu-id="58b88-142">Frekvens för fullständig säkerhets kopiering av SQL Server, varje dag eller varje vecka</span><span class="sxs-lookup"><span data-stu-id="58b88-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="58b88-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="58b88-143">-FullBackupStartHour</span></span>
<span data-ttu-id="58b88-144">Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar</span><span class="sxs-lookup"><span data-stu-id="58b88-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="58b88-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="58b88-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="58b88-146">Fönstret full säkerhets kopiering i timmar i SQL Server</span><span class="sxs-lookup"><span data-stu-id="58b88-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="58b88-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="58b88-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="58b88-148">Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter</span><span class="sxs-lookup"><span data-stu-id="58b88-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="58b88-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b88-149">-ResourceGroupName</span></span>
<span data-ttu-id="58b88-150">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58b88-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="58b88-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="58b88-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="58b88-152">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="58b88-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="58b88-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="58b88-153">-StorageContext</span></span>
<span data-ttu-id="58b88-154">Anger det lagrings konto som ska användas för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="58b88-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="58b88-155">Använd New-AzureStorageContext cmdlet för att få ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="58b88-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="58b88-156">Standardvärdet är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.</span><span class="sxs-lookup"><span data-stu-id="58b88-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58b88-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="58b88-157">-StorageKey</span></span>
<span data-ttu-id="58b88-158">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="58b88-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="58b88-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="58b88-159">-StorageUri</span></span>
<span data-ttu-id="58b88-160">Anger URI (Uniform Resource Identifier) för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="58b88-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="58b88-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b88-161">CommonParameters</span></span>
<span data-ttu-id="58b88-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b88-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b88-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b88-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b88-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58b88-164">INPUTS</span></span>

### <span data-ttu-id="58b88-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="58b88-165">None</span></span>
<span data-ttu-id="58b88-166">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="58b88-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58b88-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58b88-167">OUTPUTS</span></span>

### <span data-ttu-id="58b88-168">Microsoft. Azure. commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="58b88-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="58b88-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58b88-169">NOTES</span></span>

## <span data-ttu-id="58b88-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58b88-170">RELATED LINKS</span></span>

[<span data-ttu-id="58b88-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="58b88-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="58b88-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="58b88-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


