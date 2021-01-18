---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9f89a39b283f073c0fe826f22157570be29e74b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523970"
---
# <span data-ttu-id="907a2-101">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-101">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="907a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="907a2-102">SYNOPSIS</span></span>
<span data-ttu-id="907a2-103">Ändrar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="907a2-103">Modifies a Backup protection policy.</span></span>

## <span data-ttu-id="907a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="907a2-104">SYNTAX</span></span>

### <span data-ttu-id="907a2-105">ModifyPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="907a2-105">ModifyPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="907a2-106">FixPolicyParamSet</span><span class="sxs-lookup"><span data-stu-id="907a2-106">FixPolicyParamSet</span></span>
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="907a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="907a2-107">DESCRIPTION</span></span>
<span data-ttu-id="907a2-108">Cmdleten **set-AzRecoveryServicesBackupProtectionPolicy** ändrar en befintlig Azure Backup-säkerhetsprincip.</span><span class="sxs-lookup"><span data-stu-id="907a2-108">The **Set-AzRecoveryServicesBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="907a2-109">Du kan ändra schema för säkerhets kopiering och bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="907a2-109">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="907a2-110">De ändringar du gör påverkar säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="907a2-110">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="907a2-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="907a2-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="907a2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="907a2-112">EXAMPLES</span></span>

### <span data-ttu-id="907a2-113">Exempel 1: ändra en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="907a2-113">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="907a2-114">Här följer en beskrivning av hur du gör för att ändra skydds principer:</span><span class="sxs-lookup"><span data-stu-id="907a2-114">Here is the high-level description of the steps to be followed for modifying a protection policy:</span></span> 
1.  <span data-ttu-id="907a2-115">Skaffa en bas SchedulePolicyObject och bas RetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="907a2-115">Get a base SchedulePolicyObject and base RetentionPolicyObject.</span></span> <span data-ttu-id="907a2-116">Lagra dem i en variabel.</span><span class="sxs-lookup"><span data-stu-id="907a2-116">Store them in some variable.</span></span>
2.  <span data-ttu-id="907a2-117">Ange olika parametrar för schema-och bevarande princip objekt enligt dina behov.</span><span class="sxs-lookup"><span data-stu-id="907a2-117">Set the different parameters of schedule and retention policy object as per your requirement.</span></span> <span data-ttu-id="907a2-118">I exempel skriptet ovan försöker vi att ange en veckovis skydds policy.</span><span class="sxs-lookup"><span data-stu-id="907a2-118">For example- In the above sample script, we are trying to set a weekly protection policy.</span></span> <span data-ttu-id="907a2-119">Därför ändrade vi schema frekvensen till "vecka" och uppdaterade tiden för schema körningen.</span><span class="sxs-lookup"><span data-stu-id="907a2-119">Hence, we changed the schedule frequency to "Weekly" and also updated the schedule run time.</span></span> <span data-ttu-id="907a2-120">I bevarande princip-objekt uppdaterades varaktigheten för veckovis bevarande och ange korrekt "vecko schema aktive rad".</span><span class="sxs-lookup"><span data-stu-id="907a2-120">In the retention policy object, we updated the weekly retention duration and set the correct "weekly schedule enabled" flag.</span></span> <span data-ttu-id="907a2-121">Om du vill ange en daglig princip anger du flaggan "dagligt schema aktiverat" till sant och tilldelar lämpliga värden för andra objekt parametrar.</span><span class="sxs-lookup"><span data-stu-id="907a2-121">In case you want to set a Daily policy, set the "daily schedule enabled" flag to true and assign appropriate values for other object parameters.</span></span>
3.  <span data-ttu-id="907a2-122">Skaffa den säkerhets kopierings princip som du vill ändra och spara den i en variabel.</span><span class="sxs-lookup"><span data-stu-id="907a2-122">Get the backup protection policy that you want to modify and store it in a variable.</span></span> <span data-ttu-id="907a2-123">I exemplet ovan hämtade vi säkerhets kopierings principen med namnet "TestPolicy" som vi ville ändra.</span><span class="sxs-lookup"><span data-stu-id="907a2-123">In the above example, we retrieved the backup policy with the name "TestPolicy" that we wanted to modify.</span></span>
4.  <span data-ttu-id="907a2-124">Ändra säkerhets kopierings principen som hämtas i steg 3 med hjälp av det ändrade schema princip-och bevarande princip objekt.</span><span class="sxs-lookup"><span data-stu-id="907a2-124">Modify the backup protection policy retrieved in step 3 using the modified schedule policy object and retention policy object.</span></span>

## <span data-ttu-id="907a2-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="907a2-125">PARAMETERS</span></span>

### <span data-ttu-id="907a2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907a2-126">-DefaultProfile</span></span>
<span data-ttu-id="907a2-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="907a2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="907a2-128">-FixForInconsistentItems</span><span class="sxs-lookup"><span data-stu-id="907a2-128">-FixForInconsistentItems</span></span>
<span data-ttu-id="907a2-129">Switch parameter anger om princip uppdateringen för misslyckade försök ska upprepas eller inte.</span><span class="sxs-lookup"><span data-stu-id="907a2-129">Switch Parameter indicating whether or not to retry Policy Update for failed items.</span></span>

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

### <span data-ttu-id="907a2-130">-Princip</span><span class="sxs-lookup"><span data-stu-id="907a2-130">-Policy</span></span>
<span data-ttu-id="907a2-131">Anger säkerhets kopierings principen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="907a2-131">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="907a2-132">För att hämta ett **BackupProtectionPolicy** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="907a2-132">To obtain a **BackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="907a2-133">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-133">-RetentionPolicy</span></span>
<span data-ttu-id="907a2-134">Anger grundläggande bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="907a2-134">Specifies the base retention policy.</span></span>
<span data-ttu-id="907a2-135">För att hämta ett **RetentionPolicy** -objekt, Använd cmdleten Get-AzRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="907a2-135">To obtain a **RetentionPolicy** object, use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="907a2-136">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-136">-SchedulePolicy</span></span>
<span data-ttu-id="907a2-137">Anger det grundläggande schemaobjektet.</span><span class="sxs-lookup"><span data-stu-id="907a2-137">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="907a2-138">Du kan hämta ett **SchedulePolicy** -objekt med Get-AzRecoveryServicesBackupSchedulePolicyObject-objektet.</span><span class="sxs-lookup"><span data-stu-id="907a2-138">To obtain a **SchedulePolicy** object, use the Get-AzRecoveryServicesBackupSchedulePolicyObject object.</span></span>

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

### <span data-ttu-id="907a2-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="907a2-139">-VaultId</span></span>
<span data-ttu-id="907a2-140">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="907a2-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="907a2-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="907a2-141">-Confirm</span></span>
<span data-ttu-id="907a2-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="907a2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="907a2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="907a2-143">-WhatIf</span></span>
<span data-ttu-id="907a2-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="907a2-144">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="907a2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907a2-145">CommonParameters</span></span>
<span data-ttu-id="907a2-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="907a2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907a2-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="907a2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907a2-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="907a2-148">INPUTS</span></span>

### <span data-ttu-id="907a2-149">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="907a2-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="907a2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="907a2-150">System.String</span></span>

## <span data-ttu-id="907a2-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="907a2-151">OUTPUTS</span></span>

### <span data-ttu-id="907a2-152">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="907a2-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="907a2-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="907a2-153">NOTES</span></span>

## <span data-ttu-id="907a2-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="907a2-154">RELATED LINKS</span></span>

[<span data-ttu-id="907a2-155">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-155">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="907a2-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="907a2-156">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="907a2-157">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-157">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="907a2-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="907a2-158">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


