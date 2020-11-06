---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7235c70eae1ab7b93340e68bbb705c17b74c3408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574245"
---
# <span data-ttu-id="f63bb-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f63bb-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="f63bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f63bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f63bb-103">Inaktiverar skydd för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="f63bb-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f63bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f63bb-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f63bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f63bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f63bb-106">Cmdleten **disable-AzureRmRecoveryServicesBackupProtection** inaktiverar skyddet för ett Azure Backup-skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="f63bb-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="f63bb-107">Denna cmdlet stoppar regelbunden schemalagd säkerhets kopiering av ett objekt.</span><span class="sxs-lookup"><span data-stu-id="f63bb-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="f63bb-108">Denna cmdlet kan också ta bort befintliga återställnings punkter för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="f63bb-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="f63bb-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f63bb-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f63bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f63bb-110">EXAMPLES</span></span>

### <span data-ttu-id="f63bb-111">Exempel 1: inaktivera säkerhets kopierings skydd</span><span class="sxs-lookup"><span data-stu-id="f63bb-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="f63bb-112">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="f63bb-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="f63bb-113">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="f63bb-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="f63bb-114">Det senaste kommandot inaktiverar säkerhets kopierings skydd för objektet i $PI \[ 0 \] men behåller data.</span><span class="sxs-lookup"><span data-stu-id="f63bb-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="f63bb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f63bb-115">PARAMETERS</span></span>

### <span data-ttu-id="f63bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63bb-116">-DefaultProfile</span></span>
<span data-ttu-id="f63bb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f63bb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f63bb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f63bb-118">-Force</span></span>
<span data-ttu-id="f63bb-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f63bb-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f63bb-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="f63bb-120">-Item</span></span>
<span data-ttu-id="f63bb-121">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="f63bb-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="f63bb-122">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="f63bb-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f63bb-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="f63bb-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="f63bb-124">Anger att den här cmdleten tar bort befintliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="f63bb-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="f63bb-125">Om du vill ta bort lagrade återställnings punkter senare kör du denna cmdlet igen och anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="f63bb-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63bb-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f63bb-126">-Confirm</span></span>
<span data-ttu-id="f63bb-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f63bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f63bb-128">-WhatIf</span></span>
<span data-ttu-id="f63bb-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f63bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f63bb-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f63bb-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f63bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63bb-131">CommonParameters</span></span>
<span data-ttu-id="f63bb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f63bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63bb-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63bb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63bb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f63bb-134">INPUTS</span></span>

### <span data-ttu-id="f63bb-135">ItemBase</span><span class="sxs-lookup"><span data-stu-id="f63bb-135">ItemBase</span></span>
<span data-ttu-id="f63bb-136">Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f63bb-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="f63bb-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f63bb-137">OUTPUTS</span></span>

### <span data-ttu-id="f63bb-138">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f63bb-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f63bb-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f63bb-139">NOTES</span></span>

## <span data-ttu-id="f63bb-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f63bb-140">RELATED LINKS</span></span>

[<span data-ttu-id="f63bb-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f63bb-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="f63bb-142">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f63bb-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="f63bb-143">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f63bb-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


