---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 6c8debac9091d28091695847b36d0cbc1b219125
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919803"
---
# <span data-ttu-id="0f54a-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0f54a-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0f54a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f54a-102">SYNOPSIS</span></span>

<span data-ttu-id="0f54a-103">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="0f54a-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="0f54a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f54a-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f54a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f54a-105">DESCRIPTION</span></span>

<span data-ttu-id="0f54a-106">**Säkerhets kopiering-AzRecoveryServicesBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="0f54a-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="0f54a-107">Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="0f54a-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="0f54a-108">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="0f54a-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0f54a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f54a-109">EXAMPLES</span></span>

### <span data-ttu-id="0f54a-110">Exempel 1: starta en säkerhets kopia av ett säkerhets kopie objekt</span><span class="sxs-lookup"><span data-stu-id="0f54a-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="0f54a-111">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM med namnet pstestv2vm1 och lagrar den sedan i $NamedContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="0f54a-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="0f54a-112">Det andra kommandot får det säkerhets kopie objekt som motsvarar behållaren i $NamedContainer och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="0f54a-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="0f54a-113">Det sista kommandot utlöser säkerhets kopierings jobbet i $Item.</span><span class="sxs-lookup"><span data-stu-id="0f54a-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="0f54a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f54a-114">PARAMETERS</span></span>

### <span data-ttu-id="0f54a-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="0f54a-115">-BackupType</span></span>

<span data-ttu-id="0f54a-116">Typ av säkerhets kopiering som ska utföras</span><span class="sxs-lookup"><span data-stu-id="0f54a-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f54a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f54a-117">-DefaultProfile</span></span>

<span data-ttu-id="0f54a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f54a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f54a-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="0f54a-119">-EnableCompression</span></span>

<span data-ttu-id="0f54a-120">Om Aktivera komprimering krävs</span><span class="sxs-lookup"><span data-stu-id="0f54a-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="0f54a-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="0f54a-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="0f54a-122">Anger en förfallo tid som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0f54a-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f54a-123">-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f54a-123">-Item</span></span>

<span data-ttu-id="0f54a-124">Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.</span><span class="sxs-lookup"><span data-stu-id="0f54a-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f54a-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0f54a-125">-VaultId</span></span>

<span data-ttu-id="0f54a-126">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="0f54a-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0f54a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f54a-127">-Confirm</span></span>

<span data-ttu-id="0f54a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f54a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f54a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f54a-129">-WhatIf</span></span>

<span data-ttu-id="0f54a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f54a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f54a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f54a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f54a-132">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f54a-132">-CommonParameters</span></span>

<span data-ttu-id="0f54a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f54a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f54a-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f54a-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f54a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f54a-135">INPUTS</span></span>

### <span data-ttu-id="0f54a-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="0f54a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0f54a-137">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0f54a-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0f54a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0f54a-138">System.String</span></span>

## <span data-ttu-id="0f54a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f54a-139">OUTPUTS</span></span>

### <span data-ttu-id="0f54a-140">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="0f54a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0f54a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f54a-141">NOTES</span></span>

## <span data-ttu-id="0f54a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f54a-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f54a-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0f54a-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="0f54a-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0f54a-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0f54a-145">Återställ-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0f54a-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
