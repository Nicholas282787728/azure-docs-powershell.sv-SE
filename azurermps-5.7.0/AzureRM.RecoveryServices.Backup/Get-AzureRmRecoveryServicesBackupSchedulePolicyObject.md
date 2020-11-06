---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 4a3602363436c396b0706d9c195569874a35fdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574223"
---
# <span data-ttu-id="42d83-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="42d83-101">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>

## <span data-ttu-id="42d83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42d83-102">SYNOPSIS</span></span>
<span data-ttu-id="42d83-103">Hämtar ett grundläggande schema objekt.</span><span class="sxs-lookup"><span data-stu-id="42d83-103">Gets a base schedule policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42d83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42d83-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42d83-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42d83-105">DESCRIPTION</span></span>
<span data-ttu-id="42d83-106">Cmdleten **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** får en bas **AzureRMRecoveryServicesSchedulePolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="42d83-106">The **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** cmdlet gets a base **AzureRMRecoveryServicesSchedulePolicyObject**.</span></span>
<span data-ttu-id="42d83-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="42d83-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="42d83-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings skydds princip.</span><span class="sxs-lookup"><span data-stu-id="42d83-108">It is temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup protection policy.</span></span>

## <span data-ttu-id="42d83-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42d83-109">EXAMPLES</span></span>

### <span data-ttu-id="42d83-110">Exempel 1: Ange schema frekvensen till varje vecka</span><span class="sxs-lookup"><span data-stu-id="42d83-110">Example 1: Set the schedule frequency to weekly</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="42d83-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="42d83-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="42d83-112">Det andra kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="42d83-112">The second command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="42d83-113">Det tredje kommandot ändrar frekvensen för schemaläggnings principen till varje vecka.</span><span class="sxs-lookup"><span data-stu-id="42d83-113">The third command changes the frequency for the schedule policy to weekly.</span></span>

<span data-ttu-id="42d83-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med det uppdaterade schemat.</span><span class="sxs-lookup"><span data-stu-id="42d83-114">The last command creates a backup protection policy with the updated schedule.</span></span>

### <span data-ttu-id="42d83-115">Exempel 2: Ange tid för säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="42d83-115">Example 2: Set the backup time</span></span>
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="42d83-116">Det första kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="42d83-116">The first command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="42d83-117">Det andra kommandot tar bort alla schemalagda körnings tider från $SchPol.</span><span class="sxs-lookup"><span data-stu-id="42d83-117">The second command removes all scheduled run times from $SchPol.</span></span>

<span data-ttu-id="42d83-118">Det tredje kommandot får dagens datum och tid och lagrar det sedan i $DT variabel.</span><span class="sxs-lookup"><span data-stu-id="42d83-118">The third command gets the current date and time, and then stores it in the $DT variable.</span></span>

<span data-ttu-id="42d83-119">Det fjärde kommandot ersätter de schemalagda kör tiderna med den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="42d83-119">The fourth command replaces the scheduled run times with the current time.</span></span>
<span data-ttu-id="42d83-120">Du kan bara säkerhetskopiera AzureVM en gång per dag, så för att återställa säkerhets kopierings tiden måste du ersätta det ursprungliga schemat.</span><span class="sxs-lookup"><span data-stu-id="42d83-120">You can only backup AzureVM once per day, so to reset the backup time you must replace the original schedule.</span></span>

<span data-ttu-id="42d83-121">Med det senaste kommandot skapas en säkerhets kopierings princip med det nya schemat.</span><span class="sxs-lookup"><span data-stu-id="42d83-121">The last command creates a backup protection policy using the new schedule.</span></span>

## <span data-ttu-id="42d83-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42d83-122">PARAMETERS</span></span>

### <span data-ttu-id="42d83-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="42d83-123">-BackupManagementType</span></span>
<span data-ttu-id="42d83-124">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="42d83-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="42d83-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42d83-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42d83-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="42d83-126">AzureVM</span></span> 
- <span data-ttu-id="42d83-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="42d83-127">AzureSQLDatabase</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d83-128">-DefaultProfile</span></span>
<span data-ttu-id="42d83-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42d83-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d83-130">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="42d83-130">-WorkloadType</span></span>
<span data-ttu-id="42d83-131">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="42d83-131">Specifies the workload type.</span></span>
<span data-ttu-id="42d83-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="42d83-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="42d83-133">AzureVM</span><span class="sxs-lookup"><span data-stu-id="42d83-133">AzureVM</span></span> 
- <span data-ttu-id="42d83-134">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="42d83-134">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d83-135">CommonParameters</span></span>
<span data-ttu-id="42d83-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d83-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d83-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d83-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42d83-138">INPUTS</span></span>

### <span data-ttu-id="42d83-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="42d83-139">None</span></span>
<span data-ttu-id="42d83-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="42d83-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42d83-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42d83-141">OUTPUTS</span></span>

### <span data-ttu-id="42d83-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="42d83-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

## <span data-ttu-id="42d83-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42d83-143">NOTES</span></span>

## <span data-ttu-id="42d83-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42d83-144">RELATED LINKS</span></span>

[<span data-ttu-id="42d83-145">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42d83-145">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="42d83-146">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42d83-146">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


