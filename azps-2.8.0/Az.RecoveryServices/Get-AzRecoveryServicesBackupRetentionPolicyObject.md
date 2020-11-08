---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: b3a1c990f8dff3b91c9e46fd1f01da734e47f963
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919736"
---
# <span data-ttu-id="d9724-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d9724-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="d9724-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9724-102">SYNOPSIS</span></span>
<span data-ttu-id="d9724-103">Hämtar ett grundläggande bevarande princip objekt.</span><span class="sxs-lookup"><span data-stu-id="d9724-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="d9724-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9724-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9724-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9724-105">DESCRIPTION</span></span>
<span data-ttu-id="d9724-106">Cmdleten **Get-AzRecoveryServicesBackupRetentionPolicyObject** får en bas **AzureRMRecoveryServicesRetentionPolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="d9724-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="d9724-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="d9724-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="d9724-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="d9724-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="d9724-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9724-109">EXAMPLES</span></span>

### <span data-ttu-id="d9724-110">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="d9724-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="d9724-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="d9724-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="d9724-112">Med det andra kommandot anges längden för bevarande princip objekt till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="d9724-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="d9724-113">Det tredje kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="d9724-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="d9724-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med principen för bevarande princip och schema princip som skapats med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="d9724-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="d9724-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9724-115">PARAMETERS</span></span>

### <span data-ttu-id="d9724-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d9724-116">-BackupManagementType</span></span>
<span data-ttu-id="d9724-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="d9724-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="d9724-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d9724-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9724-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d9724-119">AzureVM</span></span> 
- <span data-ttu-id="d9724-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d9724-120">AzureSQLDatabase</span></span>
- <span data-ttu-id="d9724-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d9724-121">AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9724-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9724-122">-DefaultProfile</span></span>
<span data-ttu-id="d9724-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9724-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9724-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d9724-124">-WorkloadType</span></span>
<span data-ttu-id="d9724-125">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="d9724-125">Specifies the workload type.</span></span>
<span data-ttu-id="d9724-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d9724-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9724-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d9724-127">AzureVM</span></span> 
- <span data-ttu-id="d9724-128">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d9724-128">AzureSQLDatabase</span></span>
- <span data-ttu-id="d9724-129">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d9724-129">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9724-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9724-130">CommonParameters</span></span>
<span data-ttu-id="d9724-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9724-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9724-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9724-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9724-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9724-133">INPUTS</span></span>

### <span data-ttu-id="d9724-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="d9724-134">None</span></span>

## <span data-ttu-id="d9724-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9724-135">OUTPUTS</span></span>

### <span data-ttu-id="d9724-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="d9724-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="d9724-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9724-137">NOTES</span></span>

## <span data-ttu-id="d9724-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9724-138">RELATED LINKS</span></span>

[<span data-ttu-id="d9724-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="d9724-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="d9724-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9724-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

