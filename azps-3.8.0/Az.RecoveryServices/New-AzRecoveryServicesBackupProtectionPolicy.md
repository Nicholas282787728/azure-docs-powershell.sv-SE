---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 05704bc9971d6ef06a03e0401d9a2ba9e99b5cdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090410"
---
# <span data-ttu-id="f7299-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="f7299-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7299-102">SYNOPSIS</span></span>
<span data-ttu-id="f7299-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="f7299-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="f7299-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7299-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7299-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7299-105">DESCRIPTION</span></span>
<span data-ttu-id="f7299-106">Cmdleten **New-AzRecoveryServicesBackupProtectionPolicy** skapar en säkerhets kopierings skydds princip i ett valv.</span><span class="sxs-lookup"><span data-stu-id="f7299-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="f7299-107">En skydds princip är kopplad till minst en bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="f7299-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="f7299-108">Bevarande principen definierar hur länge en återställnings punkt behålls med Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="f7299-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="f7299-109">Du kan använda Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta standard princip för bevarande.</span><span class="sxs-lookup"><span data-stu-id="f7299-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="f7299-110">Och du kan använda Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta standard schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="f7299-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="f7299-111">**SchedulePolicy** -och **RetentionPolicy** -objekten används som indata för den **nya-AzRecoveryServicesBackupProtectionPolicy-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7299-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="f7299-112">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7299-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f7299-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7299-113">EXAMPLES</span></span>

### <span data-ttu-id="f7299-114">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="f7299-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="f7299-115">Det första kommandot får en grundläggande **SchedulePolicyObject** och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="f7299-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="f7299-116">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="f7299-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="f7299-117">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid.</span><span class="sxs-lookup"><span data-stu-id="f7299-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="f7299-118">Det fjärde kommandot lägger till dagens datum och aktuellt klock slag i $Dt som den schemalagda körnings tiden till schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="f7299-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="f7299-119">Det femte kommandot får ett bas **RetentionPolicy** -objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="f7299-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="f7299-120">Det sjätte kommandot ställer in policyn för bevarande av tids perioden till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="f7299-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="f7299-121">Med kommandot slut skapas ett **BackupProtectionPolicy** -objekt baserat på schema-och bevarande principer som skapas av föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="f7299-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="f7299-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7299-122">PARAMETERS</span></span>

### <span data-ttu-id="f7299-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f7299-123">-BackupManagementType</span></span>
<span data-ttu-id="f7299-124">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="f7299-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="f7299-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f7299-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7299-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7299-126">AzureVM</span></span> 
- <span data-ttu-id="f7299-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="f7299-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7299-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7299-128">-DefaultProfile</span></span>
<span data-ttu-id="f7299-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7299-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7299-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="f7299-130">-Name</span></span>
<span data-ttu-id="f7299-131">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="f7299-131">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="f7299-132">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-132">-RetentionPolicy</span></span>
<span data-ttu-id="f7299-133">Anger bas **RetentionPolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="f7299-133">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="f7299-134">Du kan använda Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta ett **RetentionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f7299-134">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="f7299-135">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-135">-SchedulePolicy</span></span>
<span data-ttu-id="f7299-136">Anger bas **SchedulePolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="f7299-136">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="f7299-137">Du kan använda Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta ett **SchedulePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f7299-137">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="f7299-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f7299-138">-VaultId</span></span>
<span data-ttu-id="f7299-139">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="f7299-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f7299-140">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="f7299-140">-WorkloadType</span></span>
<span data-ttu-id="f7299-141">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="f7299-141">Specifies the workload type.</span></span>
<span data-ttu-id="f7299-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f7299-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7299-143">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7299-143">AzureVM</span></span> 
- <span data-ttu-id="f7299-144">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="f7299-144">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7299-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7299-145">-Confirm</span></span>
<span data-ttu-id="f7299-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7299-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7299-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7299-147">-WhatIf</span></span>
<span data-ttu-id="f7299-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7299-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7299-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7299-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7299-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7299-150">CommonParameters</span></span>
<span data-ttu-id="f7299-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7299-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7299-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7299-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7299-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7299-153">INPUTS</span></span>

### <span data-ttu-id="f7299-154">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="f7299-154">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="f7299-155">System. Nullable ' 1 [[Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. Models. BackupManagementType, Microsoft. Azure. PowerShell. cmdletar. RecoveryServices. backup. Models, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f7299-155">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f7299-156">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="f7299-156">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="f7299-157">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="f7299-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="f7299-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f7299-158">System.String</span></span>

## <span data-ttu-id="f7299-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7299-159">OUTPUTS</span></span>

### <span data-ttu-id="f7299-160">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="f7299-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="f7299-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7299-161">NOTES</span></span>

## <span data-ttu-id="f7299-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7299-162">RELATED LINKS</span></span>

[<span data-ttu-id="f7299-163">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f7299-163">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f7299-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f7299-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f7299-165">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="f7299-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="f7299-166">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="f7299-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-167">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="f7299-168">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7299-168">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


