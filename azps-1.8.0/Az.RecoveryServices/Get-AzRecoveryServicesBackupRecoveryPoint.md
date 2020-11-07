---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9a5d0f0607692217cf4016a1261f23b725d07e68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747418"
---
# <span data-ttu-id="93590-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="93590-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="93590-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93590-102">SYNOPSIS</span></span>
<span data-ttu-id="93590-103">Hämtar återställnings punkterna för ett säkerhetskopierat objekt.</span><span class="sxs-lookup"><span data-stu-id="93590-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="93590-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93590-104">SYNTAX</span></span>

### <span data-ttu-id="93590-105">NoFilterParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="93590-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93590-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="93590-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93590-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="93590-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93590-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93590-108">DESCRIPTION</span></span>
<span data-ttu-id="93590-109">Cmdleten **Get-AzRecoveryServicesBackupRecoveryPoint** hämtar återställnings punkterna för ett säkerhetskopierat Azure-säkerhetsobjekt.</span><span class="sxs-lookup"><span data-stu-id="93590-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="93590-110">När ett objekt har säkerhetskopierats har ett **AzureRmRecoveryServicesBackupRecoveryPoint** -objekt en eller flera återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="93590-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="93590-111">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93590-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="93590-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93590-112">EXAMPLES</span></span>

### <span data-ttu-id="93590-113">Exempel 1: Hämta återställnings punkter från den förra veckan för ett objekt</span><span class="sxs-lookup"><span data-stu-id="93590-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="93590-114">Det första kommandot får datum från sju dagar sedan och lagrar det sedan i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="93590-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="93590-115">Det andra kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="93590-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="93590-116">Det tredje kommandot får AzureVM säkerhets kopierings behållare och lagrar dem i $Containers variabel.</span><span class="sxs-lookup"><span data-stu-id="93590-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="93590-117">Det fjärde kommandot får det säkerhets kopie objekt som heter V2VM och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="93590-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="93590-118">Det sista kommandot får en matris med återställnings punkter för objektet i $BackupItem och lagrar dem i $RP-variabeln.</span><span class="sxs-lookup"><span data-stu-id="93590-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="93590-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93590-119">PARAMETERS</span></span>

### <span data-ttu-id="93590-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93590-120">-DefaultProfile</span></span>
<span data-ttu-id="93590-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93590-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93590-122">-EndDate</span><span class="sxs-lookup"><span data-stu-id="93590-122">-EndDate</span></span>
<span data-ttu-id="93590-123">Anger slutet av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="93590-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="93590-124">-Objekt</span><span class="sxs-lookup"><span data-stu-id="93590-124">-Item</span></span>
<span data-ttu-id="93590-125">Anger objekt för vilka denna cmdlet hämtar återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="93590-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="93590-126">Använd Get-AzRecoveryServicesBackupItem cmdlet för att få ett **AzureRmRecoveryServicesBackupItem** -objekt.</span><span class="sxs-lookup"><span data-stu-id="93590-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="93590-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="93590-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="93590-128">Anger platsen där indatafilen ska hämtas för att återställa Key Vault-tangenten för en krypterad virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="93590-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="93590-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="93590-129">-RecoveryPointId</span></span>
<span data-ttu-id="93590-130">Anger återställnings punkt-ID.</span><span class="sxs-lookup"><span data-stu-id="93590-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="93590-131">-StartDate</span><span class="sxs-lookup"><span data-stu-id="93590-131">-StartDate</span></span>
<span data-ttu-id="93590-132">Anger början av datum intervallet.</span><span class="sxs-lookup"><span data-stu-id="93590-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="93590-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="93590-133">-VaultId</span></span>
<span data-ttu-id="93590-134">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="93590-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="93590-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93590-135">CommonParameters</span></span>
<span data-ttu-id="93590-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93590-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93590-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93590-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93590-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93590-138">INPUTS</span></span>

### <span data-ttu-id="93590-139">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="93590-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="93590-140">System. String</span><span class="sxs-lookup"><span data-stu-id="93590-140">System.String</span></span>

## <span data-ttu-id="93590-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93590-141">OUTPUTS</span></span>

### <span data-ttu-id="93590-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="93590-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="93590-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93590-143">NOTES</span></span>

## <span data-ttu-id="93590-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93590-144">RELATED LINKS</span></span>

[<span data-ttu-id="93590-145">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="93590-145">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="93590-146">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="93590-146">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


