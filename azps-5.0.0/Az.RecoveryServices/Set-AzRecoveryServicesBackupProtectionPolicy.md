---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: f9cd7064c1949639526f2e7b84f01fb6355b584f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263428"
---
# <span data-ttu-id="7b046-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="7b046-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b046-102">SYNOPSIS</span></span>
<span data-ttu-id="7b046-103">Ändrar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="7b046-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="7b046-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b046-104">SYNTAX</span></span>

### <span data-ttu-id="7b046-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="7b046-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b046-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="7b046-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b046-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b046-107">DESCRIPTION</span></span>
<span data-ttu-id="7b046-108">Cmdleten **set-AzRecoveryServicesBackupProtectionPolicy** ändrar en befintlig Azure Backup-säkerhetsprincip.</span><span class="sxs-lookup"><span data-stu-id="7b046-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="7b046-109">Du kan ändra schema för säkerhets kopiering och bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="7b046-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="7b046-110">De ändringar du gör påverkar säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="7b046-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="7b046-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b046-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7b046-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b046-112">EXAMPLES</span></span>

### <span data-ttu-id="7b046-113">Exempel 1: ändra en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="7b046-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> $Pol.AzureBackupRGName = "RG_prefix"
PS C:\> $Pol.AzureBackupRGNameSuffix = "RG_suffix"
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="7b046-114">Det första kommandot får ett bas objekt i SchedulePolicy och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="7b046-114">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="7b046-115">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="7b046-115">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="7b046-116">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid och sedan lagras de i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="7b046-116">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="7b046-117">Det fjärde kommandot lägger till datum och tid i $DT till tids schema principen.</span><span class="sxs-lookup"><span data-stu-id="7b046-117">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="7b046-118">Det femte kommandot får ett grundläggande bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="7b046-118">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="7b046-119">Med sjätte kommandot anges varaktigheten till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="7b046-119">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="7b046-120">Det sjunde kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="7b046-120">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7b046-121">I åttonde och nionde anges de resurs grupp parametrar som är associerade med principer som lagrar återställnings punkterna.</span><span class="sxs-lookup"><span data-stu-id="7b046-121">The eighth and ninth sets the resource group parameters associated with policy which stores the restore points.</span></span>
<span data-ttu-id="7b046-122">Det slutliga kommandot ändrar säkerhets kopierings princip för $Pol genom att använda en schema princip i $SchPol och bevarande principen i $RetPol.</span><span class="sxs-lookup"><span data-stu-id="7b046-122">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="7b046-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b046-123">PARAMETERS</span></span>

### <span data-ttu-id="7b046-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b046-124">-DefaultProfile</span></span>
<span data-ttu-id="7b046-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b046-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b046-126">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="7b046-126">-FixForInconsistentItems</span></span>
<span data-ttu-id="7b046-127">Switch parameter anger om princip uppdateringen för misslyckade försök ska upprepas eller inte.</span><span class="sxs-lookup"><span data-stu-id="7b046-127">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b046-128">-Princip</span><span class="sxs-lookup"><span data-stu-id="7b046-128">-Policy</span></span>
<span data-ttu-id="7b046-129">Anger säkerhets kopierings principen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="7b046-129">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="7b046-130">För att hämta ett **BackupProtectionPolicy** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7b046-130">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b046-131">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-131">-RetentionPolicy</span></span>
<span data-ttu-id="7b046-132">Anger grundläggande bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="7b046-132">Specifies the base retention policy.</span></span>
<span data-ttu-id="7b046-133">För att hämta ett **RetentionPolicy** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="7b046-133">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b046-134">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-134">-SchedulePolicy</span></span>
<span data-ttu-id="7b046-135">Anger det grundläggande schemaobjektet.</span><span class="sxs-lookup"><span data-stu-id="7b046-135">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="7b046-136">Du kan hämta ett **SchedulePolicy** -objekt med Get-AzRecoveryServicesBackupSchedulePolicyObject-objektet.</span><span class="sxs-lookup"><span data-stu-id="7b046-136">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b046-137">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7b046-137">-VaultId</span></span>
<span data-ttu-id="7b046-138">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="7b046-138">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7b046-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b046-139">-Confirm</span></span>
<span data-ttu-id="7b046-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b046-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b046-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b046-141">-WhatIf</span></span>
<span data-ttu-id="7b046-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b046-142">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="7b046-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b046-143">CommonParameters</span></span>
<span data-ttu-id="7b046-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b046-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b046-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b046-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b046-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b046-146">INPUTS</span></span>

### <span data-ttu-id="7b046-147">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="7b046-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="7b046-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7b046-148">System.String</span></span>

## <span data-ttu-id="7b046-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b046-149">OUTPUTS</span></span>

### <span data-ttu-id="7b046-150">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="7b046-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7b046-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b046-151">NOTES</span></span>

## <span data-ttu-id="7b046-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b046-152">RELATED LINKS</span></span>

[<span data-ttu-id="7b046-153">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-153">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7b046-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7b046-154">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="7b046-155">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-155">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="7b046-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b046-156">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


