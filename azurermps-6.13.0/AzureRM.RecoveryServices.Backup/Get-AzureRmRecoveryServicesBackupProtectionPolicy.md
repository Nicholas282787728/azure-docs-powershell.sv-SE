---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: d08bd0a02878b1b99b3243e80512df30eca6e1c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576820"
---
# <span data-ttu-id="367d5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="367d5-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="367d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="367d5-102">SYNOPSIS</span></span>
<span data-ttu-id="367d5-103">Hämtar säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="367d5-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="367d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="367d5-104">SYNTAX</span></span>

### <span data-ttu-id="367d5-105">NoParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="367d5-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="367d5-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="367d5-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="367d5-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="367d5-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="367d5-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="367d5-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="367d5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="367d5-109">DESCRIPTION</span></span>
<span data-ttu-id="367d5-110">Cmdleten **Get-AzureRmRecoveryServicesBackupProtectionPolicy** hämtar Azure säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="367d5-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>
<span data-ttu-id="367d5-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="367d5-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="367d5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="367d5-112">EXAMPLES</span></span>

### <span data-ttu-id="367d5-113">Exempel 1: Hämta alla principer i valvet</span><span class="sxs-lookup"><span data-stu-id="367d5-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="367d5-114">Det här kommandot får alla skydds principer som skapats i valvet.</span><span class="sxs-lookup"><span data-stu-id="367d5-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="367d5-115">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="367d5-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="367d5-116">Det här kommandot får skydds principen med namnet DefaultPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="367d5-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="367d5-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="367d5-117">PARAMETERS</span></span>

### <span data-ttu-id="367d5-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="367d5-118">-BackupManagementType</span></span>
<span data-ttu-id="367d5-119">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="367d5-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="367d5-120">För närvarande stöds endast AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="367d5-120">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367d5-121">-DefaultProfile</span></span>
<span data-ttu-id="367d5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="367d5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="367d5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="367d5-123">-Name</span></span>
<span data-ttu-id="367d5-124">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="367d5-124">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="367d5-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="367d5-125">-VaultId</span></span>
<span data-ttu-id="367d5-126">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="367d5-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="367d5-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="367d5-127">-WorkloadType</span></span>
<span data-ttu-id="367d5-128">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="367d5-128">Specifies the workload type.</span></span>
<span data-ttu-id="367d5-129">För närvarande stöds endast AzureVM, AzureFiles.</span><span class="sxs-lookup"><span data-stu-id="367d5-129">Currently, only AzureVM, AzureFiles is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType]
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367d5-130">CommonParameters</span></span>
<span data-ttu-id="367d5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="367d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367d5-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367d5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="367d5-133">INPUTS</span></span>

### <span data-ttu-id="367d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="367d5-134">System.String</span></span>
<span data-ttu-id="367d5-135">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="367d5-135">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="367d5-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="367d5-136">OUTPUTS</span></span>

### <span data-ttu-id="367d5-137">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="367d5-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="367d5-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="367d5-138">NOTES</span></span>

## <span data-ttu-id="367d5-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="367d5-139">RELATED LINKS</span></span>

[<span data-ttu-id="367d5-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="367d5-140">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="367d5-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="367d5-141">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="367d5-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="367d5-142">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


