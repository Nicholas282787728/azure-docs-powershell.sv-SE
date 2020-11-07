---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919796"
---
# <span data-ttu-id="16ea0-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="16ea0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="16ea0-103">Aktiverar säkerhets kopiering av ett objekt med en angiven säkerhets policy för säkerhet.</span><span class="sxs-lookup"><span data-stu-id="16ea0-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="16ea0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16ea0-104">SYNTAX</span></span>

### <span data-ttu-id="16ea0-105">AzureVMComputeEnableProtection (standard)</span><span class="sxs-lookup"><span data-stu-id="16ea0-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ea0-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ea0-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ea0-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ea0-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ea0-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16ea0-110">DESCRIPTION</span></span>
<span data-ttu-id="16ea0-111">Cmdleten **Enable-AzRecoveryServicesBackupProtection** anger Azure säkerhets kopierings princip för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="16ea0-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="16ea0-112">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16ea0-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="16ea0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16ea0-113">EXAMPLES</span></span>

### <span data-ttu-id="16ea0-114">Exempel 1: Aktivera säkerhets kopierings skydd för ett objekt</span><span class="sxs-lookup"><span data-stu-id="16ea0-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="16ea0-115">Den första cmdleten får ett standard princip objekt och lagrar det sedan i $Pol variabel.</span><span class="sxs-lookup"><span data-stu-id="16ea0-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="16ea0-116">Den andra cmdleten ställer in säkerhets kopierings skydds principen för den virtuella dator ARM med namnet V2VM med principen i $Pol.</span><span class="sxs-lookup"><span data-stu-id="16ea0-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="16ea0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16ea0-117">PARAMETERS</span></span>

### <span data-ttu-id="16ea0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ea0-118">-DefaultProfile</span></span>
<span data-ttu-id="16ea0-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16ea0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ea0-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="16ea0-120">-Item</span></span>
<span data-ttu-id="16ea0-121">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="16ea0-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="16ea0-122">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="16ea0-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="16ea0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="16ea0-123">-Name</span></span>
<span data-ttu-id="16ea0-124">Anger namnet på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="16ea0-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="16ea0-125">-Princip</span><span class="sxs-lookup"><span data-stu-id="16ea0-125">-Policy</span></span>
<span data-ttu-id="16ea0-126">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="16ea0-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="16ea0-127">Använd Get-AzRecoveryServicesBackupProtectionPolicy cmdlet för att få ett **AzureRmRecoveryServicesBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="16ea0-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ea0-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="16ea0-128">-ProtectableItem</span></span>
<span data-ttu-id="16ea0-129">Filter värde för jobb status.</span><span class="sxs-lookup"><span data-stu-id="16ea0-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="16ea0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ea0-130">-ResourceGroupName</span></span>
<span data-ttu-id="16ea0-131">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="16ea0-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="16ea0-132">Ange endast den här parametern för virtuella ARM datorer.</span><span class="sxs-lookup"><span data-stu-id="16ea0-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="16ea0-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="16ea0-133">-ServiceName</span></span>
<span data-ttu-id="16ea0-134">Anger tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="16ea0-134">Specifies the service name.</span></span>
<span data-ttu-id="16ea0-135">Ange endast den här parametern för virtuella ASM-datorer.</span><span class="sxs-lookup"><span data-stu-id="16ea0-135">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ea0-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="16ea0-136">-StorageAccountName</span></span>
<span data-ttu-id="16ea0-137">Azure File Share lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="16ea0-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="16ea0-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="16ea0-138">-VaultId</span></span>
<span data-ttu-id="16ea0-139">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="16ea0-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="16ea0-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16ea0-140">-Confirm</span></span>
<span data-ttu-id="16ea0-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16ea0-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ea0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ea0-142">-WhatIf</span></span>
<span data-ttu-id="16ea0-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16ea0-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16ea0-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16ea0-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ea0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ea0-145">CommonParameters</span></span>
<span data-ttu-id="16ea0-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ea0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ea0-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ea0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ea0-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16ea0-148">INPUTS</span></span>

### <span data-ttu-id="16ea0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="16ea0-149">System.String</span></span>

### <span data-ttu-id="16ea0-150">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="16ea0-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="16ea0-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16ea0-151">OUTPUTS</span></span>

### <span data-ttu-id="16ea0-152">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="16ea0-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="16ea0-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16ea0-153">NOTES</span></span>

## <span data-ttu-id="16ea0-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16ea0-154">RELATED LINKS</span></span>

[<span data-ttu-id="16ea0-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="16ea0-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="16ea0-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="16ea0-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


