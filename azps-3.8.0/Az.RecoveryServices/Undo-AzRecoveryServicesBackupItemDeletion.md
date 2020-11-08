---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 80d03117278073b7b80b9c910a5ee4101a9db09a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089337"
---
# <span data-ttu-id="65742-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="65742-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="65742-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65742-102">SYNOPSIS</span></span>
<span data-ttu-id="65742-103">Reslänger ett objekt som inte har tagits bort</span><span class="sxs-lookup"><span data-stu-id="65742-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="65742-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65742-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65742-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65742-105">DESCRIPTION</span></span>
<span data-ttu-id="65742-106">Undo-AzRecoveryServicesBackupItemDeletion cmdlet reslänger ett objekt som inte har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="65742-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="65742-107">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65742-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="65742-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65742-108">EXAMPLES</span></span>

### <span data-ttu-id="65742-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="65742-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="65742-110">Det första kommandot får en matris med säkerhets kopierings containrar och lagrar dem sedan i $Cont matris.</span><span class="sxs-lookup"><span data-stu-id="65742-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="65742-111">Det andra kommandot får det säkerhets kopie objekt som motsvarar det första behållarobjektet och lagrar det sedan i $PI variabel.</span><span class="sxs-lookup"><span data-stu-id="65742-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="65742-112">Det tredje kommandot inaktiverar säkerhets kopiering av objektet i $PI \[ 0 \] och placerar objektet i ett softdeleted-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="65742-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="65742-113">Det fjärde kommandot det nya objektet som är i ett softdeleted-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="65742-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="65742-114">Det sista kommandot rehydratiserar den softdeleted VM.</span><span class="sxs-lookup"><span data-stu-id="65742-114">The last command rehydrates the softdeleted VM.</span></span>

## <span data-ttu-id="65742-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65742-115">PARAMETERS</span></span>

### <span data-ttu-id="65742-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65742-116">-DefaultProfile</span></span>
<span data-ttu-id="65742-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65742-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65742-118">-Force</span><span class="sxs-lookup"><span data-stu-id="65742-118">-Force</span></span>
<span data-ttu-id="65742-119">Force inaktiverar säkerhets kopierings skydd (förhindrar bekräftelse dialog rutan).</span><span class="sxs-lookup"><span data-stu-id="65742-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="65742-120">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="65742-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="65742-121">-Objekt</span><span class="sxs-lookup"><span data-stu-id="65742-121">-Item</span></span>
<span data-ttu-id="65742-122">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="65742-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="65742-123">För att få en AzureRmRecoveryServicesBackupItem, Använd cmdleten Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="65742-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="65742-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="65742-124">-VaultId</span></span>
<span data-ttu-id="65742-125">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="65742-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="65742-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65742-126">-Confirm</span></span>
<span data-ttu-id="65742-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65742-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65742-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65742-128">-WhatIf</span></span>
<span data-ttu-id="65742-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65742-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65742-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65742-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65742-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65742-131">CommonParameters</span></span>
<span data-ttu-id="65742-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65742-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65742-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65742-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65742-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65742-134">INPUTS</span></span>

### <span data-ttu-id="65742-135">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="65742-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="65742-136">System. String</span><span class="sxs-lookup"><span data-stu-id="65742-136">System.String</span></span>

## <span data-ttu-id="65742-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65742-137">OUTPUTS</span></span>

### <span data-ttu-id="65742-138">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="65742-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="65742-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65742-139">NOTES</span></span>

## <span data-ttu-id="65742-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65742-140">RELATED LINKS</span></span>

[<span data-ttu-id="65742-141">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="65742-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="65742-142">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="65742-142">Get-AzRecoveryServicesBackupItem</span></span>]()

