---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582072"
---
# <span data-ttu-id="4ca61-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ca61-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="4ca61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ca61-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca61-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="4ca61-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ca61-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ca61-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca61-106">Cmdleten **restore-AzureRmBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="4ca61-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="4ca61-107">Denna cmdlet startar återställning från säkerhets kopierings valvet till ditt konto.</span><span class="sxs-lookup"><span data-stu-id="4ca61-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="4ca61-108">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4ca61-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="4ca61-109">Den återställer diskens data och konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="4ca61-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="4ca61-110">När återställningen är klar måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="4ca61-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="4ca61-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ca61-111">EXAMPLES</span></span>

### <span data-ttu-id="4ca61-112">Exempel 1: återställa en virtuell dator till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="4ca61-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="4ca61-113">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca61-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="4ca61-114">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4ca61-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="4ca61-115">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="4ca61-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="4ca61-116">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="4ca61-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="4ca61-117">Det tredje kommandot får säkerhets kopian i behållaren i $Container genom att använda cmdleten **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="4ca61-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="4ca61-118">Kommandot lagrar objektet i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="4ca61-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="4ca61-119">Det fjärde kommandot får återställnings punkt för objektet i $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="4ca61-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="4ca61-120">Kommandot lagrar objektet i $RecoveryPoint variabel.</span><span class="sxs-lookup"><span data-stu-id="4ca61-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="4ca61-121">Det sista kommandot återställer återställnings punkten i $RecoveryPoint för kontot med namnet DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="4ca61-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="4ca61-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ca61-122">PARAMETERS</span></span>

### <span data-ttu-id="4ca61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca61-123">-DefaultProfile</span></span>
<span data-ttu-id="4ca61-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ca61-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ca61-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4ca61-125">-RecoveryPoint</span></span>
<span data-ttu-id="4ca61-126">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="4ca61-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="4ca61-127">För att få en **AzureRmBackupRecoveryPoint** , Använd cmdleten Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="4ca61-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca61-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4ca61-128">-StorageAccountName</span></span>
<span data-ttu-id="4ca61-129">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4ca61-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="4ca61-130">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="4ca61-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

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

### <span data-ttu-id="4ca61-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca61-131">CommonParameters</span></span>
<span data-ttu-id="4ca61-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca61-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca61-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca61-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca61-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ca61-134">INPUTS</span></span>

### <span data-ttu-id="4ca61-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4ca61-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="4ca61-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ca61-136">OUTPUTS</span></span>

### <span data-ttu-id="4ca61-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4ca61-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="4ca61-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ca61-138">NOTES</span></span>

## <span data-ttu-id="4ca61-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ca61-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ca61-140">Säkerhets kopiering-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ca61-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="4ca61-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="4ca61-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="4ca61-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="4ca61-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


