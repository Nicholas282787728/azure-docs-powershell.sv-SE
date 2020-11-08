---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100934"
---
# <span data-ttu-id="27e05-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="27e05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27e05-102">SYNOPSIS</span></span>
<span data-ttu-id="27e05-103">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="27e05-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="27e05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27e05-104">SYNTAX</span></span>

### <span data-ttu-id="27e05-105">AzureVMComputeEnableProtection (standard)</span><span class="sxs-lookup"><span data-stu-id="27e05-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27e05-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e05-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e05-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27e05-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27e05-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27e05-110">DESCRIPTION</span></span>
<span data-ttu-id="27e05-111">Cmdleten **Enable-AzRecoveryServicesBackupProtection** aktiverar säkerhets kopian genom att koppla en skydds princip till objektet.</span><span class="sxs-lookup"><span data-stu-id="27e05-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="27e05-112">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27e05-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="27e05-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27e05-113">EXAMPLES</span></span>

### <span data-ttu-id="27e05-114">Exempel 1: Aktivera säkerhets kopierings skydd för ett objekt</span><span class="sxs-lookup"><span data-stu-id="27e05-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="27e05-115">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="27e05-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="27e05-116">Den andra cmdleten anger vilka disk enheter som ska säkerhets kopie ras och lagrar dem i $inclusionDiskLUNS variabel.</span><span class="sxs-lookup"><span data-stu-id="27e05-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="27e05-117">Den tredje cmdleten ställer in säkerhets kopierings skydds principen för den virtuella dator ARM med namnet V2VM med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="27e05-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="27e05-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="27e05-118">Example 2</span></span>

<span data-ttu-id="27e05-119">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="27e05-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="27e05-120">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="27e05-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="27e05-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27e05-121">PARAMETERS</span></span>

### <span data-ttu-id="27e05-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e05-122">-DefaultProfile</span></span>
<span data-ttu-id="27e05-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27e05-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27e05-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="27e05-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="27e05-125">Alternativet endast för att ange säkerhets kopiering av OS-diskar</span><span class="sxs-lookup"><span data-stu-id="27e05-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="27e05-126">-ExclusionDisksList</span></span>
<span data-ttu-id="27e05-127">Lista över disk-LUN som ska uteslutas i säkerhets kopiering och resten ingår automatiskt.</span><span class="sxs-lookup"><span data-stu-id="27e05-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="27e05-128">-InclusionDisksList</span></span>
<span data-ttu-id="27e05-129">Lista över diskar som är logiska för säkerhets kopiering och resten utesluts automatiskt förutom OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="27e05-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-130">-Objekt</span><span class="sxs-lookup"><span data-stu-id="27e05-130">-Item</span></span>
<span data-ttu-id="27e05-131">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="27e05-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="27e05-132">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="27e05-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="27e05-133">-Name</span></span>
<span data-ttu-id="27e05-134">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="27e05-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-135">-Princip</span><span class="sxs-lookup"><span data-stu-id="27e05-135">-Policy</span></span>
<span data-ttu-id="27e05-136">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="27e05-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="27e05-137">Använd Get-AzRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **AzureRmRecoveryServicesBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="27e05-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="27e05-138">-ProtectableItem</span></span>
<span data-ttu-id="27e05-139">Anger det objekt som ska skyddas med den angivna policyn.</span><span class="sxs-lookup"><span data-stu-id="27e05-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="27e05-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="27e05-141">Anger att inställningen för disk uteslutning är kopplad till objektet</span><span class="sxs-lookup"><span data-stu-id="27e05-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e05-142">-ResourceGroupName</span></span>
<span data-ttu-id="27e05-143">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="27e05-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="27e05-144">Ange endast den här parametern för virtuella ARM datorer.</span><span class="sxs-lookup"><span data-stu-id="27e05-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27e05-145">-StorageAccountName</span></span>
<span data-ttu-id="27e05-146">Azure File Share lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="27e05-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="27e05-147">-VaultId</span></span>
<span data-ttu-id="27e05-148">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="27e05-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="27e05-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27e05-149">-Confirm</span></span>
<span data-ttu-id="27e05-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27e05-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e05-151">-WhatIf</span></span>
<span data-ttu-id="27e05-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27e05-152">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e05-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e05-153">CommonParameters</span></span>
<span data-ttu-id="27e05-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e05-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e05-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27e05-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e05-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27e05-156">INPUTS</span></span>

### <span data-ttu-id="27e05-157">System. String</span><span class="sxs-lookup"><span data-stu-id="27e05-157">System.String</span></span>

### <span data-ttu-id="27e05-158">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="27e05-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="27e05-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27e05-159">OUTPUTS</span></span>

### <span data-ttu-id="27e05-160">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="27e05-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="27e05-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27e05-161">NOTES</span></span>

## <span data-ttu-id="27e05-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27e05-162">RELATED LINKS</span></span>

[<span data-ttu-id="27e05-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="27e05-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="27e05-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="27e05-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

