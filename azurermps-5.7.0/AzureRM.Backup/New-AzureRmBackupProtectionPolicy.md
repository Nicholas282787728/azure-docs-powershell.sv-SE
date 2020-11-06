---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582095"
---
# <span data-ttu-id="0b7e5-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="0b7e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7e5-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b7e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b7e5-104">SYNTAX</span></span>

### <span data-ttu-id="0b7e5-105">NoScheduleParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0b7e5-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b7e5-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="0b7e5-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b7e5-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="0b7e5-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b7e5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b7e5-108">DESCRIPTION</span></span>
<span data-ttu-id="0b7e5-109">Cmdleten **New-AzureRmBackupProtectionPolicy** skapar en Azure Backup-princip som ett Azure PowerShell-objekt.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="0b7e5-110">En säkerhets kopierings princip anger när och hur ofta säkerhets kopieringen ska säkerhetskopiera ett objekt.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="0b7e5-111">I Enable-AzureRmBackupProtection cmdlet används en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="0b7e5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b7e5-112">EXAMPLES</span></span>

### <span data-ttu-id="0b7e5-113">Exempel 1: skapa en daglig säkerhets kopierings princip med daglig och månads vis bevarande</span><span class="sxs-lookup"><span data-stu-id="0b7e5-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="0b7e5-114">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="0b7e5-115">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="0b7e5-116">Med det andra kommandot skapas en bevarande princip för 30 dagar efter varje dag och sparas sedan i $Daily variabel.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="0b7e5-117">Det tredje kommandot skapar en bevarande princip som behåller säkerhets kopian på den tionde och tjugonde dagen i varje månad under tolv månader.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="0b7e5-118">Kommandot lagrar bevarande principen i $Monthly variabel.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="0b7e5-119">Med kommandot slut skapas en säkerhets kopierings princip för valvet i $Vault som har en daglig säkerhets kopia av 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="0b7e5-120">Kommandot tilldelar de bevarande principer som lagras i $Daily och $Monthly.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="0b7e5-121">Resultatet sparas i $ProtectionPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="0b7e5-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b7e5-122">PARAMETERS</span></span>

### <span data-ttu-id="0b7e5-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="0b7e5-123">-BackupTime</span></span>
<span data-ttu-id="0b7e5-124">Anger klock slaget som ett **datetime** -objekt för säkerhets kopieringen.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="0b7e5-125">För att få ett **datum/tid** -värde, Använd cmdleten Get-Date.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="0b7e5-126">Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0b7e5-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-127">-Dagligen</span><span class="sxs-lookup"><span data-stu-id="0b7e5-127">-Daily</span></span>
<span data-ttu-id="0b7e5-128">Visar att säkerhets kopieringen körs på ett dagligt schema.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="0b7e5-129">-DaysOfWeek</span></span>
<span data-ttu-id="0b7e5-130">Anger en matris med dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="0b7e5-131">Med den här principen körs säkerhets kopior på de dagar som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="0b7e5-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0b7e5-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b7e5-133">Dagarna</span><span class="sxs-lookup"><span data-stu-id="0b7e5-133">Monday</span></span> 
- <span data-ttu-id="0b7e5-134">Torsdag</span><span class="sxs-lookup"><span data-stu-id="0b7e5-134">Tuesday</span></span> 
- <span data-ttu-id="0b7e5-135">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="0b7e5-135">Wednesday</span></span> 
- <span data-ttu-id="0b7e5-136">Torsdag</span><span class="sxs-lookup"><span data-stu-id="0b7e5-136">Thursday</span></span> 
- <span data-ttu-id="0b7e5-137">Fredag</span><span class="sxs-lookup"><span data-stu-id="0b7e5-137">Friday</span></span> 
- <span data-ttu-id="0b7e5-138">Afton</span><span class="sxs-lookup"><span data-stu-id="0b7e5-138">Saturday</span></span> 
- <span data-ttu-id="0b7e5-139">Lördag</span><span class="sxs-lookup"><span data-stu-id="0b7e5-139">Sunday</span></span>

<span data-ttu-id="0b7e5-140">Om du anger en *vecko* parameter anger du den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7e5-141">-DefaultProfile</span></span>
<span data-ttu-id="0b7e5-142">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0b7e5-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b7e5-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b7e5-143">-Name</span></span>
<span data-ttu-id="0b7e5-144">Anger ett namn för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="0b7e5-145">Välj ett namn som är unikt i valvet.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-146">-RetentionPolicy</span></span>
<span data-ttu-id="0b7e5-147">Anger en matris med bevarande principer för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="0b7e5-148">För att få en **AzureRmBackupRetentionPolicy** , Använd cmdleten New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-149">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0b7e5-149">-Type</span></span>
<span data-ttu-id="0b7e5-150">Anger den typ av säkerhets kopia som policyn gäller.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="0b7e5-151">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-152">-Valv</span><span class="sxs-lookup"><span data-stu-id="0b7e5-152">-Vault</span></span>
<span data-ttu-id="0b7e5-153">Anger det Azure Backup-valv som säkerhets kopierings principen tillhör.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="0b7e5-154">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-155">-Vecka</span><span class="sxs-lookup"><span data-stu-id="0b7e5-155">-Weekly</span></span>
<span data-ttu-id="0b7e5-156">Anger att säkerhets kopierings principen utlöstes varje vecka en eller flera dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7e5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7e5-157">CommonParameters</span></span>
<span data-ttu-id="0b7e5-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7e5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7e5-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7e5-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7e5-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b7e5-160">INPUTS</span></span>

### <span data-ttu-id="0b7e5-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="0b7e5-161">None</span></span>

## <span data-ttu-id="0b7e5-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b7e5-162">OUTPUTS</span></span>

### <span data-ttu-id="0b7e5-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="0b7e5-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b7e5-164">NOTES</span></span>
* <span data-ttu-id="0b7e5-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="0b7e5-165">None</span></span>

## <span data-ttu-id="0b7e5-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b7e5-166">RELATED LINKS</span></span>

[<span data-ttu-id="0b7e5-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0b7e5-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="0b7e5-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="0b7e5-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0b7e5-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="0b7e5-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0b7e5-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="0b7e5-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="0b7e5-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b7e5-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


