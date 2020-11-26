---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: d66b8515c6b2c3782c6f6c2b49d462dbb7bd1660
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263433"
---
# <span data-ttu-id="25d30-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="25d30-101">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="25d30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25d30-102">SYNOPSIS</span></span>
<span data-ttu-id="25d30-103">Hämtar ett grundläggande schema objekt.</span><span class="sxs-lookup"><span data-stu-id="25d30-103">Gets a base schedule policy object.</span></span>

## <span data-ttu-id="25d30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25d30-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25d30-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25d30-105">DESCRIPTION</span></span>
<span data-ttu-id="25d30-106">Cmdleten **Get-AzRecoveryServicesBackupSchedulePolicyObject** får en bas **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="25d30-106">The **Get-AzRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="25d30-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="25d30-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="25d30-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings skydds princip.</span><span class="sxs-lookup"><span data-stu-id="25d30-108">It is temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="25d30-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25d30-109">EXAMPLES</span></span>

### <span data-ttu-id="25d30-110">Exempel 1: Ange schema frekvensen till varje vecka</span><span class="sxs-lookup"><span data-stu-id="25d30-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="25d30-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="25d30-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="25d30-112">Det andra kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="25d30-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="25d30-113">Det tredje kommandot ändrar frekvensen för schemaläggnings principen till varje vecka.</span><span class="sxs-lookup"><span data-stu-id="25d30-113">The third command changes the frequency for the schedule policy to weekly.</span></span>
<span data-ttu-id="25d30-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med det uppdaterade schemat.</span><span class="sxs-lookup"><span data-stu-id="25d30-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="25d30-115">Exempel 2: Ange tid för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="25d30-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="25d30-116">Det första kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="25d30-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="25d30-117">Det andra kommandot tar bort alla schemalagda körnings tider från $SchPol.</span><span class="sxs-lookup"><span data-stu-id="25d30-117">The second command removes all scheduled run times from $SchPol.</span></span>
<span data-ttu-id="25d30-118">Det tredje kommandot får dagens datum och tid och lagrar det sedan i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="25d30-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>
<span data-ttu-id="25d30-119">Det fjärde kommandot ersätter de schemalagda kör tiderna med den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="25d30-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="25d30-120">Du kan bara säkerhetskopiera AzureVM en gång per dag, så för att återställa säkerhets kopierings tiden måste du ersätta det ursprungliga schemat.</span><span class="sxs-lookup"><span data-stu-id="25d30-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>
<span data-ttu-id="25d30-121">Med det senaste kommandot skapas en säkerhets kopierings princip med det nya schemat.</span><span class="sxs-lookup"><span data-stu-id="25d30-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="25d30-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25d30-122">PARAMETERS</span></span>

### <span data-ttu-id="25d30-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="25d30-123">-BackupManagementType</span></span>
<span data-ttu-id="25d30-124">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="25d30-124">The class of resources being protected.</span></span> <span data-ttu-id="25d30-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25d30-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25d30-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="25d30-126">AzureVM</span></span> 
- <span data-ttu-id="25d30-127">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="25d30-127">AzureStorage</span></span>
- <span data-ttu-id="25d30-128">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="25d30-128">AzureWorkload</span></span>

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

### <span data-ttu-id="25d30-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d30-129">-DefaultProfile</span></span>
<span data-ttu-id="25d30-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25d30-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d30-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="25d30-131">-WorkloadType</span></span>
<span data-ttu-id="25d30-132">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="25d30-132">Workload type of the resource.</span></span> <span data-ttu-id="25d30-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="25d30-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25d30-134">AzureVM</span><span class="sxs-lookup"><span data-stu-id="25d30-134">AzureVM</span></span> 
- <span data-ttu-id="25d30-135">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="25d30-135">AzureFiles</span></span>
- <span data-ttu-id="25d30-136">MSSQL</span><span class="sxs-lookup"><span data-stu-id="25d30-136">MSSQL</span></span>


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

### <span data-ttu-id="25d30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d30-137">CommonParameters</span></span>
<span data-ttu-id="25d30-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d30-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25d30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d30-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25d30-140">INPUTS</span></span>

### <span data-ttu-id="25d30-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="25d30-141">None</span></span>

## <span data-ttu-id="25d30-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25d30-142">OUTPUTS</span></span>

### <span data-ttu-id="25d30-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="25d30-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="25d30-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25d30-144">NOTES</span></span>

## <span data-ttu-id="25d30-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25d30-145">RELATED LINKS</span></span>

[<span data-ttu-id="25d30-146">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25d30-146">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="25d30-147">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25d30-147">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

