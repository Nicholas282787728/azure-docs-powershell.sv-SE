---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 476094CC-A320-4B2D-B53D-6BFFE30C76CC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRetentionPolicyObject.md
ms.openlocfilehash: d426cd18aaf3382939e55668b1c19938319a3c51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261087"
---
# <span data-ttu-id="832fa-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="832fa-101">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="832fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="832fa-102">SYNOPSIS</span></span>
<span data-ttu-id="832fa-103">Hämtar ett grundläggande bevarande princip objekt.</span><span class="sxs-lookup"><span data-stu-id="832fa-103">Gets a base retention policy object.</span></span>

## <span data-ttu-id="832fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="832fa-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRetentionPolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="832fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="832fa-105">DESCRIPTION</span></span>
<span data-ttu-id="832fa-106">Cmdleten **Get-AzRecoveryServicesBackupRetentionPolicyObject** får en bas **AzureRMRecoveryServicesRetentionPolicyObject**.</span><span class="sxs-lookup"><span data-stu-id="832fa-106">The **Get-AzRecoveryServicesBackupRetentionPolicyObject** cmdlet gets a base **AzureRMRecoveryServicesRetentionPolicyObject**.</span></span>
<span data-ttu-id="832fa-107">Det här objektet bevaras inte i systemet.</span><span class="sxs-lookup"><span data-stu-id="832fa-107">This object is not persisted in the system.</span></span>
<span data-ttu-id="832fa-108">Det är ett tillfälligt objekt som du kan ändra och använda med New-AzRecoveryServicesBackupProtectionPolicy cmdlet för att skapa en ny säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="832fa-108">It is a temporary object that you can manipulate and use with the New-AzRecoveryServicesBackupProtectionPolicy cmdlet to create a new backup policy.</span></span>

## <span data-ttu-id="832fa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="832fa-109">EXAMPLES</span></span>

### <span data-ttu-id="832fa-110">Exempel 1: skapa en säkerhets kopierings princip</span><span class="sxs-lookup"><span data-stu-id="832fa-110">Example 1: Create a backup protection policy</span></span>
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType AzureVM 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType AzureVM 
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="832fa-111">Det första kommandot hämtar bevarande princip objekt och lagrar det sedan i $RetPol variabel.</span><span class="sxs-lookup"><span data-stu-id="832fa-111">The first command gets the retention policy object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="832fa-112">Med det andra kommandot anges längden för bevarande princip objekt till 365 dagar.</span><span class="sxs-lookup"><span data-stu-id="832fa-112">The second command sets the duration for the retention policy object to 365 days.</span></span>
<span data-ttu-id="832fa-113">Det tredje kommandot hämtar schemaobjektet och lagrar det sedan i $SchPol variabel.</span><span class="sxs-lookup"><span data-stu-id="832fa-113">The third command gets the schedule policy object, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="832fa-114">Med det senaste kommandot skapas en säkerhets kopierings skydds princip med principen för bevarande princip och schema princip som skapats med föregående kommandon.</span><span class="sxs-lookup"><span data-stu-id="832fa-114">The last command creates a backup protection policy using the retention policy and schedule policy created with the previous commands.</span></span>

## <span data-ttu-id="832fa-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="832fa-115">PARAMETERS</span></span>

### <span data-ttu-id="832fa-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="832fa-116">-BackupManagementType</span></span>
<span data-ttu-id="832fa-117">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="832fa-117">The class of resources being protected.</span></span> <span data-ttu-id="832fa-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="832fa-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="832fa-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="832fa-119">AzureVM</span></span> 
- <span data-ttu-id="832fa-120">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="832fa-120">AzureWorkload</span></span>
- <span data-ttu-id="832fa-121">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="832fa-121">AzureStorage</span></span>

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

### <span data-ttu-id="832fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="832fa-122">-DefaultProfile</span></span>
<span data-ttu-id="832fa-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="832fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="832fa-124">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="832fa-124">-WorkloadType</span></span>
<span data-ttu-id="832fa-125">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="832fa-125">Workload type of the resource.</span></span> <span data-ttu-id="832fa-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="832fa-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="832fa-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="832fa-127">AzureVM</span></span> 
- <span data-ttu-id="832fa-128">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="832fa-128">AzureFiles</span></span>
- <span data-ttu-id="832fa-129">MSSQL</span><span class="sxs-lookup"><span data-stu-id="832fa-129">MSSQL</span></span>

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

### <span data-ttu-id="832fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="832fa-130">CommonParameters</span></span>
<span data-ttu-id="832fa-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="832fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="832fa-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="832fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="832fa-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="832fa-133">INPUTS</span></span>

### <span data-ttu-id="832fa-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="832fa-134">None</span></span>

## <span data-ttu-id="832fa-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="832fa-135">OUTPUTS</span></span>

### <span data-ttu-id="832fa-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="832fa-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

## <span data-ttu-id="832fa-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="832fa-137">NOTES</span></span>

## <span data-ttu-id="832fa-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="832fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="832fa-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="832fa-139">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="832fa-140">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="832fa-140">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

