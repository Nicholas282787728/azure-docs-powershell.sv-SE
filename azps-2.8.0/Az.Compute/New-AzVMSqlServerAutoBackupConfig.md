---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: dbcccaa1c0a17a616d474135be253ebb7ecc0396
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745080"
---
# <span data-ttu-id="20fad-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="20fad-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="20fad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20fad-102">SYNOPSIS</span></span>
<span data-ttu-id="20fad-103">Skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="20fad-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="20fad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20fad-104">SYNTAX</span></span>

### <span data-ttu-id="20fad-105">StorageUriSqlServerAutoBackup (standard)</span><span class="sxs-lookup"><span data-stu-id="20fad-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20fad-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="20fad-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20fad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20fad-107">DESCRIPTION</span></span>
<span data-ttu-id="20fad-108">Cmdleten **New-AzVMSqlServerAutoBackupConfig** skapar ett konfigurations objekt för automatisk säkerhets kopiering av SQL Server.</span><span class="sxs-lookup"><span data-stu-id="20fad-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="20fad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20fad-109">EXAMPLES</span></span>

### <span data-ttu-id="20fad-110">Exempel 1: skapa en automatisk säkerhets kopierings konfiguration med lagrings-URI och konto nycklar</span><span class="sxs-lookup"><span data-stu-id="20fad-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="20fad-111">Det här kommandot skapar ett automatiskt konfigurations objekt för säkerhets kopior genom att ange lagrings-URI och konto nycklar.</span><span class="sxs-lookup"><span data-stu-id="20fad-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="20fad-112">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="20fad-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="20fad-113">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="20fad-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="20fad-114">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20fad-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="20fad-115">Exempel 2: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext</span><span class="sxs-lookup"><span data-stu-id="20fad-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="20fad-116">Det första kommandot skapar en lagrings kontext och lagrar den sedan i $StorageContext variabel.</span><span class="sxs-lookup"><span data-stu-id="20fad-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="20fad-117">Mer information finns i New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="20fad-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="20fad-118">Det andra kommandot skapar ett automatiskt konfigurations objekt genom att ange lagrings kontexten i $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="20fad-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="20fad-119">Automatisk säkerhets kopiering är aktive rad och automatisk säkerhets kopiering sparas i 10 dagar.</span><span class="sxs-lookup"><span data-stu-id="20fad-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="20fad-120">Exempel 3: skapa en automatisk säkerhets kopierings konfiguration med lagrings kontext med kryptering och lösen ord</span><span class="sxs-lookup"><span data-stu-id="20fad-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="20fad-121">Det här kommandot skapar och lagrar ett automatiskt konfigurations objekt för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="20fad-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="20fad-122">Kommandot anger den lagrings kontext som skapades i ett tidigare exempel.</span><span class="sxs-lookup"><span data-stu-id="20fad-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="20fad-123">Kommandot aktiverar kryptering med lösen ord.</span><span class="sxs-lookup"><span data-stu-id="20fad-123">The command enables encryption with password.</span></span>
<span data-ttu-id="20fad-124">Lösen ordet har sparats som en säker sträng i $CertificatePassword variabel.</span><span class="sxs-lookup"><span data-stu-id="20fad-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="20fad-125">Om du vill skapa en skyddad sträng använder du ConvertTo-SecureString cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20fad-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="20fad-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20fad-126">PARAMETERS</span></span>

### <span data-ttu-id="20fad-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="20fad-127">-BackupScheduleType</span></span>
<span data-ttu-id="20fad-128">Schema typ för säkerhets kopiering, manuell eller automatisk</span><span class="sxs-lookup"><span data-stu-id="20fad-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="20fad-129">-BackupSystemDbs</span></span>
<span data-ttu-id="20fad-130">Säkerhetskopiera system databaser</span><span class="sxs-lookup"><span data-stu-id="20fad-130">Backup system databases</span></span>

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

### <span data-ttu-id="20fad-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="20fad-131">-CertificatePassword</span></span>
<span data-ttu-id="20fad-132">Anger ett lösen ord för att kryptera certifikatet som används för att utföra SQL Server-krypterade säkerhets kopieringar.</span><span class="sxs-lookup"><span data-stu-id="20fad-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fad-133">-DefaultProfile</span></span>
<span data-ttu-id="20fad-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20fad-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-135">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="20fad-135">-Enable</span></span>
<span data-ttu-id="20fad-136">Anger att automatisk säkerhets kopiering för den virtuella SQL Server-datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="20fad-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="20fad-137">Om du anger den här parametern ställer automatisk säkerhets kopiering ett schema för säkerhets kopiering för alla befintliga och nya databaser.</span><span class="sxs-lookup"><span data-stu-id="20fad-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="20fad-138">Då uppdateras de hanterade säkerhets kopierings inställningarna efter detta schema.</span><span class="sxs-lookup"><span data-stu-id="20fad-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="20fad-139">-EnableEncryption</span></span>
<span data-ttu-id="20fad-140">Anger att denna cmdlet aktiverar kryptering.</span><span class="sxs-lookup"><span data-stu-id="20fad-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="20fad-141">-FullBackupFrequency</span></span>
<span data-ttu-id="20fad-142">Frekvens för fullständig säkerhets kopiering av SQL Server, varje dag eller varje vecka</span><span class="sxs-lookup"><span data-stu-id="20fad-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="20fad-143">-FullBackupStartHour</span></span>
<span data-ttu-id="20fad-144">Timme på dagen (0-23) när fullständig säkerhets kopiering av SQL Server startar</span><span class="sxs-lookup"><span data-stu-id="20fad-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="20fad-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="20fad-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="20fad-146">Fönstret full säkerhets kopiering i timmar i SQL Server</span><span class="sxs-lookup"><span data-stu-id="20fad-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="20fad-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="20fad-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="20fad-148">Säkerhets kopierings frekvens för SQL Server-loggning, en gång var 1-60 minuter</span><span class="sxs-lookup"><span data-stu-id="20fad-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="20fad-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fad-149">-ResourceGroupName</span></span>
<span data-ttu-id="20fad-150">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="20fad-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="20fad-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="20fad-152">Anger antalet dagar som en säkerhets kopia ska behållas.</span><span class="sxs-lookup"><span data-stu-id="20fad-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="20fad-153">-StorageContext</span></span>
<span data-ttu-id="20fad-154">Anger det lagrings konto som ska användas för att lagra säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="20fad-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="20fad-155">Använd New-AzStorageContext cmdlet för att få ett **AzureStorageContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="20fad-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="20fad-156">Standardvärdet är det lagrings konto som är kopplat till den virtuella SQL Server-datorn.</span><span class="sxs-lookup"><span data-stu-id="20fad-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20fad-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="20fad-157">-StorageKey</span></span>
<span data-ttu-id="20fad-158">Anger lagrings Key för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="20fad-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="20fad-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="20fad-159">-StorageUri</span></span>
<span data-ttu-id="20fad-160">Anger URI (Uniform Resource Identifier) för Blob Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="20fad-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="20fad-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fad-161">CommonParameters</span></span>
<span data-ttu-id="20fad-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20fad-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fad-163">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20fad-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fad-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20fad-164">INPUTS</span></span>

### <span data-ttu-id="20fad-165">System. String</span><span class="sxs-lookup"><span data-stu-id="20fad-165">System.String</span></span>

### <span data-ttu-id="20fad-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20fad-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="20fad-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="20fad-167">System.Int32</span></span>

### <span data-ttu-id="20fad-168">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="20fad-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="20fad-169">System. URI</span><span class="sxs-lookup"><span data-stu-id="20fad-169">System.Uri</span></span>

### <span data-ttu-id="20fad-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="20fad-170">System.Security.SecureString</span></span>

### <span data-ttu-id="20fad-171">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20fad-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="20fad-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20fad-172">OUTPUTS</span></span>

### <span data-ttu-id="20fad-173">Microsoft. Azure. commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="20fad-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="20fad-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20fad-174">NOTES</span></span>

## <span data-ttu-id="20fad-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20fad-175">RELATED LINKS</span></span>

[<span data-ttu-id="20fad-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="20fad-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="20fad-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="20fad-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


