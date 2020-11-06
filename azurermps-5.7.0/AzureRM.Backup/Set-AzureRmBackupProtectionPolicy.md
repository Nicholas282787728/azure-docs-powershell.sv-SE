---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582067"
---
# <span data-ttu-id="70765-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70765-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="70765-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70765-102">SYNOPSIS</span></span>
<span data-ttu-id="70765-103">Ändrar en befintlig skydds princip.</span><span class="sxs-lookup"><span data-stu-id="70765-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70765-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70765-104">SYNTAX</span></span>

### <span data-ttu-id="70765-105">NoScheduleParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70765-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70765-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="70765-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70765-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="70765-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70765-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70765-108">DESCRIPTION</span></span>
<span data-ttu-id="70765-109">Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig skydds princip i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="70765-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="70765-110">Du kan ändra följande komponent komponenter:</span><span class="sxs-lookup"><span data-stu-id="70765-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="70765-111">Namn</span><span class="sxs-lookup"><span data-stu-id="70765-111">Name</span></span>
- <span data-ttu-id="70765-112">Säkerhets kopierings schema</span><span class="sxs-lookup"><span data-stu-id="70765-112">Backup schedule</span></span>
- <span data-ttu-id="70765-113">Bevarande principer</span><span class="sxs-lookup"><span data-stu-id="70765-113">Retention policies</span></span>

<span data-ttu-id="70765-114">Alla ändringar kan påverka säkerhets kopiering och bevarande av objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="70765-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="70765-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70765-115">EXAMPLES</span></span>

## <span data-ttu-id="70765-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70765-116">PARAMETERS</span></span>

### <span data-ttu-id="70765-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="70765-117">-BackupTime</span></span>
<span data-ttu-id="70765-118">Anger den nya säkerhets kopierings tiden som ett **datetime** -objekt för principen.</span><span class="sxs-lookup"><span data-stu-id="70765-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="70765-119">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="70765-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="70765-120">Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="70765-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-121">-Dagligen</span><span class="sxs-lookup"><span data-stu-id="70765-121">-Daily</span></span>
<span data-ttu-id="70765-122">Visar att säkerhets kopieringen körs på ett dagligt schema.</span><span class="sxs-lookup"><span data-stu-id="70765-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="70765-123">-DaysOfWeek</span></span>
<span data-ttu-id="70765-124">Anger en matris med dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="70765-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="70765-125">Med den här principen körs säkerhets kopior på de dagar som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="70765-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="70765-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="70765-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70765-127">Dagarna</span><span class="sxs-lookup"><span data-stu-id="70765-127">Monday</span></span> 
- <span data-ttu-id="70765-128">Torsdag</span><span class="sxs-lookup"><span data-stu-id="70765-128">Tuesday</span></span> 
- <span data-ttu-id="70765-129">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="70765-129">Wednesday</span></span> 
- <span data-ttu-id="70765-130">Torsdag</span><span class="sxs-lookup"><span data-stu-id="70765-130">Thursday</span></span> 
- <span data-ttu-id="70765-131">Fredag</span><span class="sxs-lookup"><span data-stu-id="70765-131">Friday</span></span> 
- <span data-ttu-id="70765-132">Afton</span><span class="sxs-lookup"><span data-stu-id="70765-132">Saturday</span></span> 
- <span data-ttu-id="70765-133">Lördag</span><span class="sxs-lookup"><span data-stu-id="70765-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70765-134">-DefaultProfile</span></span>
<span data-ttu-id="70765-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="70765-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70765-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="70765-136">-NewName</span></span>
<span data-ttu-id="70765-137">Anger det nya namnet för principen.</span><span class="sxs-lookup"><span data-stu-id="70765-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="70765-138">Det här namnet måste vara unikt i ett valv.</span><span class="sxs-lookup"><span data-stu-id="70765-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70765-139">-ProtectionPolicy</span></span>
<span data-ttu-id="70765-140">Anger skydds princip som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="70765-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="70765-141">Använd Get-AzureRmBackupProtectionPolicy cmdlet för att få ett **AzureRmBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="70765-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70765-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="70765-142">-RetentionPolicy</span></span>
<span data-ttu-id="70765-143">Anger en matris med bevarande principer för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="70765-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="70765-144">För att hämta **AzureRmBackupRetentionPolicy** -objekt, Använd cmdleten New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="70765-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-145">-Vecka</span><span class="sxs-lookup"><span data-stu-id="70765-145">-Weekly</span></span>
<span data-ttu-id="70765-146">Visar att säkerhets kopieringen körs på ett vecko schema.</span><span class="sxs-lookup"><span data-stu-id="70765-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70765-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70765-147">CommonParameters</span></span>
<span data-ttu-id="70765-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70765-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70765-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70765-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70765-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70765-150">INPUTS</span></span>

### <span data-ttu-id="70765-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70765-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="70765-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70765-152">OUTPUTS</span></span>

### <span data-ttu-id="70765-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="70765-153">None</span></span>

## <span data-ttu-id="70765-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70765-154">NOTES</span></span>

## <span data-ttu-id="70765-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70765-155">RELATED LINKS</span></span>

[<span data-ttu-id="70765-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70765-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


