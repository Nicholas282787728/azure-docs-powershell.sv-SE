---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393851"
---
# <span data-ttu-id="48791-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="48791-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="48791-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48791-102">SYNOPSIS</span></span>

<span data-ttu-id="48791-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="48791-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="48791-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48791-104">SYNTAX</span></span>

### <span data-ttu-id="48791-105">NoFilterParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="48791-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48791-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="48791-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48791-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="48791-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48791-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48791-108">DESCRIPTION</span></span>

<span data-ttu-id="48791-109">Cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="48791-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="48791-110">När ett objekt har säkerhetskopierats har ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="48791-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="48791-111">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="48791-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="48791-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48791-112">EXAMPLES</span></span>

### <span data-ttu-id="48791-113">Exempel 1: Hämta återställnings punkter från den förra veckan för ett objekt</span><span class="sxs-lookup"><span data-stu-id="48791-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="48791-114">Det första kommandot får ett valv-objekt baserat på vaultName.</span><span class="sxs-lookup"><span data-stu-id="48791-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="48791-115">Det andra kommandot får datum från sju dagar sedan och lagrar det sedan i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="48791-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="48791-116">Det tredje kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="48791-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="48791-117">Det fjärde kommandot får AzureVM säkerhets kopierings behållare och lagrar dem i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="48791-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="48791-118">Det femte kommandot hämtar säkerhets kopian baserat på workloadType, vaultId och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="48791-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="48791-119">Det sista kommandot får en matris med återställnings punkter för objektet i $BackupItem och lagrar dem i $RP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="48791-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="48791-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48791-120">PARAMETERS</span></span>

### <span data-ttu-id="48791-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48791-121">-DefaultProfile</span></span>

<span data-ttu-id="48791-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48791-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48791-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="48791-123">-EndDate</span></span>

<span data-ttu-id="48791-124">Anger slutet av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="48791-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="48791-125">-Objekt</span><span class="sxs-lookup"><span data-stu-id="48791-125">-Item</span></span>

<span data-ttu-id="48791-126">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="48791-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="48791-127">För att få ett **AzureRmRecoveryServicesBackupItem** -objekt, Använd cmdleten **Get-AzRecoveryServicesBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="48791-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="48791-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="48791-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="48791-129">Anger platsen där indatafilen ska hämtas för att återställa Key Vault-tangenten för en krypterad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="48791-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="48791-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="48791-130">-RecoveryPointId</span></span>

<span data-ttu-id="48791-131">Anger återställnings punkt-ID.</span><span class="sxs-lookup"><span data-stu-id="48791-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="48791-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="48791-132">-StartDate</span></span>

<span data-ttu-id="48791-133">Anger början av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="48791-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="48791-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="48791-134">-VaultId</span></span>

<span data-ttu-id="48791-135">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="48791-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="48791-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48791-136">CommonParameters</span></span>
<span data-ttu-id="48791-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48791-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48791-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48791-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48791-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48791-139">INPUTS</span></span>

### <span data-ttu-id="48791-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="48791-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="48791-141">System. String</span><span class="sxs-lookup"><span data-stu-id="48791-141">System.String</span></span>

## <span data-ttu-id="48791-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48791-142">OUTPUTS</span></span>

### <span data-ttu-id="48791-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="48791-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="48791-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48791-144">NOTES</span></span>

## <span data-ttu-id="48791-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48791-145">RELATED LINKS</span></span>

[<span data-ttu-id="48791-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="48791-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="48791-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="48791-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
