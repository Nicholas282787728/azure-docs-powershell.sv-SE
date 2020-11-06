---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574220"
---
# <span data-ttu-id="36b8d-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36b8d-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="36b8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="36b8d-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="36b8d-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36b8d-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="36b8d-106">Cmdleten **restore-AzureRmRecoveryServicesBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="36b8d-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="36b8d-107">Denna cmdlet startar återställning från Recovery Services-valvet till kundens lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="36b8d-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="36b8d-108">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="36b8d-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="36b8d-109">Den återställer diskens data och konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="36b8d-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="36b8d-110">När återställningen är klar måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="36b8d-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="36b8d-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36b8d-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="36b8d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36b8d-112">EXAMPLES</span></span>

### <span data-ttu-id="36b8d-113">Exempel 1: Återställ ett objekt till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="36b8d-113">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="36b8d-114">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM och lagrar den sedan i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="36b8d-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="36b8d-115">Det andra kommandot får det säkerhets kopie objekt som heter V2VM från $Container och lagrar det sedan i $BackupItem-variabeln.</span><span class="sxs-lookup"><span data-stu-id="36b8d-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="36b8d-116">Det tredje kommandot får datum från sju dagar innan det sparas i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="36b8d-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="36b8d-117">Det fjärde kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="36b8d-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="36b8d-118">Det femte kommandot får en lista över återställnings punkter för det specifika säkerhets kopierings objekt som filtrerats efter $StartDate och $EndDate.</span><span class="sxs-lookup"><span data-stu-id="36b8d-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="36b8d-119">Det angivna datum intervallet är de senaste sju dagarna.</span><span class="sxs-lookup"><span data-stu-id="36b8d-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="36b8d-120">Med det senaste kommandot återställs diskarna till mål lagrings kontots DestAccount i resurs gruppen DestRG.</span><span class="sxs-lookup"><span data-stu-id="36b8d-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="36b8d-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36b8d-121">PARAMETERS</span></span>

### <span data-ttu-id="36b8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b8d-122">-DefaultProfile</span></span>
<span data-ttu-id="36b8d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36b8d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="36b8d-124">-RecoveryPoint</span></span>
<span data-ttu-id="36b8d-125">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="36b8d-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="36b8d-126">Använd Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet för att få ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt.</span><span class="sxs-lookup"><span data-stu-id="36b8d-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36b8d-127">-StorageAccountName</span></span>
<span data-ttu-id="36b8d-128">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="36b8d-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="36b8d-129">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="36b8d-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b8d-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="36b8d-131">Anger namnet på den resurs grupp som innehåller mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="36b8d-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="36b8d-132">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="36b8d-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36b8d-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="36b8d-134">Använd den här växeln om diskarna från återställnings punkten ska återställas till sina ursprungliga lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="36b8d-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36b8d-135">-Confirm</span></span>
<span data-ttu-id="36b8d-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36b8d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b8d-137">-WhatIf</span></span>
<span data-ttu-id="36b8d-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36b8d-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36b8d-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36b8d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b8d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b8d-140">CommonParameters</span></span>
<span data-ttu-id="36b8d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b8d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b8d-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b8d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b8d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36b8d-143">INPUTS</span></span>

### <span data-ttu-id="36b8d-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="36b8d-144">RecoveryPointBase</span></span>
<span data-ttu-id="36b8d-145">Parametern ' RecoveryPoint ' godkänner värdet av typen ' RecoveryPointBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="36b8d-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="36b8d-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36b8d-146">OUTPUTS</span></span>

### <span data-ttu-id="36b8d-147">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="36b8d-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="36b8d-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36b8d-148">NOTES</span></span>

## <span data-ttu-id="36b8d-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36b8d-149">RELATED LINKS</span></span>

[<span data-ttu-id="36b8d-150">Säkerhets kopiering-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36b8d-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="36b8d-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="36b8d-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="36b8d-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="36b8d-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


