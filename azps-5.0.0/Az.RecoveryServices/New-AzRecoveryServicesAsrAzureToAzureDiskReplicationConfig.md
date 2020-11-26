---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271710"
---
# <span data-ttu-id="bda4b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="bda4b-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="bda4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bda4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bda4b-103">Skapar ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras.</span><span class="sxs-lookup"><span data-stu-id="bda4b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="bda4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bda4b-104">SYNTAX</span></span>

### <span data-ttu-id="bda4b-105">AzureToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="bda4b-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bda4b-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bda4b-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda4b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bda4b-107">DESCRIPTION</span></span>
<span data-ttu-id="bda4b-108">Skapar ett disk kart objekt som mappar en virtuell Azure-dator-disk till det lagrings konto och mål lagrings konto (återställnings område) som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="bda4b-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="bda4b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bda4b-109">EXAMPLES</span></span>

### <span data-ttu-id="bda4b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bda4b-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="bda4b-111">Skapa ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras. Används under Azure till Azure-Aktiveradre och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bda4b-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="bda4b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="bda4b-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="bda4b-113">Skapa ett hanterat disk kart objekt för virtuella Azure Virtual Machine-diskar. Används under Azure till Azure-Aktiveradre och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bda4b-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="bda4b-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="bda4b-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="bda4b-115">Skapa ett hanterat disk kart objekt med ett pass krypterings-inställningar för virtuella Azure Virtual Machine-diskar. Används under Azure till Azure-Aktiveradre och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bda4b-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="bda4b-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="bda4b-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="bda4b-117">Skapa ett hanterat disk kart objekt med mål disk kryptering Set ID för att replikera Azure Virtual Machine-diskar. Används under Azure till Azure-Aktiveradre och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="bda4b-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="bda4b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bda4b-118">PARAMETERS</span></span>

### <span data-ttu-id="bda4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda4b-119">-DefaultProfile</span></span>
<span data-ttu-id="bda4b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bda4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda4b-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="bda4b-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="bda4b-122">Anger den hemliga URL-adressen för disk krypteringen.</span><span class="sxs-lookup"><span data-stu-id="bda4b-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="bda4b-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="bda4b-124">Anger disk krypterings Key valv-ID.</span><span class="sxs-lookup"><span data-stu-id="bda4b-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="bda4b-125">-DiskId</span></span>
<span data-ttu-id="bda4b-126">Anger disk-ID för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="bda4b-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="bda4b-127">-FailoverDiskName</span></span>
<span data-ttu-id="bda4b-128">Anger namnet på disken som skapades vid redundans.</span><span class="sxs-lookup"><span data-stu-id="bda4b-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="bda4b-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="bda4b-130">Anger URL för Key Encryption.</span><span class="sxs-lookup"><span data-stu-id="bda4b-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="bda4b-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="bda4b-132">Anger Key krypterings Key valv-ID.</span><span class="sxs-lookup"><span data-stu-id="bda4b-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bda4b-133">-LogStorageAccountId</span></span>
<span data-ttu-id="bda4b-134">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="bda4b-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="bda4b-135">-ManagedDisk</span></span>
<span data-ttu-id="bda4b-136">Anger att indata används för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="bda4b-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bda4b-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bda4b-138">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="bda4b-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="bda4b-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="bda4b-140">Anger ID för den Azure Disk Encryption-uppsättning som ska användas för återställnings diskar.</span><span class="sxs-lookup"><span data-stu-id="bda4b-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="bda4b-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="bda4b-142">Anger kontotyp för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="bda4b-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bda4b-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="bda4b-144">Anger ID för återställnings resurs för den replikerade hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="bda4b-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="bda4b-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="bda4b-146">Anger återställnings mål disken för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="bda4b-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="bda4b-147">-TfoDiskName</span></span>
<span data-ttu-id="bda4b-148">Anger namnet på den disk som skapades under redundanstestning.</span><span class="sxs-lookup"><span data-stu-id="bda4b-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="bda4b-149">-VhdUri</span></span>
<span data-ttu-id="bda4b-150">Ange VHD URI för den disk som den här mappningen motsvarar.</span><span class="sxs-lookup"><span data-stu-id="bda4b-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda4b-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bda4b-151">-Confirm</span></span>
<span data-ttu-id="bda4b-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bda4b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda4b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda4b-153">-WhatIf</span></span>
<span data-ttu-id="bda4b-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bda4b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda4b-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bda4b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bda4b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda4b-156">CommonParameters</span></span>
<span data-ttu-id="bda4b-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bda4b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda4b-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bda4b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda4b-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bda4b-159">INPUTS</span></span>

### <span data-ttu-id="bda4b-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="bda4b-160">None</span></span>

## <span data-ttu-id="bda4b-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bda4b-161">OUTPUTS</span></span>

### <span data-ttu-id="bda4b-162">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="bda4b-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="bda4b-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bda4b-163">NOTES</span></span>

## <span data-ttu-id="bda4b-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bda4b-164">RELATED LINKS</span></span>