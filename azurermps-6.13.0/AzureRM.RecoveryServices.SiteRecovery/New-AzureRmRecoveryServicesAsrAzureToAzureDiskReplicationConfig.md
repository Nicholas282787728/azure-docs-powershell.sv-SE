---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 19ba256176c47b5841b9d124d186f376f0ecce7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755335"
---
# <span data-ttu-id="0b520-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="0b520-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="0b520-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b520-102">SYNOPSIS</span></span>
<span data-ttu-id="0b520-103">Skapar ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras.</span><span class="sxs-lookup"><span data-stu-id="0b520-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b520-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b520-104">SYNTAX</span></span>

### <span data-ttu-id="0b520-105">AzureToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="0b520-105">AzureToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b520-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0b520-106">AzureToAzureManagedDisk</span></span>
```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b520-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b520-107">DESCRIPTION</span></span>
<span data-ttu-id="0b520-108">Skapar ett disk kart objekt som mappar en virtuell Azure-dator-disk till det lagrings konto och mål lagrings konto (återställnings område) som ska användas för att replikera disken.</span><span class="sxs-lookup"><span data-stu-id="0b520-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="0b520-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b520-109">EXAMPLES</span></span>

### <span data-ttu-id="0b520-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0b520-110">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="0b520-111">Skapa ett disk kart objekt för virtuella Azure Virtual Machine-diskar att replikeras. Används under Azure to Azure-Aktiveradare och skydds åtgärd.</span><span class="sxs-lookup"><span data-stu-id="0b520-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="0b520-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b520-112">PARAMETERS</span></span>

### <span data-ttu-id="0b520-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b520-113">-DefaultProfile</span></span>
<span data-ttu-id="0b520-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b520-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b520-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="0b520-115">-DiskId</span></span>
<span data-ttu-id="0b520-116">Anger disk-ID för hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0b520-116">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="0b520-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b520-117">-LogStorageAccountId</span></span>
<span data-ttu-id="0b520-118">Anger det ID för logg-eller cache-minnet som ska användas för att lagra loggar.</span><span class="sxs-lookup"><span data-stu-id="0b520-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="0b520-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0b520-119">-ManagedDisk</span></span>
<span data-ttu-id="0b520-120">Anger att indata används för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="0b520-120">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="0b520-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b520-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="0b520-122">Anger ID för det Azure Storage-konto som ska replikeras till.</span><span class="sxs-lookup"><span data-stu-id="0b520-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="0b520-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="0b520-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="0b520-124">Anger kontotyp för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0b520-124">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="0b520-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="0b520-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="0b520-126">Anger ID för återställnings resurs för den replikerade hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="0b520-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="0b520-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="0b520-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="0b520-128">Anger återställnings mål disken för replikerad hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="0b520-128">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="0b520-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="0b520-129">-VhdUri</span></span>
<span data-ttu-id="0b520-130">Ange VHD URI för den disk som den här mappningen motsvarar.</span><span class="sxs-lookup"><span data-stu-id="0b520-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="0b520-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b520-131">-Confirm</span></span>
<span data-ttu-id="0b520-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b520-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b520-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b520-133">-WhatIf</span></span>
<span data-ttu-id="0b520-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b520-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b520-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b520-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b520-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b520-136">CommonParameters</span></span>
<span data-ttu-id="0b520-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b520-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b520-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b520-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b520-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b520-139">INPUTS</span></span>

### <span data-ttu-id="0b520-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="0b520-140">None</span></span>

## <span data-ttu-id="0b520-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b520-141">OUTPUTS</span></span>

### <span data-ttu-id="0b520-142">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="0b520-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="0b520-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b520-143">NOTES</span></span>

## <span data-ttu-id="0b520-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b520-144">RELATED LINKS</span></span>
