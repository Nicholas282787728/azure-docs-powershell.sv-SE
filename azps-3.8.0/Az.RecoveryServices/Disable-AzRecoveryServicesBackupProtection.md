---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: d0b2d15b3f2515969e423e8ac8d019a1413fcad7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927706"
---
# <span data-ttu-id="4976c-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4976c-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="4976c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4976c-102">SYNOPSIS</span></span>
<span data-ttu-id="4976c-103">Inaktiverar skydd för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="4976c-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="4976c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4976c-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4976c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4976c-105">DESCRIPTION</span></span>
<span data-ttu-id="4976c-106">Cmdleten **disable-AzRecoveryServicesBackupProtection** inaktiverar skyddet för ett Azure Backup-skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="4976c-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="4976c-107">Denna cmdlet stoppar regelbunden schemalagd säkerhets kopiering av ett objekt.</span><span class="sxs-lookup"><span data-stu-id="4976c-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="4976c-108">Denna cmdlet kan också ta bort befintliga återställnings punkter för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="4976c-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="4976c-109">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4976c-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4976c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4976c-110">EXAMPLES</span></span>

### <span data-ttu-id="4976c-111">Exempel 1: inaktivera säkerhets kopierings skydd</span><span class="sxs-lookup"><span data-stu-id="4976c-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="4976c-112">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="4976c-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="4976c-113">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="4976c-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="4976c-114">Det senaste kommandot inaktiverar säkerhets kopierings skydd för objektet i $PI \[ 0 \] men behåller data.</span><span class="sxs-lookup"><span data-stu-id="4976c-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="4976c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4976c-115">PARAMETERS</span></span>

### <span data-ttu-id="4976c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4976c-116">-DefaultProfile</span></span>
<span data-ttu-id="4976c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4976c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4976c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4976c-118">-Force</span></span>
<span data-ttu-id="4976c-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4976c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4976c-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="4976c-120">-Item</span></span>
<span data-ttu-id="4976c-121">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="4976c-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="4976c-122">För att få en **AzureRmRecoveryServicesBackupItem** , Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="4976c-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="4976c-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="4976c-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="4976c-124">Anger att den här cmdleten tar bort befintliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="4976c-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="4976c-125">Om du vill ta bort lagrade återställnings punkter senare kör du denna cmdlet igen och anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="4976c-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

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

### <span data-ttu-id="4976c-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4976c-126">-VaultId</span></span>
<span data-ttu-id="4976c-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4976c-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4976c-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4976c-128">-Confirm</span></span>
<span data-ttu-id="4976c-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4976c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4976c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4976c-130">-WhatIf</span></span>
<span data-ttu-id="4976c-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4976c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4976c-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4976c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4976c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4976c-133">CommonParameters</span></span>
<span data-ttu-id="4976c-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4976c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4976c-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4976c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4976c-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4976c-136">INPUTS</span></span>

### <span data-ttu-id="4976c-137">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="4976c-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="4976c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4976c-138">System.String</span></span>

## <span data-ttu-id="4976c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4976c-139">OUTPUTS</span></span>

### <span data-ttu-id="4976c-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4976c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4976c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4976c-141">NOTES</span></span>

## <span data-ttu-id="4976c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4976c-142">RELATED LINKS</span></span>

[<span data-ttu-id="4976c-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="4976c-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="4976c-144">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4976c-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="4976c-145">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4976c-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


