---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 1a9eb2ef731e7ce555fbac1a08cd8468de83ebc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582559"
---
# <span data-ttu-id="1fb76-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="1fb76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fb76-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb76-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="1fb76-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fb76-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fb76-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb76-106">Cmdleten **New-AzureRmRecoveryServicesBackupProtectionPolicy** skapar en säkerhets kopierings skydds princip i ett valv.</span><span class="sxs-lookup"><span data-stu-id="1fb76-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="1fb76-107">En skydds princip är kopplad till minst en bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="1fb76-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="1fb76-108">Bevarande principen definierar hur länge en återställnings punkt behålls med Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="1fb76-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="1fb76-109">Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta standard princip för bevarande.</span><span class="sxs-lookup"><span data-stu-id="1fb76-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="1fb76-110">Och du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta standard schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="1fb76-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="1fb76-111">**SchedulePolicy** -och **RetentionPolicy** -objekten används som indata för den **nya-AzureRmRecoveryServicesBackupProtectionPolicy-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fb76-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="1fb76-112">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fb76-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1fb76-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fb76-113">EXAMPLES</span></span>

### <span data-ttu-id="1fb76-114">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="1fb76-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="1fb76-115">Det första kommandot får en grundläggande **SchedulePolicyObject** och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="1fb76-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="1fb76-116">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="1fb76-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="1fb76-117">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid.</span><span class="sxs-lookup"><span data-stu-id="1fb76-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="1fb76-118">Det fjärde kommandot lägger till dagens datum och aktuellt klock slag i $Dt som den schemalagda körnings tiden till schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="1fb76-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="1fb76-119">Det femte kommandot får ett bas **RetentionPolicy** -objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="1fb76-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="1fb76-120">Det sjätte kommandot ställer in policyn för bevarande av tids perioden till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="1fb76-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="1fb76-121">Med kommandot slut skapas ett **BackupProtectionPolicy** -objekt baserat på schema-och bevarande principer som skapas av föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="1fb76-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="1fb76-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fb76-122">PARAMETERS</span></span>

### <span data-ttu-id="1fb76-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1fb76-123">-BackupManagementType</span></span>
<span data-ttu-id="1fb76-124">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="1fb76-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="1fb76-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1fb76-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fb76-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1fb76-126">AzureVM</span></span> 
- <span data-ttu-id="1fb76-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="1fb76-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb76-128">-DefaultProfile</span></span>
<span data-ttu-id="1fb76-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb76-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb76-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fb76-130">-Name</span></span>
<span data-ttu-id="1fb76-131">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="1fb76-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="1fb76-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-132">-RetentionPolicy</span></span>
<span data-ttu-id="1fb76-133">Anger bas **RetentionPolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="1fb76-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="1fb76-134">Du kan använda Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta ett **RetentionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1fb76-134">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-135">-SchedulePolicy</span></span>
<span data-ttu-id="1fb76-136">Anger bas **SchedulePolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="1fb76-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="1fb76-137">Du kan använda Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta ett **SchedulePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1fb76-137">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1fb76-138">-VaultId</span></span>
<span data-ttu-id="1fb76-139">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="1fb76-139">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1fb76-140">-WorkloadType</span></span>
<span data-ttu-id="1fb76-141">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="1fb76-141">Specifies the workload type.</span></span>
<span data-ttu-id="1fb76-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1fb76-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fb76-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1fb76-143">AzureVM</span></span> 
- <span data-ttu-id="1fb76-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="1fb76-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1fb76-145">-Confirm</span></span>
<span data-ttu-id="1fb76-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1fb76-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb76-147">-WhatIf</span></span>
<span data-ttu-id="1fb76-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1fb76-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fb76-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1fb76-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fb76-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb76-150">CommonParameters</span></span>
<span data-ttu-id="1fb76-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb76-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb76-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb76-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb76-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fb76-153">INPUTS</span></span>

### <span data-ttu-id="1fb76-154">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1fb76-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="1fb76-155">System. Nullable ' 1 [[Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. Models. BackupManagementType, Microsoft. Azure. kommandon. RecoveryServices. backup. Models, version = 4.3.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1fb76-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.Commands.RecoveryServices.Backup.Models, Version=4.3.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1fb76-156">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="1fb76-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="1fb76-157">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="1fb76-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="1fb76-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb76-158">System.String</span></span>
<span data-ttu-id="1fb76-159">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1fb76-159">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="1fb76-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fb76-160">OUTPUTS</span></span>

### <span data-ttu-id="1fb76-161">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="1fb76-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="1fb76-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fb76-162">NOTES</span></span>

## <span data-ttu-id="1fb76-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fb76-163">RELATED LINKS</span></span>

[<span data-ttu-id="1fb76-164">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1fb76-164">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1fb76-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-165">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1fb76-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1fb76-166">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="1fb76-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="1fb76-167">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="1fb76-168">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-168">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="1fb76-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb76-169">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


