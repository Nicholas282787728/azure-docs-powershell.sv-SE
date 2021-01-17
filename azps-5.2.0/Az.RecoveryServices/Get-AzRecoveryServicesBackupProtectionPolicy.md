---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 9595f3fc3062d6afdd5b5bbfab74f297b39b3f6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415416"
---
# <span data-ttu-id="29c69-101">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29c69-101">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="29c69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29c69-102">SYNOPSIS</span></span>
<span data-ttu-id="29c69-103">Hämtar säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="29c69-103">Gets Backup protection policies for a vault.</span></span>

## <span data-ttu-id="29c69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29c69-104">SYNTAX</span></span>

### <span data-ttu-id="29c69-105">NoParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="29c69-105">NoParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29c69-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="29c69-106">PolicyNameParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c69-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="29c69-107">WorkloadParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29c69-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="29c69-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29c69-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29c69-109">DESCRIPTION</span></span>
<span data-ttu-id="29c69-110">Cmdleten **Get-AzRecoveryServicesBackupProtectionPolicy** hämtar Azure säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="29c69-110">The **Get-AzRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="29c69-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29c69-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="29c69-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29c69-112">EXAMPLES</span></span>

### <span data-ttu-id="29c69-113">Exempel 1: Hämta alla principer i valvet</span><span class="sxs-lookup"><span data-stu-id="29c69-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="29c69-114">Det här kommandot får alla skydds principer som skapats i valvet.</span><span class="sxs-lookup"><span data-stu-id="29c69-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="29c69-115">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="29c69-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="29c69-116">Det här kommandot får skydds principen med namnet DefaultPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="29c69-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="29c69-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29c69-117">PARAMETERS</span></span>

### <span data-ttu-id="29c69-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="29c69-118">-BackupManagementType</span></span>
<span data-ttu-id="29c69-119">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="29c69-119">The class of resources being protected.</span></span> <span data-ttu-id="29c69-120">För närvarande är de värden som stöds för denna cmdlet AzureVM, AzureStorage, AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="29c69-120">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureStorage, AzureWorkload, MAB

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c69-121">-DefaultProfile</span></span>
<span data-ttu-id="29c69-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29c69-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c69-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="29c69-123">-Name</span></span>
<span data-ttu-id="29c69-124">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="29c69-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="29c69-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="29c69-125">-VaultId</span></span>
<span data-ttu-id="29c69-126">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="29c69-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="29c69-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="29c69-127">-WorkloadType</span></span>
<span data-ttu-id="29c69-128">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="29c69-128">Workload type of the resource.</span></span> <span data-ttu-id="29c69-129">De aktuella värdena är AzureVM, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="29c69-129">The current supported values are AzureVM, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="29c69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c69-130">CommonParameters</span></span>
<span data-ttu-id="29c69-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c69-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29c69-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c69-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29c69-133">INPUTS</span></span>

### <span data-ttu-id="29c69-134">System. String</span><span class="sxs-lookup"><span data-stu-id="29c69-134">System.String</span></span>

## <span data-ttu-id="29c69-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29c69-135">OUTPUTS</span></span>

### <span data-ttu-id="29c69-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="29c69-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="29c69-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29c69-137">NOTES</span></span>

## <span data-ttu-id="29c69-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29c69-138">RELATED LINKS</span></span>

[<span data-ttu-id="29c69-139">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29c69-139">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="29c69-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29c69-140">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="29c69-141">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29c69-141">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


