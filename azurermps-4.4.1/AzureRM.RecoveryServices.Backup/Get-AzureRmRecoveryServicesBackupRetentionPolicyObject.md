---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 5fd705d38f2deb232c9b62861804eb2830f45999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757759"
---
# <span data-ttu-id="b6751-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b6751-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="b6751-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6751-102">SYNOPSIS</span></span>
<span data-ttu-id="b6751-103">Hämtar ett grundläggande bevarande princip objekt.</span><span class="sxs-lookup"><span data-stu-id="b6751-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6751-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6751-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6751-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6751-105">DESCRIPTION</span></span>
<span data-ttu-id="b6751-106">Cmdleten **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** får en bas **AzureRMRecoveryServicesRetentionPolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="b6751-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="b6751-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="b6751-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="b6751-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="b6751-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="b6751-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6751-109">EXAMPLES</span></span>

### <span data-ttu-id="b6751-110">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="b6751-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b6751-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="b6751-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="b6751-112">Med det andra kommandot anges längden för bevarande princip objekt till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="b6751-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="b6751-113">Det tredje kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="b6751-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="b6751-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med principen för bevarande princip och schema princip som skapats med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="b6751-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="b6751-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6751-115">PARAMETERS</span></span>

### <span data-ttu-id="b6751-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b6751-116">-BackupManagementType</span></span>
<span data-ttu-id="b6751-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="b6751-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="b6751-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b6751-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6751-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b6751-119">AzureVM</span></span> 
- <span data-ttu-id="b6751-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b6751-120">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6751-121">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b6751-121">-WorkloadType</span></span>
<span data-ttu-id="b6751-122">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="b6751-122">Specifies the workload type.</span></span>
<span data-ttu-id="b6751-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b6751-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6751-124">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b6751-124">AzureVM</span></span> 
- <span data-ttu-id="b6751-125">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b6751-125">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6751-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6751-126">-DefaultProfile</span></span>
<span data-ttu-id="b6751-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6751-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6751-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6751-128">CommonParameters</span></span>
<span data-ttu-id="b6751-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6751-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6751-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6751-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6751-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6751-131">INPUTS</span></span>

## <span data-ttu-id="b6751-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6751-132">OUTPUTS</span></span>

### <span data-ttu-id="b6751-133">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="b6751-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="b6751-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6751-134">NOTES</span></span>

## <span data-ttu-id="b6751-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6751-135">RELATED LINKS</span></span>

[<span data-ttu-id="b6751-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b6751-136">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="b6751-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b6751-137">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

