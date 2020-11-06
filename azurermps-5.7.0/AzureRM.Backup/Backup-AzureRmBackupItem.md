---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1e68e1b711e6e365920b717f9d7675473d3c911b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582108"
---
# <span data-ttu-id="72201-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="72201-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="72201-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72201-102">SYNOPSIS</span></span>
<span data-ttu-id="72201-103">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="72201-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72201-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72201-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72201-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72201-105">DESCRIPTION</span></span>
<span data-ttu-id="72201-106">**Säkerhets kopiering-AzureRmBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="72201-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="72201-107">Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="72201-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="72201-108">Om det finns ett befintligt säkerhets kopierings jobb Miss lyckas denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72201-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="72201-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72201-109">EXAMPLES</span></span>

### <span data-ttu-id="72201-110">Exempel 1: börja säkerhetskopiera en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="72201-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="72201-111">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72201-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="72201-112">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="72201-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="72201-113">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda Get-AzureRmBackupContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72201-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="72201-114">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="72201-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="72201-115">Med det senaste kommandot hämtas säkerhets kopierings objekt i $Container med hjälp av Get-AzureRmBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72201-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="72201-116">Kommandot skickar objekten till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="72201-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72201-117">Den aktuella cmdleten börjar säkerhetskopiera den virtuella datorn i behållaren.</span><span class="sxs-lookup"><span data-stu-id="72201-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="72201-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72201-118">PARAMETERS</span></span>

### <span data-ttu-id="72201-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72201-119">-DefaultProfile</span></span>
<span data-ttu-id="72201-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="72201-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72201-121">-Objekt</span><span class="sxs-lookup"><span data-stu-id="72201-121">-Item</span></span>
<span data-ttu-id="72201-122">Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.</span><span class="sxs-lookup"><span data-stu-id="72201-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72201-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72201-123">CommonParameters</span></span>
<span data-ttu-id="72201-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72201-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72201-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72201-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72201-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72201-126">INPUTS</span></span>

### <span data-ttu-id="72201-127">AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="72201-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="72201-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72201-128">OUTPUTS</span></span>

### <span data-ttu-id="72201-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="72201-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="72201-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72201-130">NOTES</span></span>

## <span data-ttu-id="72201-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72201-131">RELATED LINKS</span></span>

[<span data-ttu-id="72201-132">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="72201-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="72201-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="72201-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="72201-134">Återställ-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="72201-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


