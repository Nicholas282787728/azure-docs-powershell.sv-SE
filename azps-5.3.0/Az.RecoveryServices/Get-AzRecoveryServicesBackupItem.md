---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 429e0801cc0c003aa1ffdb7080caada8e8d07517
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522349"
---
# <span data-ttu-id="3a685-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3a685-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="3a685-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a685-102">SYNOPSIS</span></span>

<span data-ttu-id="3a685-103">Hämtar objekten från en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="3a685-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="3a685-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a685-104">SYNTAX</span></span>

### <span data-ttu-id="3a685-105">GetItemsForContainer (standard)</span><span class="sxs-lookup"><span data-stu-id="3a685-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a685-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="3a685-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a685-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="3a685-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a685-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a685-108">DESCRIPTION</span></span>

<span data-ttu-id="3a685-109">Cmdleten **Get-AzRecoveryServicesBackupItem** hämtar listan över skyddade objekt i en behållare och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="3a685-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="3a685-110">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="3a685-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="3a685-111">För virtuella Azure-datorer kan det bara finnas ett säkerhets kopie objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3a685-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="3a685-112">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="3a685-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="3a685-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a685-113">EXAMPLES</span></span>

### <span data-ttu-id="3a685-114">Exempel 1: Hämta ett objekt från en säkerhets kopia av en behållare</span><span class="sxs-lookup"><span data-stu-id="3a685-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="3a685-115">Det första kommandot får behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="3a685-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3a685-116">Det andra kommandot får det säkerhets kopie objekt som heter V2VM i $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="3a685-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="3a685-117">Exempel 2: Hämta ett Azure File Share-objekt från FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3a685-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="3a685-118">Det första kommandot får behållaren av typen AzureStorage och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="3a685-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="3a685-119">Det andra kommandot får det säkerhets kopie objekt vars friendlyName matchar det värde som skickades till FriendlyName-parametern och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="3a685-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3a685-120">Om du använder FriendlyName-parametern kan du returnera mer än en Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="3a685-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="3a685-121">I sådana fall kör du cmdleten genom att skicka värdet för parametern namn som namn-egenskapen som visas i resultat uppsättningen med $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="3a685-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="3a685-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a685-122">PARAMETERS</span></span>

### <span data-ttu-id="3a685-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="3a685-123">-BackupManagementType</span></span>

<span data-ttu-id="3a685-124">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="3a685-124">The class of resources being protected.</span></span> <span data-ttu-id="3a685-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3a685-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a685-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a685-126">AzureVM</span></span>
- <span data-ttu-id="3a685-127">ANTI</span><span class="sxs-lookup"><span data-stu-id="3a685-127">MAB</span></span>
- <span data-ttu-id="3a685-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="3a685-128">AzureStorage</span></span>
- <span data-ttu-id="3a685-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="3a685-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a685-130">-Container</span><span class="sxs-lookup"><span data-stu-id="3a685-130">-Container</span></span>

<span data-ttu-id="3a685-131">Anger ett Container-objekt som den här cmdleten ska säkerhetskopiera objekt från.</span><span class="sxs-lookup"><span data-stu-id="3a685-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="3a685-132">För att få en **AzureRmRecoveryServicesBackupContainer** använder du cmdleten **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="3a685-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="3a685-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a685-133">-DefaultProfile</span></span>

<span data-ttu-id="3a685-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a685-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a685-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="3a685-135">-DeleteState</span></span>
<span data-ttu-id="3a685-136">Anger deletestate för artikeln de acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3a685-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a685-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="3a685-137">ToBeDeleted</span></span>
- <span data-ttu-id="3a685-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="3a685-138">NotDeleted</span></span>

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

### <span data-ttu-id="3a685-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3a685-139">-FriendlyName</span></span>
<span data-ttu-id="3a685-140">FriendlyName för det säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="3a685-140">FriendlyName of the backed up item</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a685-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="3a685-141">-Name</span></span>

<span data-ttu-id="3a685-142">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="3a685-142">Specifies the name of backup item.</span></span> <span data-ttu-id="3a685-143">Ange det unika ID: t för skyddad fil resurs för fil resurs.</span><span class="sxs-lookup"><span data-stu-id="3a685-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="3a685-144">-Princip</span><span class="sxs-lookup"><span data-stu-id="3a685-144">-Policy</span></span>

<span data-ttu-id="3a685-145">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="3a685-145">Protection policy object.</span></span>

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

### <span data-ttu-id="3a685-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="3a685-146">-ProtectionState</span></span>

<span data-ttu-id="3a685-147">Anger skydds tillståndet.</span><span class="sxs-lookup"><span data-stu-id="3a685-147">Specifies the state of protection.</span></span>
<span data-ttu-id="3a685-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3a685-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a685-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="3a685-149">IRPending.</span></span>
<span data-ttu-id="3a685-150">Den första synkroniseringen har inte påbörjats och det finns ingen återställnings punkt ännu.</span><span class="sxs-lookup"><span data-stu-id="3a685-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="3a685-151">Upphovsrättsskydd.</span><span class="sxs-lookup"><span data-stu-id="3a685-151">Protected.</span></span>
<span data-ttu-id="3a685-152">Skyddet pågår.</span><span class="sxs-lookup"><span data-stu-id="3a685-152">Protection is ongoing.</span></span>
- <span data-ttu-id="3a685-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="3a685-153">ProtectionError.</span></span>
<span data-ttu-id="3a685-154">Ett skydds fel har uppstått.</span><span class="sxs-lookup"><span data-stu-id="3a685-154">There is a protection error.</span></span>
- <span data-ttu-id="3a685-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="3a685-155">ProtectionStopped.</span></span>
<span data-ttu-id="3a685-156">Skyddet är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="3a685-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="3a685-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="3a685-157">-ProtectionStatus</span></span>

<span data-ttu-id="3a685-158">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="3a685-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="3a685-159">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3a685-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a685-160">Sund</span><span class="sxs-lookup"><span data-stu-id="3a685-160">Healthy</span></span>
- <span data-ttu-id="3a685-161">Ohälsosamt</span><span class="sxs-lookup"><span data-stu-id="3a685-161">Unhealthy</span></span>

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

### <span data-ttu-id="3a685-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3a685-162">-VaultId</span></span>

<span data-ttu-id="3a685-163">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="3a685-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3a685-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="3a685-164">-WorkloadType</span></span>

<span data-ttu-id="3a685-165">Arbets belastnings typ för resursen.</span><span class="sxs-lookup"><span data-stu-id="3a685-165">Workload type of the resource.</span></span> <span data-ttu-id="3a685-166">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3a685-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3a685-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="3a685-167">AzureVM</span></span>
- <span data-ttu-id="3a685-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="3a685-168">AzureFiles</span></span>
- <span data-ttu-id="3a685-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="3a685-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a685-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a685-170">CommonParameters</span></span>
<span data-ttu-id="3a685-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a685-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a685-172">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a685-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a685-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a685-173">INPUTS</span></span>

### <span data-ttu-id="3a685-174">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="3a685-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="3a685-175">System. String</span><span class="sxs-lookup"><span data-stu-id="3a685-175">System.String</span></span>

## <span data-ttu-id="3a685-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a685-176">OUTPUTS</span></span>

### <span data-ttu-id="3a685-177">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="3a685-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="3a685-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a685-178">NOTES</span></span>

## <span data-ttu-id="3a685-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a685-179">RELATED LINKS</span></span>

[<span data-ttu-id="3a685-180">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3a685-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="3a685-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3a685-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="3a685-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="3a685-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="3a685-183">Återställ-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="3a685-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
