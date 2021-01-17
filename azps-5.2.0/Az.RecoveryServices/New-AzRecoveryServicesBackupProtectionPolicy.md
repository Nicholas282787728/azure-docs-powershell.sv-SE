---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408283"
---
# <span data-ttu-id="98548-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="98548-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="98548-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98548-102">SYNOPSIS</span></span>
<span data-ttu-id="98548-103">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="98548-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="98548-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98548-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98548-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98548-105">DESCRIPTION</span></span>
<span data-ttu-id="98548-106">Cmdleten **New-AzRecoveryServicesBackupProtectionPolicy** skapar en säkerhets kopierings skydds princip i ett valv.</span><span class="sxs-lookup"><span data-stu-id="98548-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="98548-107">En skydds princip är kopplad till minst en bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="98548-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="98548-108">Bevarande principen definierar hur länge en återställnings punkt behålls med Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="98548-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="98548-109">Du kan använda Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta standard princip för bevarande.</span><span class="sxs-lookup"><span data-stu-id="98548-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="98548-110">Och du kan använda Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta standard schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="98548-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="98548-111">**SchedulePolicy** -och **RetentionPolicy** -objekten används som indata för den **nya-AzRecoveryServicesBackupProtectionPolicy-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98548-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="98548-112">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98548-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="98548-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98548-113">EXAMPLES</span></span>

### <span data-ttu-id="98548-114">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="98548-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="98548-115">Det första kommandot får en grundläggande **SchedulePolicyObject** och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="98548-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="98548-116">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="98548-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="98548-117">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid.</span><span class="sxs-lookup"><span data-stu-id="98548-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="98548-118">Det fjärde kommandot lägger till dagens datum och aktuellt klock slag i $Dt som den schemalagda körnings tiden till schemaläggnings principen.</span><span class="sxs-lookup"><span data-stu-id="98548-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="98548-119">Det femte kommandot får ett bas **RetentionPolicy** -objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="98548-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="98548-120">Det sjätte kommandot ställer in policyn för bevarande av tids perioden till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="98548-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="98548-121">Med kommandot slut skapas ett **BackupProtectionPolicy** -objekt baserat på schema-och bevarande principer som skapas av föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="98548-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="98548-122">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="98548-122">Example 2</span></span>

<span data-ttu-id="98548-123">Skapar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="98548-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="98548-124">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="98548-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="98548-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98548-125">PARAMETERS</span></span>

### <span data-ttu-id="98548-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="98548-126">-BackupManagementType</span></span>
<span data-ttu-id="98548-127">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="98548-127">The class of resources being protected.</span></span> <span data-ttu-id="98548-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="98548-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98548-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="98548-129">AzureVM</span></span> 
- <span data-ttu-id="98548-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="98548-130">AzureStorage</span></span>
- <span data-ttu-id="98548-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="98548-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98548-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98548-132">-DefaultProfile</span></span>
<span data-ttu-id="98548-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98548-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98548-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="98548-134">-Name</span></span>
<span data-ttu-id="98548-135">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="98548-135">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="98548-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="98548-136">-RetentionPolicy</span></span>
<span data-ttu-id="98548-137">Anger bas **RetentionPolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="98548-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="98548-138">Du kan använda Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet för att hämta ett **RetentionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="98548-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="98548-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="98548-139">-SchedulePolicy</span></span>
<span data-ttu-id="98548-140">Anger bas **SchedulePolicy** -objektet.</span><span class="sxs-lookup"><span data-stu-id="98548-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="98548-141">Du kan använda Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet för att hämta ett **SchedulePolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="98548-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="98548-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="98548-142">-VaultId</span></span>
<span data-ttu-id="98548-143">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="98548-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="98548-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="98548-144">-WorkloadType</span></span>
<span data-ttu-id="98548-145">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="98548-145">Workload type of the resource.</span></span> <span data-ttu-id="98548-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="98548-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="98548-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="98548-147">AzureVM</span></span> 
- <span data-ttu-id="98548-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="98548-148">AzureFiles</span></span>
- <span data-ttu-id="98548-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="98548-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98548-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98548-150">-Confirm</span></span>
<span data-ttu-id="98548-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98548-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98548-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98548-152">-WhatIf</span></span>
<span data-ttu-id="98548-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98548-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="98548-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98548-154">CommonParameters</span></span>
<span data-ttu-id="98548-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98548-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98548-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98548-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98548-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98548-157">INPUTS</span></span>

### <span data-ttu-id="98548-158">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. WorkloadType</span><span class="sxs-lookup"><span data-stu-id="98548-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="98548-159">System. Nullable ' 1 [[Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. Models. BackupManagementType, Microsoft. Azure. PowerShell. cmdletar. RecoveryServices. backup. Models, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="98548-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="98548-160">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="98548-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="98548-161">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="98548-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="98548-162">System. String</span><span class="sxs-lookup"><span data-stu-id="98548-162">System.String</span></span>

## <span data-ttu-id="98548-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98548-163">OUTPUTS</span></span>

### <span data-ttu-id="98548-164">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="98548-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="98548-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98548-165">NOTES</span></span>

## <span data-ttu-id="98548-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98548-166">RELATED LINKS</span></span>

[<span data-ttu-id="98548-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="98548-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="98548-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="98548-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="98548-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="98548-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="98548-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="98548-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="98548-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="98548-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="98548-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="98548-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


