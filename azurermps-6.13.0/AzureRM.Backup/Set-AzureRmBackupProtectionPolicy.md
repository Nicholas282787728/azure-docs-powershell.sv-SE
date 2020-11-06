---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575335"
---
# <span data-ttu-id="5d984-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d984-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="5d984-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d984-102">SYNOPSIS</span></span>
<span data-ttu-id="5d984-103">Ändrar en befintlig skydds princip.</span><span class="sxs-lookup"><span data-stu-id="5d984-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d984-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d984-104">SYNTAX</span></span>

### <span data-ttu-id="5d984-105">NoScheduleParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5d984-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d984-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="5d984-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d984-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="5d984-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d984-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d984-108">DESCRIPTION</span></span>
<span data-ttu-id="5d984-109">Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig skydds princip i Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="5d984-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="5d984-110">Du kan ändra följande komponent komponenter:</span><span class="sxs-lookup"><span data-stu-id="5d984-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="5d984-111">Namn</span><span class="sxs-lookup"><span data-stu-id="5d984-111">Name</span></span>
- <span data-ttu-id="5d984-112">Säkerhets kopierings schema</span><span class="sxs-lookup"><span data-stu-id="5d984-112">Backup schedule</span></span>
- <span data-ttu-id="5d984-113">Bevarande principer alla ändringar kan påverka säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="5d984-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="5d984-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d984-114">EXAMPLES</span></span>

## <span data-ttu-id="5d984-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d984-115">PARAMETERS</span></span>

### <span data-ttu-id="5d984-116">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="5d984-116">-BackupTime</span></span>
<span data-ttu-id="5d984-117">Anger den nya säkerhets kopierings tiden som ett **datetime** -objekt för principen.</span><span class="sxs-lookup"><span data-stu-id="5d984-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="5d984-118">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5d984-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="5d984-119">Om du vill ha information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5d984-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-120">-Dagligen</span><span class="sxs-lookup"><span data-stu-id="5d984-120">-Daily</span></span>
<span data-ttu-id="5d984-121">Visar att säkerhets kopieringen körs på ett dagligt schema.</span><span class="sxs-lookup"><span data-stu-id="5d984-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="5d984-122">-DaysOfWeek</span></span>
<span data-ttu-id="5d984-123">Anger en matris med dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="5d984-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="5d984-124">Med den här principen körs säkerhets kopior på de dagar som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="5d984-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="5d984-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5d984-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d984-126">Dagarna</span><span class="sxs-lookup"><span data-stu-id="5d984-126">Monday</span></span> 
- <span data-ttu-id="5d984-127">Torsdag</span><span class="sxs-lookup"><span data-stu-id="5d984-127">Tuesday</span></span> 
- <span data-ttu-id="5d984-128">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="5d984-128">Wednesday</span></span> 
- <span data-ttu-id="5d984-129">Torsdag</span><span class="sxs-lookup"><span data-stu-id="5d984-129">Thursday</span></span> 
- <span data-ttu-id="5d984-130">Fredag</span><span class="sxs-lookup"><span data-stu-id="5d984-130">Friday</span></span> 
- <span data-ttu-id="5d984-131">Afton</span><span class="sxs-lookup"><span data-stu-id="5d984-131">Saturday</span></span> 
- <span data-ttu-id="5d984-132">Lördag</span><span class="sxs-lookup"><span data-stu-id="5d984-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d984-133">-DefaultProfile</span></span>
<span data-ttu-id="5d984-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5d984-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d984-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="5d984-135">-NewName</span></span>
<span data-ttu-id="5d984-136">Anger det nya namnet för principen.</span><span class="sxs-lookup"><span data-stu-id="5d984-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="5d984-137">Det här namnet måste vara unikt i ett valv.</span><span class="sxs-lookup"><span data-stu-id="5d984-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d984-138">-ProtectionPolicy</span></span>
<span data-ttu-id="5d984-139">Anger skydds princip som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5d984-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="5d984-140">Använd Get-AzureRmBackupProtectionPolicy cmdlet för att få ett **AzureRmBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="5d984-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d984-141">-RetentionPolicy</span></span>
<span data-ttu-id="5d984-142">Anger en matris med bevarande principer för säkerhets kopierings principen.</span><span class="sxs-lookup"><span data-stu-id="5d984-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="5d984-143">För att hämta **AzureRmBackupRetentionPolicy** -objekt, Använd cmdleten New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="5d984-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-144">-Vecka</span><span class="sxs-lookup"><span data-stu-id="5d984-144">-Weekly</span></span>
<span data-ttu-id="5d984-145">Visar att säkerhets kopieringen körs på ett vecko schema.</span><span class="sxs-lookup"><span data-stu-id="5d984-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d984-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d984-146">CommonParameters</span></span>
<span data-ttu-id="5d984-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d984-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d984-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d984-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d984-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d984-149">INPUTS</span></span>

### <span data-ttu-id="5d984-150">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d984-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="5d984-151">Parametrar: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d984-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="5d984-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d984-152">OUTPUTS</span></span>

### <span data-ttu-id="5d984-153">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="5d984-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="5d984-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d984-154">NOTES</span></span>

## <span data-ttu-id="5d984-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d984-155">RELATED LINKS</span></span>

[<span data-ttu-id="5d984-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5d984-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


