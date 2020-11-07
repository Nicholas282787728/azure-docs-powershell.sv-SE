---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 2E202D0D-076D-431D-9338-9A84ABC0B461
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 3220ef801ff86a3fb95a4595efd8c94330bfcba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755378"
---
# <span data-ttu-id="debbc-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="debbc-101">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="debbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="debbc-102">SYNOPSIS</span></span>
<span data-ttu-id="debbc-103">Hämtar säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="debbc-103">Gets Backup protection policies for a vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="debbc-104">SYNTAX</span></span>

### <span data-ttu-id="debbc-105">NoParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="debbc-105">NoParamSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="debbc-106">PolicyNameParamSet</span><span class="sxs-lookup"><span data-stu-id="debbc-106">PolicyNameParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="debbc-107">WorkloadParamSet</span><span class="sxs-lookup"><span data-stu-id="debbc-107">WorkloadParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="debbc-108">WorkloadBackupManagementTypeParamSet</span><span class="sxs-lookup"><span data-stu-id="debbc-108">WorkloadBackupManagementTypeParamSet</span></span>
```
Get-AzureRmRecoveryServicesBackupProtectionPolicy [-WorkloadType] <WorkloadType>
 [-BackupManagementType] <BackupManagementType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="debbc-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="debbc-109">DESCRIPTION</span></span>
<span data-ttu-id="debbc-110">Cmdleten **Get-AzureRmRecoveryServicesBackupProtectionPolicy** hämtar Azure säkerhets kopierings principer för ett valv.</span><span class="sxs-lookup"><span data-stu-id="debbc-110">The **Get-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet gets Azure Backup protection policies for a vault.</span></span>

<span data-ttu-id="debbc-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="debbc-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="debbc-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="debbc-112">EXAMPLES</span></span>

### <span data-ttu-id="debbc-113">Exempel 1: Hämta alla principer i valvet</span><span class="sxs-lookup"><span data-stu-id="debbc-113">Example 1: Get all policies in the vault</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProtectionPolicy 
Name                 WorkloadType       BackupManagementType BackupTime                DaysOfWeek   
----                 ------------       -------------------- ----------                ----------   
DefaultPolicy        AzureVM            AzureVM              4/14/2016 5:00:00 PM                   
NewPolicy            AzureVM            AzureVM              4/23/2016 5:30:00 PM                   
NewPolicy2           AzureVM            AzureVM              4/24/2016 1:30:00 AM
```

<span data-ttu-id="debbc-114">Det här kommandot får alla skydds principer som skapats i valvet.</span><span class="sxs-lookup"><span data-stu-id="debbc-114">This command gets all protection policies created in the vault.</span></span>

### <span data-ttu-id="debbc-115">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="debbc-115">Example 2: Get a specific policy</span></span>
```
PS C:\> $Pol= Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
```

<span data-ttu-id="debbc-116">Det här kommandot får skydds principen med namnet DefaultPolicy och lagrar den sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="debbc-116">This command gets the protection policy named DefaultPolicy, and then stores it in the $Pol variable.</span></span>

## <span data-ttu-id="debbc-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="debbc-117">PARAMETERS</span></span>

### <span data-ttu-id="debbc-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="debbc-118">-BackupManagementType</span></span>
<span data-ttu-id="debbc-119">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="debbc-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="debbc-120">För närvarande stöds endast AzureVM.</span><span class="sxs-lookup"><span data-stu-id="debbc-120">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debbc-121">-DefaultProfile</span></span>
<span data-ttu-id="debbc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="debbc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="debbc-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="debbc-123">-Name</span></span>
<span data-ttu-id="debbc-124">Anger namnet på policyn.</span><span class="sxs-lookup"><span data-stu-id="debbc-124">Specifies the name of the policy.</span></span>

```yaml
Type: String
Parameter Sets: PolicyNameParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debbc-125">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="debbc-125">-WorkloadType</span></span>
<span data-ttu-id="debbc-126">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="debbc-126">Specifies the workload type.</span></span>
<span data-ttu-id="debbc-127">För närvarande stöds endast AzureVM.</span><span class="sxs-lookup"><span data-stu-id="debbc-127">Currently, only AzureVM is supported.</span></span>

```yaml
Type: WorkloadType
Parameter Sets: WorkloadParamSet, WorkloadBackupManagementTypeParamSet
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debbc-128">CommonParameters</span></span>
<span data-ttu-id="debbc-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="debbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debbc-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debbc-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="debbc-131">INPUTS</span></span>

### <span data-ttu-id="debbc-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="debbc-132">None</span></span>
<span data-ttu-id="debbc-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="debbc-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="debbc-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="debbc-134">OUTPUTS</span></span>

### <span data-ttu-id="debbc-135">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="debbc-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="debbc-136">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. PolicyBase]</span><span class="sxs-lookup"><span data-stu-id="debbc-136">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase]</span></span>

## <span data-ttu-id="debbc-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="debbc-137">NOTES</span></span>

## <span data-ttu-id="debbc-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="debbc-138">RELATED LINKS</span></span>

[<span data-ttu-id="debbc-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="debbc-139">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="debbc-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="debbc-140">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="debbc-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="debbc-141">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


