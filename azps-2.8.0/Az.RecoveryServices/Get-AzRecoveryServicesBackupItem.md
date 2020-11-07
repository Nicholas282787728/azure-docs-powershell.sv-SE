---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919756"
---
# <span data-ttu-id="91ff4-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91ff4-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="91ff4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91ff4-102">SYNOPSIS</span></span>

<span data-ttu-id="91ff4-103">Hämtar objekten från en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="91ff4-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="91ff4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91ff4-104">SYNTAX</span></span>

### <span data-ttu-id="91ff4-105">GetItemsForContainer (standard)</span><span class="sxs-lookup"><span data-stu-id="91ff4-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91ff4-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="91ff4-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91ff4-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="91ff4-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ff4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91ff4-108">DESCRIPTION</span></span>

<span data-ttu-id="91ff4-109">Cmdleten **Get-AzRecoveryServicesBackupItem** hämtar objekten i en container eller ett värde i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="91ff4-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="91ff4-110">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="91ff4-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="91ff4-111">För virtuella Azure-datorer kan det bara finnas ett säkerhets kopie objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="91ff4-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="91ff4-112">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="91ff4-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="91ff4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91ff4-113">EXAMPLES</span></span>

### <span data-ttu-id="91ff4-114">Exempel 1: Hämta ett objekt från en säkerhets kopia av en behållare</span><span class="sxs-lookup"><span data-stu-id="91ff4-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="91ff4-115">Det första kommandot får behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="91ff4-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="91ff4-116">Det andra kommandot får det säkerhets kopie objekt som heter V2VM i $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="91ff4-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="91ff4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91ff4-117">PARAMETERS</span></span>

### <span data-ttu-id="91ff4-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="91ff4-118">-BackupManagementType</span></span>

<span data-ttu-id="91ff4-119">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="91ff4-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="91ff4-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91ff4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ff4-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="91ff4-121">AzureVM</span></span>
- <span data-ttu-id="91ff4-122">OM</span><span class="sxs-lookup"><span data-stu-id="91ff4-122">MARS</span></span>
- <span data-ttu-id="91ff4-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="91ff4-123">SCDPM</span></span>
- <span data-ttu-id="91ff4-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="91ff4-124">AzureBackupServer</span></span>
- <span data-ttu-id="91ff4-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="91ff4-125">AzureSQL</span></span>
- <span data-ttu-id="91ff4-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="91ff4-126">AzureStorage</span></span>
- <span data-ttu-id="91ff4-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="91ff4-127">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff4-128">-Container</span><span class="sxs-lookup"><span data-stu-id="91ff4-128">-Container</span></span>

<span data-ttu-id="91ff4-129">Anger ett Container-objekt som den här cmdleten ska säkerhetskopiera objekt från.</span><span class="sxs-lookup"><span data-stu-id="91ff4-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="91ff4-130">För att få en **AzureRmRecoveryServicesBackupContainer** använder du cmdleten **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="91ff4-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="91ff4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ff4-131">-DefaultProfile</span></span>

<span data-ttu-id="91ff4-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91ff4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ff4-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="91ff4-133">-DeleteState</span></span>
<span data-ttu-id="91ff4-134">Anger deletestate för artikeln de acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91ff4-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ff4-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="91ff4-135">ToBeDeleted</span></span>
- <span data-ttu-id="91ff4-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="91ff4-136">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff4-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="91ff4-137">-Name</span></span>

<span data-ttu-id="91ff4-138">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="91ff4-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="91ff4-139">-Princip</span><span class="sxs-lookup"><span data-stu-id="91ff4-139">-Policy</span></span>

<span data-ttu-id="91ff4-140">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="91ff4-140">Protection policy object.</span></span>

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

### <span data-ttu-id="91ff4-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="91ff4-141">-ProtectionState</span></span>

<span data-ttu-id="91ff4-142">Anger skydds tillståndet.</span><span class="sxs-lookup"><span data-stu-id="91ff4-142">Specifies the state of protection.</span></span>
<span data-ttu-id="91ff4-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91ff4-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ff4-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="91ff4-144">IRPending.</span></span>
<span data-ttu-id="91ff4-145">Den första synkroniseringen har inte påbörjats och det finns ingen återställnings punkt ännu.</span><span class="sxs-lookup"><span data-stu-id="91ff4-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="91ff4-146">Upphovsrättsskydd.</span><span class="sxs-lookup"><span data-stu-id="91ff4-146">Protected.</span></span>
<span data-ttu-id="91ff4-147">Skyddet pågår.</span><span class="sxs-lookup"><span data-stu-id="91ff4-147">Protection is ongoing.</span></span>
- <span data-ttu-id="91ff4-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="91ff4-148">ProtectionError.</span></span>
<span data-ttu-id="91ff4-149">Ett skydds fel har uppstått.</span><span class="sxs-lookup"><span data-stu-id="91ff4-149">There is a protection error.</span></span>
- <span data-ttu-id="91ff4-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="91ff4-150">ProtectionStopped.</span></span>
<span data-ttu-id="91ff4-151">Skyddet är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="91ff4-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="91ff4-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="91ff4-152">-ProtectionStatus</span></span>

<span data-ttu-id="91ff4-153">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="91ff4-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="91ff4-154">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91ff4-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ff4-155">Sund</span><span class="sxs-lookup"><span data-stu-id="91ff4-155">Healthy</span></span>
- <span data-ttu-id="91ff4-156">Ohälsosamt</span><span class="sxs-lookup"><span data-stu-id="91ff4-156">Unhealthy</span></span>

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

### <span data-ttu-id="91ff4-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="91ff4-157">-VaultId</span></span>

<span data-ttu-id="91ff4-158">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="91ff4-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="91ff4-159">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="91ff4-159">-WorkloadType</span></span>

<span data-ttu-id="91ff4-160">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="91ff4-160">Specifies the workload type.</span></span>
<span data-ttu-id="91ff4-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="91ff4-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ff4-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="91ff4-162">AzureVM</span></span>
- <span data-ttu-id="91ff4-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="91ff4-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="91ff4-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="91ff4-164">AzureFiles</span></span>
- <span data-ttu-id="91ff4-165">MSSQL</span><span class="sxs-lookup"><span data-stu-id="91ff4-165">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff4-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ff4-166">-CommonParameters</span></span>

<span data-ttu-id="91ff4-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ff4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ff4-168">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91ff4-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ff4-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91ff4-169">INPUTS</span></span>

### <span data-ttu-id="91ff4-170">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="91ff4-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="91ff4-171">System. String</span><span class="sxs-lookup"><span data-stu-id="91ff4-171">System.String</span></span>

## <span data-ttu-id="91ff4-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91ff4-172">OUTPUTS</span></span>

### <span data-ttu-id="91ff4-173">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="91ff4-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="91ff4-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91ff4-174">NOTES</span></span>

## <span data-ttu-id="91ff4-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91ff4-175">RELATED LINKS</span></span>

[<span data-ttu-id="91ff4-176">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91ff4-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="91ff4-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="91ff4-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="91ff4-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="91ff4-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="91ff4-179">Återställ-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="91ff4-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
