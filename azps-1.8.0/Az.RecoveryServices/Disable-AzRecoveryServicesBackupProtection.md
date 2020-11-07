---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 4c023de04cb431e18dc027c0ca3563aa6a2410e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747488"
---
# <span data-ttu-id="c3608-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c3608-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c3608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3608-102">SYNOPSIS</span></span>
<span data-ttu-id="c3608-103">Inaktiverar skydd för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="c3608-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="c3608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3608-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3608-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3608-105">DESCRIPTION</span></span>
<span data-ttu-id="c3608-106">Cmdleten **disable-AzRecoveryServicesBackupProtection** inaktiverar skyddet för ett Azure Backup-skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="c3608-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="c3608-107">Denna cmdlet stoppar regelbunden schemalagd säkerhets kopiering av ett objekt.</span><span class="sxs-lookup"><span data-stu-id="c3608-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="c3608-108">Denna cmdlet kan också ta bort befintliga återställnings punkter för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="c3608-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="c3608-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3608-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c3608-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3608-110">EXAMPLES</span></span>

### <span data-ttu-id="c3608-111">Exempel 1: inaktivera säkerhets kopierings skydd</span><span class="sxs-lookup"><span data-stu-id="c3608-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="c3608-112">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="c3608-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="c3608-113">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="c3608-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="c3608-114">Det senaste kommandot inaktiverar säkerhets kopierings skydd för objektet i $PI \[ 0 \] men behåller data.</span><span class="sxs-lookup"><span data-stu-id="c3608-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="c3608-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3608-115">PARAMETERS</span></span>

### <span data-ttu-id="c3608-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3608-116">-DefaultProfile</span></span>
<span data-ttu-id="c3608-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3608-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3608-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c3608-118">-Force</span></span>
<span data-ttu-id="c3608-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3608-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3608-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="c3608-120">-Item</span></span>
<span data-ttu-id="c3608-121">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="c3608-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="c3608-122">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c3608-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="c3608-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="c3608-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="c3608-124">Anger att den här cmdleten tar bort befintliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="c3608-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="c3608-125">Om du vill ta bort lagrade återställnings punkter senare kör du denna cmdlet igen och anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c3608-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="c3608-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c3608-126">-VaultId</span></span>
<span data-ttu-id="c3608-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c3608-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c3608-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3608-128">-Confirm</span></span>
<span data-ttu-id="c3608-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3608-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3608-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3608-130">-WhatIf</span></span>
<span data-ttu-id="c3608-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3608-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3608-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3608-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3608-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3608-133">CommonParameters</span></span>
<span data-ttu-id="c3608-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3608-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3608-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3608-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3608-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3608-136">INPUTS</span></span>

### <span data-ttu-id="c3608-137">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="c3608-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="c3608-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c3608-138">System.String</span></span>

## <span data-ttu-id="c3608-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3608-139">OUTPUTS</span></span>

### <span data-ttu-id="c3608-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c3608-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c3608-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3608-141">NOTES</span></span>

## <span data-ttu-id="c3608-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3608-142">RELATED LINKS</span></span>

[<span data-ttu-id="c3608-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c3608-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c3608-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c3608-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="c3608-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c3608-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


