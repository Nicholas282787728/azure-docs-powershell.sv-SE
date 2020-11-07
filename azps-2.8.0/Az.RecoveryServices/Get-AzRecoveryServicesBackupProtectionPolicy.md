---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 295cb5bad09584c16e1217e68d3fc80c5ebf8598
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919741"
---
# <span data-ttu-id="0647d-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0647d-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="0647d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0647d-102">SYNOPSIS</span></span>
<span data-ttu-id="0647d-103">Hämtar säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="0647d-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="0647d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0647d-104">SYNTAX</span></span>

### <span data-ttu-id="0647d-105">NoParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0647d-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0647d-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="0647d-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0647d-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="0647d-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0647d-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="0647d-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0647d-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0647d-109">DESCRIPTION</span></span>
<span data-ttu-id="0647d-110">Cmdleten **Get-AzRecoveryServicesBackupProtectionPolicy** hämtar Azure säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="0647d-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="0647d-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0647d-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0647d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0647d-112">EXAMPLES</span></span>

### <span data-ttu-id="0647d-113">Exempel 1: Hämta alla principer i valvet</span><span class="sxs-lookup"><span data-stu-id="0647d-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="0647d-114">Det här kommandot får alla skydds principer som skapats i valvet.</span><span class="sxs-lookup"><span data-stu-id="0647d-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="0647d-115">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="0647d-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="0647d-116">Det här kommandot får skydds principen med namnet DefaultPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="0647d-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="0647d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0647d-117">PARAMETERS</span></span>

### <span data-ttu-id="0647d-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0647d-118">-BackupManagementType</span></span>
<span data-ttu-id="0647d-119">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="0647d-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="0647d-120">För närvarande stöds endast AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="0647d-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0647d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0647d-121">-DefaultProfile</span></span>
<span data-ttu-id="0647d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0647d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0647d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0647d-123">-Name</span></span>
<span data-ttu-id="0647d-124">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="0647d-124">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0647d-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0647d-125">-VaultId</span></span>
<span data-ttu-id="0647d-126">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="0647d-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0647d-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0647d-127">-WorkloadType</span></span>
<span data-ttu-id="0647d-128">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="0647d-128">Specifies the workload type.</span></span>
<span data-ttu-id="0647d-129">För närvarande stöds endast AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="0647d-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0647d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0647d-130">CommonParameters</span></span>
<span data-ttu-id="0647d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0647d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0647d-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0647d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0647d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0647d-133">INPUTS</span></span>

### <span data-ttu-id="0647d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0647d-134">System.String</span></span>

## <span data-ttu-id="0647d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0647d-135">OUTPUTS</span></span>

### <span data-ttu-id="0647d-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="0647d-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="0647d-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0647d-137">NOTES</span></span>

## <span data-ttu-id="0647d-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0647d-138">RELATED LINKS</span></span>

[<span data-ttu-id="0647d-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0647d-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0647d-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0647d-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="0647d-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0647d-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


