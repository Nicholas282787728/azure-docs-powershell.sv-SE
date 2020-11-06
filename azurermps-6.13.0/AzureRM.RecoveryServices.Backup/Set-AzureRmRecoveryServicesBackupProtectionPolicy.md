---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: fb0373e97d719535c87c01c0a4b53b029cc2a878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580727"
---
# <span data-ttu-id="9dbd5-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-101">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="9dbd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9dbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbd5-103">Ändrar en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-103">Modifies a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dbd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9dbd5-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbd5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9dbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbd5-106">Cmdleten **set-AzureRmBackupProtectionPolicy** ändrar en befintlig Azure Backup-säkerhetsprincip.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-106">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing Azure Backup protection policy.</span></span>
<span data-ttu-id="9dbd5-107">Du kan ändra schema för säkerhets kopiering och bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-107">You can modify the Backup schedule and retention policy components.</span></span>
<span data-ttu-id="9dbd5-108">De ändringar du gör påverkar säkerhets kopieringen och bevarande av de objekt som är kopplade till principen.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-108">Any changes you make affect the backup and retention of the items associated with the policy.</span></span>
<span data-ttu-id="9dbd5-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9dbd5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9dbd5-110">EXAMPLES</span></span>

### <span data-ttu-id="9dbd5-111">Exempel 1: ändra en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="9dbd5-111">Example 1: Modify a Backup protection policy</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

<span data-ttu-id="9dbd5-112">Det första kommandot får ett bas objekt i SchedulePolicy och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-112">The first command gets a base SchedulePolicy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="9dbd5-113">Det andra kommandot tar bort alla schemalagda körnings tider från schemaläggnings principen i $SchPol.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-113">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="9dbd5-114">I det tredje kommandot används cmdleten Get-Date för att hämta dagens datum och aktuell tid och sedan lagras de i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-114">The third command uses the Get-Date cmdlet to get the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="9dbd5-115">Det fjärde kommandot lägger till datum och tid i $DT till tids schema principen.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-115">The fourth command adds the date and time in $DT to the schedule run time for the schedule policy.</span></span>
<span data-ttu-id="9dbd5-116">Det femte kommandot får ett grundläggande bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-116">The fifth command gets a base retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="9dbd5-117">Med sjätte kommandot anges varaktigheten till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-117">The sixth command sets the retention duration to 365 days.</span></span>
<span data-ttu-id="9dbd5-118">Det sjunde kommandot får säkerhets kopierings principen med namnet NewPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-118">The seventh command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="9dbd5-119">Det slutliga kommandot ändrar säkerhets kopierings princip för $Pol genom att använda en schema princip i $SchPol och bevarande principen i $RetPol.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-119">The final command modifies the Backup protection policy in $Pol using schedule policy in $SchPol and the retention policy in $RetPol.</span></span>

## <span data-ttu-id="9dbd5-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9dbd5-120">PARAMETERS</span></span>

### <span data-ttu-id="9dbd5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbd5-121">-DefaultProfile</span></span>
<span data-ttu-id="9dbd5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dbd5-123">-Princip</span><span class="sxs-lookup"><span data-stu-id="9dbd5-123">-Policy</span></span>
<span data-ttu-id="9dbd5-124">Anger säkerhets kopierings principen som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-124">Specifies the Backup protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="9dbd5-125">För att hämta ett **BackupProtectionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-125">To obtain a **BackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="9dbd5-126">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-126">-RetentionPolicy</span></span>
<span data-ttu-id="9dbd5-127">Anger grundläggande bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-127">Specifies the base retention policy.</span></span>
<span data-ttu-id="9dbd5-128">För att hämta ett **RetentionPolicy** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-128">To obtain a **RetentionPolicy** object, use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd5-129">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-129">-SchedulePolicy</span></span>
<span data-ttu-id="9dbd5-130">Anger det grundläggande schemaobjektet.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-130">Specifies the base schedule policy object.</span></span>
<span data-ttu-id="9dbd5-131">Du kan hämta ett **SchedulePolicy** -objekt med Get-AzureRmRecoveryServicesBackupSchedulePolicyObject-objektet.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-131">To obtain a **SchedulePolicy** object, use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd5-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9dbd5-132">-VaultId</span></span>
<span data-ttu-id="9dbd5-133">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9dbd5-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9dbd5-134">-Confirm</span></span>
<span data-ttu-id="9dbd5-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbd5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbd5-136">-WhatIf</span></span>
<span data-ttu-id="9dbd5-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dbd5-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbd5-139">CommonParameters</span></span>
<span data-ttu-id="9dbd5-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbd5-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbd5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbd5-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9dbd5-142">INPUTS</span></span>

### <span data-ttu-id="9dbd5-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="9dbd5-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>
<span data-ttu-id="9dbd5-144">Parametrar: princip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9dbd5-144">Parameters: Policy (ByValue)</span></span>

### <span data-ttu-id="9dbd5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9dbd5-145">System.String</span></span>
<span data-ttu-id="9dbd5-146">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9dbd5-146">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="9dbd5-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9dbd5-147">OUTPUTS</span></span>

### <span data-ttu-id="9dbd5-148">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9dbd5-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9dbd5-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9dbd5-149">NOTES</span></span>

## <span data-ttu-id="9dbd5-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9dbd5-150">RELATED LINKS</span></span>

[<span data-ttu-id="9dbd5-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-151">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="9dbd5-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="9dbd5-152">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="9dbd5-153">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-153">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="9dbd5-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd5-154">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


