---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 07406378df0439171c5be2e7558e8ac33cb32687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755690"
---
# <span data-ttu-id="dc396-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="dc396-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="dc396-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc396-102">SYNOPSIS</span></span>
<span data-ttu-id="dc396-103">Inaktiverar skydd för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="dc396-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc396-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc396-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc396-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc396-105">DESCRIPTION</span></span>
<span data-ttu-id="dc396-106">Cmdleten **disable-AzureRmRecoveryServicesBackupProtection** inaktiverar skyddet för ett Azure Backup-skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="dc396-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="dc396-107">Denna cmdlet stoppar regelbunden schemalagd säkerhets kopiering av ett objekt.</span><span class="sxs-lookup"><span data-stu-id="dc396-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="dc396-108">Denna cmdlet kan också ta bort befintliga återställnings punkter för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="dc396-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="dc396-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc396-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="dc396-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc396-110">EXAMPLES</span></span>

### <span data-ttu-id="dc396-111">Exempel 1: inaktivera säkerhets kopierings skydd</span><span class="sxs-lookup"><span data-stu-id="dc396-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="dc396-112">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="dc396-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="dc396-113">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="dc396-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="dc396-114">Det senaste kommandot inaktiverar säkerhets kopierings skydd för objektet i $PI \[ 0 \] men behåller data.</span><span class="sxs-lookup"><span data-stu-id="dc396-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="dc396-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc396-115">PARAMETERS</span></span>

### <span data-ttu-id="dc396-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc396-116">-DefaultProfile</span></span>
<span data-ttu-id="dc396-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc396-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc396-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dc396-118">-Force</span></span>
<span data-ttu-id="dc396-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dc396-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc396-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="dc396-120">-Item</span></span>
<span data-ttu-id="dc396-121">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="dc396-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="dc396-122">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="dc396-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc396-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="dc396-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="dc396-124">Anger att den här cmdleten tar bort befintliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="dc396-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="dc396-125">Om du vill ta bort lagrade återställnings punkter senare kör du denna cmdlet igen och anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="dc396-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc396-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dc396-126">-VaultId</span></span>
<span data-ttu-id="dc396-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="dc396-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="dc396-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc396-128">-Confirm</span></span>
<span data-ttu-id="dc396-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc396-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc396-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc396-130">-WhatIf</span></span>
<span data-ttu-id="dc396-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc396-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc396-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc396-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc396-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc396-133">CommonParameters</span></span>
<span data-ttu-id="dc396-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc396-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc396-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc396-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc396-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc396-136">INPUTS</span></span>

### <span data-ttu-id="dc396-137">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="dc396-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="dc396-138">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc396-138">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="dc396-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc396-139">System.String</span></span>
<span data-ttu-id="dc396-140">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dc396-140">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="dc396-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc396-141">OUTPUTS</span></span>

### <span data-ttu-id="dc396-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="dc396-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="dc396-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc396-143">NOTES</span></span>

## <span data-ttu-id="dc396-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc396-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc396-145">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="dc396-145">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="dc396-146">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="dc396-146">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="dc396-147">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="dc396-147">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


