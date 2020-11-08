---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088616"
---
# <span data-ttu-id="18142-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="18142-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="18142-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18142-102">SYNOPSIS</span></span>

<span data-ttu-id="18142-103">Hämtar objekten från en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="18142-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="18142-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18142-104">SYNTAX</span></span>

### <span data-ttu-id="18142-105">GetItemsForContainer (standard)</span><span class="sxs-lookup"><span data-stu-id="18142-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18142-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="18142-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18142-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="18142-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18142-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18142-108">DESCRIPTION</span></span>

<span data-ttu-id="18142-109">Cmdleten **Get-AzRecoveryServicesBackupItem** hämtar objekten i en container eller ett värde i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="18142-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="18142-110">En behållare som är registrerad på ett Azure Recovery Services-valv kan ha en eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="18142-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="18142-111">För virtuella Azure-datorer kan det bara finnas ett säkerhets kopie objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="18142-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="18142-112">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="18142-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="18142-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18142-113">EXAMPLES</span></span>

### <span data-ttu-id="18142-114">Exempel 1: Hämta ett objekt från en säkerhets kopia av en behållare</span><span class="sxs-lookup"><span data-stu-id="18142-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="18142-115">Det första kommandot får behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="18142-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="18142-116">Det andra kommandot får det säkerhets kopie objekt som heter V2VM i $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="18142-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="18142-117">Exempel 2: Hämta ett Azure File Share-objekt från FriendlyName</span><span class="sxs-lookup"><span data-stu-id="18142-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="18142-118">Det första kommandot får behållaren av typen AzureStorage och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="18142-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="18142-119">Det andra kommandot får det säkerhets kopie objekt vars friendlyName matchar det värde som skickades till FriendlyName-parametern och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="18142-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="18142-120">Om du använder FriendlyName-parametern kan du returnera mer än en Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="18142-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="18142-121">I sådana fall används-parametern namn med parametervärdet som namn egenskap som returneras i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="18142-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="18142-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18142-122">PARAMETERS</span></span>

### <span data-ttu-id="18142-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="18142-123">-BackupManagementType</span></span>

<span data-ttu-id="18142-124">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="18142-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="18142-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18142-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18142-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="18142-126">AzureVM</span></span>
- <span data-ttu-id="18142-127">OM</span><span class="sxs-lookup"><span data-stu-id="18142-127">MARS</span></span>
- <span data-ttu-id="18142-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="18142-128">SCDPM</span></span>
- <span data-ttu-id="18142-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="18142-129">AzureBackupServer</span></span>
- <span data-ttu-id="18142-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="18142-130">AzureSQL</span></span>
- <span data-ttu-id="18142-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="18142-131">AzureStorage</span></span>
- <span data-ttu-id="18142-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="18142-132">AzureWorkload</span></span>

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

### <span data-ttu-id="18142-133">-Container</span><span class="sxs-lookup"><span data-stu-id="18142-133">-Container</span></span>

<span data-ttu-id="18142-134">Anger ett Container-objekt som den här cmdleten ska säkerhetskopiera objekt från.</span><span class="sxs-lookup"><span data-stu-id="18142-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="18142-135">För att få en **AzureRmRecoveryServicesBackupContainer** använder du cmdleten **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="18142-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="18142-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18142-136">-DefaultProfile</span></span>

<span data-ttu-id="18142-137">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18142-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18142-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="18142-138">-DeleteState</span></span>
<span data-ttu-id="18142-139">Anger deletestate för artikeln de acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18142-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18142-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="18142-140">ToBeDeleted</span></span>
- <span data-ttu-id="18142-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="18142-141">NotDeleted</span></span>

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

### <span data-ttu-id="18142-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="18142-142">-FriendlyName</span></span>
<span data-ttu-id="18142-143">FriendlyName för det säkerhetskopierade objektet</span><span class="sxs-lookup"><span data-stu-id="18142-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="18142-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="18142-144">-Name</span></span>

<span data-ttu-id="18142-145">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="18142-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="18142-146">-Princip</span><span class="sxs-lookup"><span data-stu-id="18142-146">-Policy</span></span>

<span data-ttu-id="18142-147">Skydds princip objekt.</span><span class="sxs-lookup"><span data-stu-id="18142-147">Protection policy object.</span></span>

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

### <span data-ttu-id="18142-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="18142-148">-ProtectionState</span></span>

<span data-ttu-id="18142-149">Anger skydds tillståndet.</span><span class="sxs-lookup"><span data-stu-id="18142-149">Specifies the state of protection.</span></span>
<span data-ttu-id="18142-150">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18142-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18142-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="18142-151">IRPending.</span></span>
<span data-ttu-id="18142-152">Den första synkroniseringen har inte påbörjats och det finns ingen återställnings punkt ännu.</span><span class="sxs-lookup"><span data-stu-id="18142-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="18142-153">Upphovsrättsskydd.</span><span class="sxs-lookup"><span data-stu-id="18142-153">Protected.</span></span>
<span data-ttu-id="18142-154">Skyddet pågår.</span><span class="sxs-lookup"><span data-stu-id="18142-154">Protection is ongoing.</span></span>
- <span data-ttu-id="18142-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="18142-155">ProtectionError.</span></span>
<span data-ttu-id="18142-156">Ett skydds fel har uppstått.</span><span class="sxs-lookup"><span data-stu-id="18142-156">There is a protection error.</span></span>
- <span data-ttu-id="18142-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="18142-157">ProtectionStopped.</span></span>
<span data-ttu-id="18142-158">Skyddet är inaktiverat.</span><span class="sxs-lookup"><span data-stu-id="18142-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="18142-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="18142-159">-ProtectionStatus</span></span>

<span data-ttu-id="18142-160">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="18142-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="18142-161">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18142-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18142-162">Sund</span><span class="sxs-lookup"><span data-stu-id="18142-162">Healthy</span></span>
- <span data-ttu-id="18142-163">Ohälsosamt</span><span class="sxs-lookup"><span data-stu-id="18142-163">Unhealthy</span></span>

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

### <span data-ttu-id="18142-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="18142-164">-VaultId</span></span>

<span data-ttu-id="18142-165">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="18142-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="18142-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="18142-166">-WorkloadType</span></span>

<span data-ttu-id="18142-167">Anger arbets belastnings typen.</span><span class="sxs-lookup"><span data-stu-id="18142-167">Specifies the workload type.</span></span>
<span data-ttu-id="18142-168">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="18142-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18142-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="18142-169">AzureVM</span></span>
- <span data-ttu-id="18142-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="18142-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="18142-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="18142-171">AzureFiles</span></span>
- <span data-ttu-id="18142-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="18142-172">MSSQL</span></span>

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

### <span data-ttu-id="18142-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18142-173">CommonParameters</span></span>
<span data-ttu-id="18142-174">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18142-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18142-175">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18142-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18142-176">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18142-176">INPUTS</span></span>

### <span data-ttu-id="18142-177">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="18142-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="18142-178">System. String</span><span class="sxs-lookup"><span data-stu-id="18142-178">System.String</span></span>

## <span data-ttu-id="18142-179">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18142-179">OUTPUTS</span></span>

### <span data-ttu-id="18142-180">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="18142-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="18142-181">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18142-181">NOTES</span></span>

## <span data-ttu-id="18142-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18142-182">RELATED LINKS</span></span>

[<span data-ttu-id="18142-183">Säkerhets kopiering-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="18142-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="18142-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="18142-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="18142-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="18142-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="18142-186">Återställ-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="18142-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
