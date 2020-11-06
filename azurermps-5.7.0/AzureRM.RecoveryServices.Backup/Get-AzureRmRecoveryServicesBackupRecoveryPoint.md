---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 8223172994eb4fdbea3c887f788c4b0e445e0202
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574227"
---
# <span data-ttu-id="9cbc3-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9cbc3-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="9cbc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbc3-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cbc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cbc3-104">SYNTAX</span></span>

### <span data-ttu-id="9cbc3-105">NoFilterParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9cbc3-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9cbc3-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="9cbc3-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cbc3-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9cbc3-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cbc3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cbc3-108">DESCRIPTION</span></span>
<span data-ttu-id="9cbc3-109">Cmdleten **Get-AzureRmRecoveryServicesBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="9cbc3-110">När ett objekt har säkerhetskopierats har ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="9cbc3-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9cbc3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cbc3-112">EXAMPLES</span></span>

### <span data-ttu-id="9cbc3-113">Exempel 1: Hämta återställnings punkter från den förra veckan för ett objekt</span><span class="sxs-lookup"><span data-stu-id="9cbc3-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="9cbc3-114">Det första kommandot får datum från sju dagar sedan och lagrar det sedan i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="9cbc3-115">Det andra kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="9cbc3-116">Det tredje kommandot får AzureVM säkerhets kopierings behållare och lagrar dem i $Containers variabel.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="9cbc3-117">Det fjärde kommandot får det säkerhets kopie objekt som heter V2VM och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="9cbc3-118">Det sista kommandot får en matris med återställnings punkter för objektet i $BackupItem och lagrar dem i $RP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="9cbc3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cbc3-119">PARAMETERS</span></span>

### <span data-ttu-id="9cbc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbc3-120">-DefaultProfile</span></span>
<span data-ttu-id="9cbc3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cbc3-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9cbc3-122">-EndDate</span></span>
<span data-ttu-id="9cbc3-123">Anger slutet av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-123">Specifies the end of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-124">-Objekt</span><span class="sxs-lookup"><span data-stu-id="9cbc3-124">-Item</span></span>
<span data-ttu-id="9cbc3-125">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="9cbc3-126">Använd Get-AzureRmRecoveryServicesBackupItem cmdlet för att få ett **AzureRmRecoveryServicesBackupItem** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="9cbc3-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="9cbc3-128">Anger platsen där indatafilen ska hämtas för att återställa Key Vault-tangenten för en krypterad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="9cbc3-129">-RecoveryPointId</span></span>
<span data-ttu-id="9cbc3-130">Anger återställnings punkt-ID.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-130">Specifies the recovery point ID.</span></span>

```yaml
Type: String
Parameter Sets: RecoveryPointId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9cbc3-131">-StartDate</span></span>
<span data-ttu-id="9cbc3-132">Anger början av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-132">Specifies the start of the date range.</span></span>

```yaml
Type: DateTime
Parameter Sets: DateTimeFilter
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbc3-133">CommonParameters</span></span>
<span data-ttu-id="9cbc3-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbc3-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbc3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbc3-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cbc3-136">INPUTS</span></span>

### <span data-ttu-id="9cbc3-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="9cbc3-137">ItemBase</span></span>
<span data-ttu-id="9cbc3-138">Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9cbc3-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="9cbc3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cbc3-139">OUTPUTS</span></span>

### <span data-ttu-id="9cbc3-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9cbc3-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="9cbc3-141">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. RecoveryPointBase]</span><span class="sxs-lookup"><span data-stu-id="9cbc3-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="9cbc3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cbc3-142">NOTES</span></span>

## <span data-ttu-id="9cbc3-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cbc3-143">RELATED LINKS</span></span>

[<span data-ttu-id="9cbc3-144">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9cbc3-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9cbc3-145">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9cbc3-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


