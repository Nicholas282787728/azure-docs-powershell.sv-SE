---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: b449b96417f0ac05fa857a48a10143a285ed888f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575017"
---
# <span data-ttu-id="bcb81-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bcb81-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="bcb81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcb81-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb81-103">Återställer data och konfiguration för ett säkerhets kopie objekt till en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="bcb81-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcb81-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcb81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcb81-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb81-106">Cmdleten **restore-AzureRmBackupItem** återställer data och konfiguration för ett Azure Backup-objekt till en angiven återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="bcb81-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="bcb81-107">Denna cmdlet startar återställning från säkerhets kopierings valvet till ditt konto.</span><span class="sxs-lookup"><span data-stu-id="bcb81-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="bcb81-108">Återställnings åtgärden återställer inte den fullständiga virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bcb81-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="bcb81-109">Den återställer diskens data och konfigurations information.</span><span class="sxs-lookup"><span data-stu-id="bcb81-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="bcb81-110">När återställningen är klar måste du skapa den virtuella datorn och starta den.</span><span class="sxs-lookup"><span data-stu-id="bcb81-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="bcb81-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcb81-111">EXAMPLES</span></span>

### <span data-ttu-id="bcb81-112">Exempel 1: återställa en virtuell dator till en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="bcb81-112">Example 1: Restore a virtual machine to a recovery point</span></span>
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

<span data-ttu-id="bcb81-113">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb81-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="bcb81-114">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="bcb81-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="bcb81-115">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="bcb81-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="bcb81-116">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="bcb81-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="bcb81-117">Det tredje kommandot får säkerhets kopian i behållaren i $Container genom att använda cmdleten **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="bcb81-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="bcb81-118">Kommandot lagrar objektet i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="bcb81-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="bcb81-119">Det fjärde kommandot får återställnings punkt för objektet i $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="bcb81-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="bcb81-120">Kommandot lagrar objektet i $RecoveryPoint variabel.</span><span class="sxs-lookup"><span data-stu-id="bcb81-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="bcb81-121">Det sista kommandot återställer återställnings punkten i $RecoveryPoint för kontot med namnet DestinationAccount.</span><span class="sxs-lookup"><span data-stu-id="bcb81-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="bcb81-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcb81-122">PARAMETERS</span></span>

### <span data-ttu-id="bcb81-123">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bcb81-123">-RecoveryPoint</span></span>
<span data-ttu-id="bcb81-124">Anger den återställnings punkt där den virtuella datorn ska återställas.</span><span class="sxs-lookup"><span data-stu-id="bcb81-124">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="bcb81-125">För att få en **AzureRmBackupRecoveryPoint** , Använd cmdleten Get-AzureRmBackupRecoveryPoint.</span><span class="sxs-lookup"><span data-stu-id="bcb81-125">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb81-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bcb81-126">-StorageAccountName</span></span>
<span data-ttu-id="bcb81-127">Anger namnet på mål lagrings kontot i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="bcb81-127">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="bcb81-128">Som en del av återställnings processen lagrar denna cmdlet diskar och konfigurations information i det här lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="bcb81-128">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb81-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb81-129">-DefaultProfile</span></span>
<span data-ttu-id="bcb81-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb81-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb81-131">CommonParameters</span></span>
<span data-ttu-id="bcb81-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb81-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb81-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb81-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcb81-134">INPUTS</span></span>

### <span data-ttu-id="bcb81-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bcb81-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="bcb81-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcb81-136">OUTPUTS</span></span>

### <span data-ttu-id="bcb81-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="bcb81-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="bcb81-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcb81-138">NOTES</span></span>

## <span data-ttu-id="bcb81-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcb81-139">RELATED LINKS</span></span>

[<span data-ttu-id="bcb81-140">Säkerhets kopiering-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bcb81-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="bcb81-141">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="bcb81-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="bcb81-142">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="bcb81-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)


