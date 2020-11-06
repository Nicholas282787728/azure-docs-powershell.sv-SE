---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574218"
---
# <span data-ttu-id="f00f7-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="f00f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f00f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f00f7-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="f00f7-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f00f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f00f7-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f00f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f00f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f00f7-106">Cmdleten **New-AzureRmRecoveryServicesBackupProtectionPolicy** skapar en säkerhets kopierings skydds princip i ett valv.</span><span class="sxs-lookup"><span data-stu-id="f00f7-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="f00f7-107">En skydds princip är kopplad till minst en bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="f00f7-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="f00f7-108">Bevarande principen definierar hur länge en återställnings punkt behålls med Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="f00f7-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="f00f7-109">Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta standard princip för bevarande.</span><span class="sxs-lookup"><span data-stu-id="f00f7-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="f00f7-110">Och du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta standard schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="f00f7-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="f00f7-111">**SchedulePolicy** -och **RetentionPolicy** -objekten används som indata för den **nya-AzureRmRecoveryServicesBackupProtectionPolicy-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f00f7-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="f00f7-112">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f00f7-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f00f7-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f00f7-113">EXAMPLES</span></span>

### <span data-ttu-id="f00f7-114">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f00f7-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="f00f7-115">Det första kommandot får en grundläggande **SchedulePolicyObject** och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="f00f7-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="f00f7-116">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="f00f7-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="f00f7-117">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid.</span><span class="sxs-lookup"><span data-stu-id="f00f7-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="f00f7-118">Det fjärde kommandot lägger till dagens datum och aktuellt klock slag i $Dt som den schemalagda körnings tiden till schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="f00f7-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="f00f7-119">Det femte kommandot får ett bas **RetentionPolicy** -objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="f00f7-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="f00f7-120">Det sjätte kommandot ställer in policyn för bevarande av tids perioden till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="f00f7-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="f00f7-121">Med kommandot slut skapas ett **BackupProtectionPolicy** -objekt baserat på schema-och bevarande principer som skapas av föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="f00f7-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="f00f7-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f00f7-122">PARAMETERS</span></span>

### <span data-ttu-id="f00f7-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f00f7-123">-BackupManagementType</span></span>
<span data-ttu-id="f00f7-124">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="f00f7-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="f00f7-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f00f7-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f00f7-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f00f7-126">AzureVM</span></span> 
- <span data-ttu-id="f00f7-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="f00f7-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00f7-128">-DefaultProfile</span></span>
<span data-ttu-id="f00f7-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f00f7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00f7-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f00f7-130">-Name</span></span>
<span data-ttu-id="f00f7-131">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="f00f7-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="f00f7-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-132">-RetentionPolicy</span></span>
<span data-ttu-id="f00f7-133">Anger bas **RetentionPolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="f00f7-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="f00f7-134">Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta ett **RetentionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f00f7-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f7-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-135">-SchedulePolicy</span></span>
<span data-ttu-id="f00f7-136">Anger bas **SchedulePolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="f00f7-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="f00f7-137">Du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta ett **SchedulePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f00f7-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f7-138">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="f00f7-138">-WorkloadType</span></span>
<span data-ttu-id="f00f7-139">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="f00f7-139">Specifies the workload type.</span></span>
<span data-ttu-id="f00f7-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f00f7-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f00f7-141">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f00f7-141">AzureVM</span></span> 
- <span data-ttu-id="f00f7-142">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="f00f7-142">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00f7-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f00f7-143">-Confirm</span></span>
<span data-ttu-id="f00f7-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f00f7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00f7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00f7-145">-WhatIf</span></span>
<span data-ttu-id="f00f7-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f00f7-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f00f7-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f00f7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f00f7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00f7-148">CommonParameters</span></span>
<span data-ttu-id="f00f7-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00f7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00f7-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00f7-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00f7-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f00f7-151">INPUTS</span></span>

### <span data-ttu-id="f00f7-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="f00f7-152">None</span></span>
<span data-ttu-id="f00f7-153">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f00f7-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f00f7-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f00f7-154">OUTPUTS</span></span>

### <span data-ttu-id="f00f7-155">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="f00f7-155">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="f00f7-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f00f7-156">NOTES</span></span>

## <span data-ttu-id="f00f7-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f00f7-157">RELATED LINKS</span></span>

[<span data-ttu-id="f00f7-158">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f00f7-158">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f00f7-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-159">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f00f7-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f00f7-160">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="f00f7-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="f00f7-161">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="f00f7-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-162">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f00f7-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f00f7-163">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


