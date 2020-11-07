---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757046"
---
# <span data-ttu-id="90ce2-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="90ce2-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="90ce2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="90ce2-103">Hämtar objekten från en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="90ce2-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90ce2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90ce2-104">SYNTAX</span></span>

### <span data-ttu-id="90ce2-105">GetItemsForContainer (standard)</span><span class="sxs-lookup"><span data-stu-id="90ce2-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90ce2-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="90ce2-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90ce2-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="90ce2-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90ce2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="90ce2-109">Cmdleten **Get-AzureRmRecoveryServicesBackupItem** hämtar objekten i en container eller ett värde i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="90ce2-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="90ce2-110">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="90ce2-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="90ce2-111">För virtuella Azure-datorer kan det bara finnas ett säkerhets kopie objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="90ce2-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="90ce2-112">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90ce2-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="90ce2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90ce2-113">EXAMPLES</span></span>

### <span data-ttu-id="90ce2-114">Exempel 1: Hämta ett objekt från en säkerhets kopia av en behållare</span><span class="sxs-lookup"><span data-stu-id="90ce2-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="90ce2-115">Det första kommandot får behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="90ce2-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="90ce2-116">Det andra kommandot får det säkerhets kopie objekt som heter V2VM i $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="90ce2-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="90ce2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90ce2-117">PARAMETERS</span></span>

### <span data-ttu-id="90ce2-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="90ce2-118">-BackupManagementType</span></span>
<span data-ttu-id="90ce2-119">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="90ce2-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="90ce2-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="90ce2-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90ce2-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="90ce2-121">AzureVM</span></span> 
- <span data-ttu-id="90ce2-122">OM</span><span class="sxs-lookup"><span data-stu-id="90ce2-122">MARS</span></span> 
- <span data-ttu-id="90ce2-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="90ce2-123">SCDPM</span></span> 
- <span data-ttu-id="90ce2-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="90ce2-124">AzureBackupServer</span></span> 
- <span data-ttu-id="90ce2-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="90ce2-125">AzureSQL</span></span>
- <span data-ttu-id="90ce2-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="90ce2-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-127">-Container</span><span class="sxs-lookup"><span data-stu-id="90ce2-127">-Container</span></span>
<span data-ttu-id="90ce2-128">Anger ett Container-objekt som den här cmdleten ska säkerhetskopiera objekt från.</span><span class="sxs-lookup"><span data-stu-id="90ce2-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="90ce2-129">För att få en **AzureRmRecoveryServicesBackupContainer** , Använd cmdleten Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="90ce2-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ce2-130">-DefaultProfile</span></span>
<span data-ttu-id="90ce2-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90ce2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90ce2-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="90ce2-132">-Name</span></span>
<span data-ttu-id="90ce2-133">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="90ce2-133">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-134">-Princip</span><span class="sxs-lookup"><span data-stu-id="90ce2-134">-Policy</span></span>
<span data-ttu-id="90ce2-135">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="90ce2-135">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="90ce2-136">-ProtectionState</span></span>
<span data-ttu-id="90ce2-137">Anger skydds tillståndet.</span><span class="sxs-lookup"><span data-stu-id="90ce2-137">Specifies the state of protection.</span></span>
<span data-ttu-id="90ce2-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="90ce2-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90ce2-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="90ce2-139">IRPending.</span></span>
<span data-ttu-id="90ce2-140">Den första synkroniseringen har inte påbörjats och det finns ingen återställnings punkt ännu.</span><span class="sxs-lookup"><span data-stu-id="90ce2-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="90ce2-141">Upphovsrättsskydd.</span><span class="sxs-lookup"><span data-stu-id="90ce2-141">Protected.</span></span>
<span data-ttu-id="90ce2-142">Skyddet pågår.</span><span class="sxs-lookup"><span data-stu-id="90ce2-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="90ce2-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="90ce2-143">ProtectionError.</span></span>
<span data-ttu-id="90ce2-144">Ett skydds fel har uppstått.</span><span class="sxs-lookup"><span data-stu-id="90ce2-144">There is a protection error.</span></span>
- <span data-ttu-id="90ce2-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="90ce2-145">ProtectionStopped.</span></span>
<span data-ttu-id="90ce2-146">Skyddet är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="90ce2-146">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="90ce2-147">-ProtectionStatus</span></span>
<span data-ttu-id="90ce2-148">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="90ce2-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="90ce2-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="90ce2-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90ce2-150">Sund</span><span class="sxs-lookup"><span data-stu-id="90ce2-150">Healthy</span></span>
- <span data-ttu-id="90ce2-151">Ohälsosamt</span><span class="sxs-lookup"><span data-stu-id="90ce2-151">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="90ce2-152">-VaultId</span></span>
<span data-ttu-id="90ce2-153">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="90ce2-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="90ce2-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="90ce2-154">-WorkloadType</span></span>
<span data-ttu-id="90ce2-155">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="90ce2-155">Specifies the workload type.</span></span> <span data-ttu-id="90ce2-156">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="90ce2-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90ce2-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="90ce2-157">AzureVM</span></span> 
- <span data-ttu-id="90ce2-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="90ce2-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="90ce2-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="90ce2-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90ce2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ce2-160">CommonParameters</span></span>
<span data-ttu-id="90ce2-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ce2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ce2-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90ce2-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ce2-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90ce2-163">INPUTS</span></span>

### <span data-ttu-id="90ce2-164">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="90ce2-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="90ce2-165">System. String</span><span class="sxs-lookup"><span data-stu-id="90ce2-165">System.String</span></span>
<span data-ttu-id="90ce2-166">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="90ce2-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="90ce2-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90ce2-167">OUTPUTS</span></span>

### <span data-ttu-id="90ce2-168">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="90ce2-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="90ce2-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90ce2-169">NOTES</span></span>

## <span data-ttu-id="90ce2-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90ce2-170">RELATED LINKS</span></span>

[<span data-ttu-id="90ce2-171">Säkerhets kopiering-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="90ce2-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="90ce2-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="90ce2-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="90ce2-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="90ce2-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="90ce2-174">Återställ-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="90ce2-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


