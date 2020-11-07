---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757764"
---
# <span data-ttu-id="4526d-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4526d-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4526d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4526d-102">SYNOPSIS</span></span>
<span data-ttu-id="4526d-103">Hämtar objekten från en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="4526d-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4526d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4526d-104">SYNTAX</span></span>

### <span data-ttu-id="4526d-105">GetItemsForContainer (standard)</span><span class="sxs-lookup"><span data-stu-id="4526d-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4526d-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="4526d-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4526d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4526d-107">DESCRIPTION</span></span>
<span data-ttu-id="4526d-108">Cmdleten **Get-AzureRmRecoveryServicesBackupItem** hämtar objekten i en container eller ett värde i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="4526d-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="4526d-109">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="4526d-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="4526d-110">För virtuella Azure-datorer kan det bara finnas ett säkerhets kopie objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4526d-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="4526d-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4526d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4526d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4526d-112">EXAMPLES</span></span>

### <span data-ttu-id="4526d-113">Exempel 1: Hämta ett objekt från en säkerhets kopia av en behållare</span><span class="sxs-lookup"><span data-stu-id="4526d-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="4526d-114">Det första kommandot får behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="4526d-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="4526d-115">Det andra kommandot får det säkerhets kopie objekt som heter V2VM i $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="4526d-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="4526d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4526d-116">PARAMETERS</span></span>

### <span data-ttu-id="4526d-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4526d-117">-BackupManagementType</span></span>
<span data-ttu-id="4526d-118">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="4526d-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="4526d-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4526d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4526d-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4526d-120">AzureVM</span></span> 
- <span data-ttu-id="4526d-121">OM</span><span class="sxs-lookup"><span data-stu-id="4526d-121">MARS</span></span> 
- <span data-ttu-id="4526d-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="4526d-122">SCDPM</span></span> 
- <span data-ttu-id="4526d-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="4526d-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4526d-124">-Container</span><span class="sxs-lookup"><span data-stu-id="4526d-124">-Container</span></span>
<span data-ttu-id="4526d-125">Anger ett Container-objekt som den här cmdleten ska säkerhetskopiera objekt från.</span><span class="sxs-lookup"><span data-stu-id="4526d-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="4526d-126">För att få en **AzureRmRecoveryServicesBackupContainer** , Använd cmdleten Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="4526d-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="4526d-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="4526d-127">-Name</span></span>
<span data-ttu-id="4526d-128">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="4526d-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="4526d-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="4526d-129">-ProtectionState</span></span>
<span data-ttu-id="4526d-130">Anger skydds tillståndet.</span><span class="sxs-lookup"><span data-stu-id="4526d-130">Specifies the state of protection.</span></span>
<span data-ttu-id="4526d-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4526d-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4526d-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="4526d-132">IRPending.</span></span>
<span data-ttu-id="4526d-133">Den första synkroniseringen har inte påbörjats och det finns ingen återställnings punkt ännu.</span><span class="sxs-lookup"><span data-stu-id="4526d-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="4526d-134">Upphovsrättsskydd.</span><span class="sxs-lookup"><span data-stu-id="4526d-134">Protected.</span></span>
<span data-ttu-id="4526d-135">Skyddet pågår.</span><span class="sxs-lookup"><span data-stu-id="4526d-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="4526d-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="4526d-136">ProtectionError.</span></span>
<span data-ttu-id="4526d-137">Ett skydds fel har uppstått.</span><span class="sxs-lookup"><span data-stu-id="4526d-137">There is a protection error.</span></span>
- <span data-ttu-id="4526d-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="4526d-138">ProtectionStopped.</span></span>
<span data-ttu-id="4526d-139">Skyddet är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="4526d-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="4526d-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="4526d-140">-ProtectionStatus</span></span>
<span data-ttu-id="4526d-141">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="4526d-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="4526d-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4526d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4526d-143">Sund</span><span class="sxs-lookup"><span data-stu-id="4526d-143">Healthy</span></span>
- <span data-ttu-id="4526d-144">Ohälsosamt</span><span class="sxs-lookup"><span data-stu-id="4526d-144">Unhealthy</span></span>

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

### <span data-ttu-id="4526d-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="4526d-145">-WorkloadType</span></span>
<span data-ttu-id="4526d-146">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="4526d-146">Specifies the workload type.</span></span> <span data-ttu-id="4526d-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4526d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4526d-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4526d-148">AzureVM</span></span> 
- <span data-ttu-id="4526d-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="4526d-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4526d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4526d-150">-DefaultProfile</span></span>
<span data-ttu-id="4526d-151">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4526d-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4526d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4526d-152">CommonParameters</span></span>
<span data-ttu-id="4526d-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4526d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4526d-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4526d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4526d-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4526d-155">INPUTS</span></span>

## <span data-ttu-id="4526d-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4526d-156">OUTPUTS</span></span>

### <span data-ttu-id="4526d-157">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="4526d-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="4526d-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="4526d-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="4526d-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4526d-159">NOTES</span></span>

## <span data-ttu-id="4526d-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4526d-160">RELATED LINKS</span></span>

[<span data-ttu-id="4526d-161">Säkerhets kopiering-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4526d-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="4526d-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4526d-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4526d-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4526d-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="4526d-164">Återställ-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4526d-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


