---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578780"
---
# <span data-ttu-id="8ea4b-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8ea4b-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="8ea4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ea4b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ea4b-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ea4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ea4b-104">SYNTAX</span></span>

### <span data-ttu-id="8ea4b-105">NoFilterParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8ea4b-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea4b-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="8ea4b-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ea4b-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="8ea4b-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ea4b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ea4b-108">DESCRIPTION</span></span>
<span data-ttu-id="8ea4b-109">Cmdleten **Get-AzureRmRecoveryServicesBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="8ea4b-110">När ett objekt har säkerhetskopierats har ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="8ea4b-111">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8ea4b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ea4b-112">EXAMPLES</span></span>

### <span data-ttu-id="8ea4b-113">Exempel 1: Hämta återställnings punkter från den förra veckan för ett objekt</span><span class="sxs-lookup"><span data-stu-id="8ea4b-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="8ea4b-114">Det första kommandot får datum från sju dagar sedan och lagrar det sedan i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="8ea4b-115">Det andra kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="8ea4b-116">Det tredje kommandot får AzureVM säkerhets kopierings behållare och lagrar dem i $Containers variabel.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="8ea4b-117">Det fjärde kommandot får det säkerhets kopie objekt som heter V2VM och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="8ea4b-118">Det sista kommandot får en matris med återställnings punkter för objektet i $BackupItem och lagrar dem i $RP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="8ea4b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ea4b-119">PARAMETERS</span></span>

### <span data-ttu-id="8ea4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea4b-120">-DefaultProfile</span></span>
<span data-ttu-id="8ea4b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ea4b-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8ea4b-122">-EndDate</span></span>
<span data-ttu-id="8ea4b-123">Anger slutet av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-123">Specifies the end of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea4b-124">-Objekt</span><span class="sxs-lookup"><span data-stu-id="8ea4b-124">-Item</span></span>
<span data-ttu-id="8ea4b-125">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="8ea4b-126">Använd Get-AzureRmRecoveryServicesBackupItem cmdlet för att få ett **AzureRmRecoveryServicesBackupItem** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea4b-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="8ea4b-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="8ea4b-128">Anger platsen där indatafilen ska hämtas för att återställa Key Vault-tangenten för en krypterad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea4b-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="8ea4b-129">-RecoveryPointId</span></span>
<span data-ttu-id="8ea4b-130">Anger återställnings punkt-ID.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-130">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea4b-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="8ea4b-131">-StartDate</span></span>
<span data-ttu-id="8ea4b-132">Anger början av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-132">Specifies the start of the date range.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea4b-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8ea4b-133">-VaultId</span></span>
<span data-ttu-id="8ea4b-134">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8ea4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea4b-135">CommonParameters</span></span>
<span data-ttu-id="8ea4b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea4b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea4b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ea4b-138">INPUTS</span></span>

### <span data-ttu-id="8ea4b-139">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8ea4b-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="8ea4b-140">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ea4b-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="8ea4b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8ea4b-141">System.String</span></span>
<span data-ttu-id="8ea4b-142">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8ea4b-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="8ea4b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ea4b-143">OUTPUTS</span></span>

### <span data-ttu-id="8ea4b-144">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8ea4b-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="8ea4b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ea4b-145">NOTES</span></span>

## <span data-ttu-id="8ea4b-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ea4b-146">RELATED LINKS</span></span>

[<span data-ttu-id="8ea4b-147">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="8ea4b-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="8ea4b-148">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8ea4b-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


