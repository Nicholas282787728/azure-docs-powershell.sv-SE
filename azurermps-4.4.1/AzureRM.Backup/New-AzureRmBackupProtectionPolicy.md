---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 803299a64fb98aecc249bc7bb2f505ada74a5573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583840"
---
# <span data-ttu-id="b1266-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="b1266-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1266-102">SYNOPSIS</span></span>
<span data-ttu-id="b1266-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="b1266-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1266-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1266-104">SYNTAX</span></span>

### <span data-ttu-id="b1266-105">NoScheduleParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b1266-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1266-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="b1266-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1266-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="b1266-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1266-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1266-108">DESCRIPTION</span></span>
<span data-ttu-id="b1266-109">Cmdleten **New-AzureRmBackupProtectionPolicy** skapar en Azure Backup-princip som ett Azure PowerShell-objekt.</span><span class="sxs-lookup"><span data-stu-id="b1266-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="b1266-110">En säkerhets kopierings princip anger när och hur ofta säkerhets kopieringen ska säkerhetskopiera ett objekt.</span><span class="sxs-lookup"><span data-stu-id="b1266-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="b1266-111">I Enable-AzureRmBackupProtection cmdlet används en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="b1266-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="b1266-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1266-112">EXAMPLES</span></span>

### <span data-ttu-id="b1266-113">Exempel 1: skapa en daglig säkerhets kopierings princip med daglig och månads vis bevarande</span><span class="sxs-lookup"><span data-stu-id="b1266-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="b1266-114">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1266-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b1266-115">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="b1266-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="b1266-116">Med det andra kommandot skapas en bevarande princip för 30 dagar efter varje dag och sparas sedan i $Daily variabel.</span><span class="sxs-lookup"><span data-stu-id="b1266-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="b1266-117">Det tredje kommandot skapar en bevarande princip som behåller säkerhets kopian på den tionde och tjugonde dagen i varje månad under tolv månader.</span><span class="sxs-lookup"><span data-stu-id="b1266-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="b1266-118">Kommandot lagrar bevarande principen i $Monthly variabel.</span><span class="sxs-lookup"><span data-stu-id="b1266-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="b1266-119">Med kommandot slut skapas en säkerhets kopierings princip för valvet i $Vault som har en daglig säkerhets kopia av 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="b1266-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="b1266-120">Kommandot tilldelar de bevarande principer som lagras i $Daily och $Monthly.</span><span class="sxs-lookup"><span data-stu-id="b1266-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="b1266-121">Resultatet sparas i $ProtectionPolicy variabel.</span><span class="sxs-lookup"><span data-stu-id="b1266-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="b1266-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1266-122">PARAMETERS</span></span>

### <span data-ttu-id="b1266-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="b1266-123">-BackupTime</span></span>
<span data-ttu-id="b1266-124">Anger klock slaget som ett **datetime** -objekt för säkerhets kopieringen.</span><span class="sxs-lookup"><span data-stu-id="b1266-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="b1266-125">För att få ett **datum/tid** -värde, Använd cmdleten Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b1266-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="b1266-126">Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b1266-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-127">-Dagligen</span><span class="sxs-lookup"><span data-stu-id="b1266-127">-Daily</span></span>
<span data-ttu-id="b1266-128">Visar att säkerhets kopieringen körs på ett dagligt schema.</span><span class="sxs-lookup"><span data-stu-id="b1266-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b1266-129">-DaysOfWeek</span></span>
<span data-ttu-id="b1266-130">Anger en matris med dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="b1266-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="b1266-131">Med den här principen körs säkerhets kopior på de dagar som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b1266-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="b1266-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b1266-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1266-133">Dagarna</span><span class="sxs-lookup"><span data-stu-id="b1266-133">Monday</span></span> 
- <span data-ttu-id="b1266-134">Torsdag</span><span class="sxs-lookup"><span data-stu-id="b1266-134">Tuesday</span></span> 
- <span data-ttu-id="b1266-135">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="b1266-135">Wednesday</span></span> 
- <span data-ttu-id="b1266-136">Torsdag</span><span class="sxs-lookup"><span data-stu-id="b1266-136">Thursday</span></span> 
- <span data-ttu-id="b1266-137">Fredag</span><span class="sxs-lookup"><span data-stu-id="b1266-137">Friday</span></span> 
- <span data-ttu-id="b1266-138">Afton</span><span class="sxs-lookup"><span data-stu-id="b1266-138">Saturday</span></span> 
- <span data-ttu-id="b1266-139">Lördag</span><span class="sxs-lookup"><span data-stu-id="b1266-139">Sunday</span></span>

<span data-ttu-id="b1266-140">Om du anger en *vecko* parameter anger du den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b1266-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1266-141">-Name</span></span>
<span data-ttu-id="b1266-142">Anger ett namn för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="b1266-142">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="b1266-143">Välj ett namn som är unikt i valvet.</span><span class="sxs-lookup"><span data-stu-id="b1266-143">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-144">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-144">-RetentionPolicy</span></span>
<span data-ttu-id="b1266-145">Anger en matris med bevarande principer för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="b1266-145">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="b1266-146">För att få en **AzureRmBackupRetentionPolicy** , Använd cmdleten New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="b1266-146">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-147">– Skriv</span><span class="sxs-lookup"><span data-stu-id="b1266-147">-Type</span></span>
<span data-ttu-id="b1266-148">Anger den typ av säkerhets kopia som policyn gäller.</span><span class="sxs-lookup"><span data-stu-id="b1266-148">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="b1266-149">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b1266-149">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-150">-Valv</span><span class="sxs-lookup"><span data-stu-id="b1266-150">-Vault</span></span>
<span data-ttu-id="b1266-151">Anger det Azure Backup-valv som säkerhets kopierings principen tillhör.</span><span class="sxs-lookup"><span data-stu-id="b1266-151">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="b1266-152">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b1266-152">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-153">-Vecka</span><span class="sxs-lookup"><span data-stu-id="b1266-153">-Weekly</span></span>
<span data-ttu-id="b1266-154">Anger att säkerhets kopierings principen utlöstes varje vecka en eller flera dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="b1266-154">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1266-155">-DefaultProfile</span></span>
<span data-ttu-id="b1266-156">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1266-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1266-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1266-157">CommonParameters</span></span>
<span data-ttu-id="b1266-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1266-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1266-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1266-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1266-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1266-160">INPUTS</span></span>

### <span data-ttu-id="b1266-161">Ingen</span><span class="sxs-lookup"><span data-stu-id="b1266-161">None</span></span>

## <span data-ttu-id="b1266-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1266-162">OUTPUTS</span></span>

### <span data-ttu-id="b1266-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="b1266-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1266-164">NOTES</span></span>
* <span data-ttu-id="b1266-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="b1266-165">None</span></span>

## <span data-ttu-id="b1266-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1266-166">RELATED LINKS</span></span>

[<span data-ttu-id="b1266-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b1266-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="b1266-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="b1266-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b1266-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="b1266-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b1266-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="b1266-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="b1266-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b1266-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


