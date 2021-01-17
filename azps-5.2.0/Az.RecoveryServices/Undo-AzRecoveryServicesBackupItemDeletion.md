---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 62d8dc302dc5819272034cfdd1c3fd0c0c79f54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391288"
---
# <span data-ttu-id="cd494-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="cd494-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="cd494-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd494-102">SYNOPSIS</span></span>
<span data-ttu-id="cd494-103">Om ett säkerhets objekt tas bort och förekommer i ett läget tyst borttag flyttas det här kommandot till ett tillstånd där data behålls för alltid</span><span class="sxs-lookup"><span data-stu-id="cd494-103">If a backup item is deleted and present in a soft-deleted state, this command brings the item back to a state where the data is retained forever</span></span> 

## <span data-ttu-id="cd494-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd494-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd494-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd494-105">DESCRIPTION</span></span>
<span data-ttu-id="cd494-106">Undo-AzRecoveryServicesBackupItemDeletion cmdlet återställer ett borttaget objekt till ett tillstånd där skyddet stoppas men data behålls alltid.</span><span class="sxs-lookup"><span data-stu-id="cd494-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet reverts a soft-deleted item to a state where the protection is stopped but data is retained forever.</span></span>

## <span data-ttu-id="cd494-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd494-107">EXAMPLES</span></span>

### <span data-ttu-id="cd494-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd494-108">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM | Where-Object {$_.DeleteState -eq "ToBeDeleted"}
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="cd494-109">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="cd494-109">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="cd494-110">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="cd494-110">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="cd494-111">Det tredje kommandot inaktiverar säkerhets kopiering av objektet i $PI \[ 0 \] och placerar objektet i ett softdeleted-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="cd494-111">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="cd494-112">Det fjärde kommandot får objektet som är i ett softdeleted-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="cd494-112">The fourth command gets the item which is in a softdeleted state.</span></span>
<span data-ttu-id="cd494-113">Med det senaste kommandot blir softdeleted VM till ett tillstånd där skyddet stoppas, men data behålls alltid.</span><span class="sxs-lookup"><span data-stu-id="cd494-113">The last command brings the softdeleted VM to a state where the protection is stopped but data is retained forever.</span></span>

### <span data-ttu-id="cd494-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd494-114">Example 2</span></span>

<span data-ttu-id="cd494-115">Reslänger ett objekt som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="cd494-115">Rehydrates a soft-deleted Item.</span></span> <span data-ttu-id="cd494-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="cd494-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0] -VaultId $vault.ID
```

## <span data-ttu-id="cd494-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd494-117">PARAMETERS</span></span>

### <span data-ttu-id="cd494-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd494-118">-DefaultProfile</span></span>
<span data-ttu-id="cd494-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd494-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd494-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cd494-120">-Force</span></span>
<span data-ttu-id="cd494-121">Force inaktiverar säkerhets kopierings skydd (förhindrar bekräftelse dialog rutan).</span><span class="sxs-lookup"><span data-stu-id="cd494-121">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="cd494-122">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cd494-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd494-123">-Objekt</span><span class="sxs-lookup"><span data-stu-id="cd494-123">-Item</span></span>
<span data-ttu-id="cd494-124">Anger det säkerhets kopierings objekt som denna cmdlet återställer borttagningen för.</span><span class="sxs-lookup"><span data-stu-id="cd494-124">Specifies the backup item for which this cmdlet reverts the deletion.</span></span>
<span data-ttu-id="cd494-125">För att få en AzureRmRecoveryServicesBackupItem, Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="cd494-125">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="cd494-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cd494-126">-VaultId</span></span>
<span data-ttu-id="cd494-127">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="cd494-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cd494-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd494-128">-Confirm</span></span>
<span data-ttu-id="cd494-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd494-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd494-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd494-130">-WhatIf</span></span>
<span data-ttu-id="cd494-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd494-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd494-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd494-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd494-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd494-133">CommonParameters</span></span>
<span data-ttu-id="cd494-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd494-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd494-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd494-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd494-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd494-136">INPUTS</span></span>

### <span data-ttu-id="cd494-137">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="cd494-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="cd494-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd494-138">System.String</span></span>

## <span data-ttu-id="cd494-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd494-139">OUTPUTS</span></span>

### <span data-ttu-id="cd494-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="cd494-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="cd494-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd494-141">NOTES</span></span>

## <span data-ttu-id="cd494-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd494-142">RELATED LINKS</span></span>

[<span data-ttu-id="cd494-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="cd494-143">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="cd494-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="cd494-144">Get-AzRecoveryServicesBackupItem</span></span>]()

