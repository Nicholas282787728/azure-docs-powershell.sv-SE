---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: 83ed9062c5ad4beb0dff9c9c89b79a443cc68a52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574226"
---
# <span data-ttu-id="e84d9-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e84d9-101">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="e84d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e84d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e84d9-103">Hämtar ett grundläggande bevarande princip objekt.</span><span class="sxs-lookup"><span data-stu-id="e84d9-103">Gets a base retention policy object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e84d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e84d9-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e84d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e84d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e84d9-106">Cmdleten **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** får en bas **AzureRMRecoveryServicesRetentionPolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="e84d9-106">The **Get-AzureRmRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="e84d9-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="e84d9-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="e84d9-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="e84d9-108">It is a temporary object that you can manipulate and use with the New-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="e84d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e84d9-109">EXAMPLES</span></span>

### <span data-ttu-id="e84d9-110">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="e84d9-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e84d9-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="e84d9-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="e84d9-112">Med det andra kommandot anges längden för bevarande princip objekt till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="e84d9-112">The second command sets the duration for the retention policy object to 365 days.</span></span>

<span data-ttu-id="e84d9-113">Det tredje kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="e84d9-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="e84d9-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med principen för bevarande princip och schema princip som skapats med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="e84d9-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="e84d9-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e84d9-115">PARAMETERS</span></span>

### <span data-ttu-id="e84d9-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e84d9-116">-BackupManagementType</span></span>
<span data-ttu-id="e84d9-117">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="e84d9-117">Specifies the Backup management type.</span></span>
<span data-ttu-id="e84d9-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e84d9-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e84d9-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e84d9-119">AzureVM</span></span> 
- <span data-ttu-id="e84d9-120">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e84d9-120">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="e84d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e84d9-121">-DefaultProfile</span></span>
<span data-ttu-id="e84d9-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e84d9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e84d9-123">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e84d9-123">-WorkloadType</span></span>
<span data-ttu-id="e84d9-124">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="e84d9-124">Specifies the workload type.</span></span>
<span data-ttu-id="e84d9-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e84d9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e84d9-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e84d9-126">AzureVM</span></span> 
- <span data-ttu-id="e84d9-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="e84d9-127">AzureSQLDatabase</span></span>

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

### <span data-ttu-id="e84d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e84d9-128">CommonParameters</span></span>
<span data-ttu-id="e84d9-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e84d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e84d9-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e84d9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e84d9-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e84d9-131">INPUTS</span></span>

### <span data-ttu-id="e84d9-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="e84d9-132">None</span></span>
<span data-ttu-id="e84d9-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e84d9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e84d9-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e84d9-134">OUTPUTS</span></span>

### <span data-ttu-id="e84d9-135">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="e84d9-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="e84d9-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e84d9-136">NOTES</span></span>

## <span data-ttu-id="e84d9-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e84d9-137">RELATED LINKS</span></span>

[<span data-ttu-id="e84d9-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e84d9-138">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="e84d9-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e84d9-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)


