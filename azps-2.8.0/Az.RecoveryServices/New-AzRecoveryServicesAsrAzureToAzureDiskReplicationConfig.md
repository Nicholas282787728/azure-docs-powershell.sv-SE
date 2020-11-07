---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919719"
---
# <span data-ttu-id="afdb1-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="afdb1-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="afdb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afdb1-102">SYNOPSIS</span></span>
<span data-ttu-id="afdb1-103">Skapar ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras.</span><span class="sxs-lookup"><span data-stu-id="afdb1-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="afdb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afdb1-104">SYNTAX</span></span>

### <span data-ttu-id="afdb1-105">AzureToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="afdb1-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afdb1-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="afdb1-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afdb1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afdb1-107">DESCRIPTION</span></span>
<span data-ttu-id="afdb1-108">Skapar ett disk kart objekt som mappar en virtuell Azure-dator-disk till det lagrings konto och mål lagrings konto (återställnings område) som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="afdb1-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="afdb1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afdb1-109">EXAMPLES</span></span>

### <span data-ttu-id="afdb1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="afdb1-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="afdb1-111">Skapa ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras. Används under Azure to Azure-Aktiveradare och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="afdb1-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="afdb1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afdb1-112">PARAMETERS</span></span>

### <span data-ttu-id="afdb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdb1-113">-DefaultProfile</span></span>
<span data-ttu-id="afdb1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afdb1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afdb1-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="afdb1-115">-DiskId</span></span>
<span data-ttu-id="afdb1-116">Anger disk-ID för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="afdb1-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="afdb1-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="afdb1-117">-LogStorageAccountId</span></span>
<span data-ttu-id="afdb1-118">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="afdb1-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="afdb1-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="afdb1-119">-ManagedDisk</span></span>
<span data-ttu-id="afdb1-120">Anger att indata används för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="afdb1-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="afdb1-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="afdb1-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="afdb1-122">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="afdb1-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="afdb1-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="afdb1-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="afdb1-124">Anger kontotyp för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="afdb1-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdb1-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="afdb1-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="afdb1-126">Anger ID för återställnings resurs för den replikerade hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="afdb1-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="afdb1-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="afdb1-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="afdb1-128">Anger återställnings mål disken för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="afdb1-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdb1-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="afdb1-129">-VhdUri</span></span>
<span data-ttu-id="afdb1-130">Ange VHD URI för den disk som den här mappningen motsvarar.</span><span class="sxs-lookup"><span data-stu-id="afdb1-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="afdb1-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afdb1-131">-Confirm</span></span>
<span data-ttu-id="afdb1-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afdb1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afdb1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdb1-133">-WhatIf</span></span>
<span data-ttu-id="afdb1-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afdb1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afdb1-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afdb1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afdb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdb1-136">CommonParameters</span></span>
<span data-ttu-id="afdb1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afdb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdb1-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afdb1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdb1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afdb1-139">INPUTS</span></span>

### <span data-ttu-id="afdb1-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="afdb1-140">None</span></span>

## <span data-ttu-id="afdb1-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afdb1-141">OUTPUTS</span></span>

### <span data-ttu-id="afdb1-142">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="afdb1-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="afdb1-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afdb1-143">NOTES</span></span>

## <span data-ttu-id="afdb1-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afdb1-144">RELATED LINKS</span></span>
