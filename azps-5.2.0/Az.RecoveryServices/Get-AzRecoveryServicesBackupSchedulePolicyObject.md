---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399208"
---
# <span data-ttu-id="96eb0-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="96eb0-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="96eb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="96eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="96eb0-103">Hämtar ett grundläggande schema objekt.</span><span class="sxs-lookup"><span data-stu-id="96eb0-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="96eb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="96eb0-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96eb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="96eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="96eb0-106">Cmdleten **Get-AzRecoveryServicesBackupSchedulePolicyObject** får en bas **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="96eb0-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="96eb0-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="96eb0-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="96eb0-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings skydds princip.</span><span class="sxs-lookup"><span data-stu-id="96eb0-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="96eb0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="96eb0-109">EXAMPLES</span></span>

### <span data-ttu-id="96eb0-110">Exempel 1: Ange schema frekvensen till varje vecka</span><span class="sxs-lookup"><span data-stu-id="96eb0-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="96eb0-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="96eb0-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="96eb0-112">Det andra kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="96eb0-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="96eb0-113">Det tredje kommandot ändrar frekvensen för schemaläggnings principen till varje vecka.</span><span class="sxs-lookup"><span data-stu-id="96eb0-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="96eb0-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med det uppdaterade schemat.</span><span class="sxs-lookup"><span data-stu-id="96eb0-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="96eb0-115">Exempel 2: Ange tid för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="96eb0-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="96eb0-116">Det första kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="96eb0-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="96eb0-117">Det andra kommandot tar bort alla schemalagda körnings tider från $SchPol.</span><span class="sxs-lookup"><span data-stu-id="96eb0-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="96eb0-118">Det tredje kommandot får dagens datum och tid och lagrar det sedan i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="96eb0-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="96eb0-119">Det fjärde kommandot ersätter de schemalagda kör tiderna med den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="96eb0-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="96eb0-120">Du kan bara säkerhetskopiera AzureVM en gång per dag, så för att återställa säkerhets kopierings tiden måste du ersätta det ursprungliga schemat.</span><span class="sxs-lookup"><span data-stu-id="96eb0-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="96eb0-121">Med det senaste kommandot skapas en säkerhets kopierings princip med det nya schemat.</span><span class="sxs-lookup"><span data-stu-id="96eb0-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="96eb0-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="96eb0-122">PARAMETERS</span></span>

### <span data-ttu-id="96eb0-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="96eb0-123">-BackupManagementType</span></span>
<span data-ttu-id="96eb0-124">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="96eb0-124">The class of resources being protected.</span></span> <span data-ttu-id="96eb0-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96eb0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96eb0-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="96eb0-126">AzureVM</span></span> 
- <span data-ttu-id="96eb0-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="96eb0-127">AzureStorage</span></span>
- <span data-ttu-id="96eb0-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="96eb0-128">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96eb0-129">-DefaultProfile</span></span>
<span data-ttu-id="96eb0-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="96eb0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96eb0-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="96eb0-131">-WorkloadType</span></span>
<span data-ttu-id="96eb0-132">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="96eb0-132">Workload type of the resource.</span></span> <span data-ttu-id="96eb0-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="96eb0-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96eb0-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="96eb0-134">AzureVM</span></span> 
- <span data-ttu-id="96eb0-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="96eb0-135">AzureFiles</span></span>
- <span data-ttu-id="96eb0-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="96eb0-136">MSSQL</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96eb0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96eb0-137">CommonParameters</span></span>
<span data-ttu-id="96eb0-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96eb0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96eb0-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96eb0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96eb0-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="96eb0-140">INPUTS</span></span>

### <span data-ttu-id="96eb0-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="96eb0-141">None</span></span>

## <span data-ttu-id="96eb0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="96eb0-142">OUTPUTS</span></span>

### <span data-ttu-id="96eb0-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="96eb0-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="96eb0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="96eb0-144">NOTES</span></span>

## <span data-ttu-id="96eb0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="96eb0-145">RELATED LINKS</span></span>

[<span data-ttu-id="96eb0-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96eb0-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="96eb0-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="96eb0-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


