---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270784"
---
# <span data-ttu-id="a5aff-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a5aff-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a5aff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5aff-102">SYNOPSIS</span></span>

<span data-ttu-id="a5aff-103">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="a5aff-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="a5aff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5aff-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5aff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5aff-105">DESCRIPTION</span></span>

<span data-ttu-id="a5aff-106">**Säkerhets kopiering-AzRecoveryServicesBackupItem** cmdlet utför en adhoc-säkerhets kopiering av skyddat Azure Backup-objekt.</span><span class="sxs-lookup"><span data-stu-id="a5aff-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="a5aff-107">Med denna cmdlet kan du göra en initial säkerhets kopia omedelbart efter att du har aktiverat skyddet eller starta en säkerhets kopia om en schemalagd säkerhets kopiering Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="a5aff-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="a5aff-108">Denna cmdlet kan också användas för anpassad bevarande med eller utan utgångs datum-se parameter hjälp text för mer information.</span><span class="sxs-lookup"><span data-stu-id="a5aff-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="a5aff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5aff-109">EXAMPLES</span></span>

### <span data-ttu-id="a5aff-110">Exempel 1: starta en säkerhets kopia av ett säkerhets kopie objekt</span><span class="sxs-lookup"><span data-stu-id="a5aff-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="a5aff-111">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM med namnet pstestv2vm1 och lagrar den sedan i $NamedContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="a5aff-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="a5aff-112">Det andra kommandot får det säkerhets kopie objekt som motsvarar behållaren i $NamedContainer och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="a5aff-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="a5aff-113">Det sista kommandot utlöser säkerhets kopierings jobbet i $Item.</span><span class="sxs-lookup"><span data-stu-id="a5aff-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="a5aff-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a5aff-114">Example 2</span></span>

<span data-ttu-id="a5aff-115">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="a5aff-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="a5aff-116">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="a5aff-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="a5aff-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5aff-117">PARAMETERS</span></span>

### <span data-ttu-id="a5aff-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="a5aff-118">-BackupType</span></span>

<span data-ttu-id="a5aff-119">Typ av säkerhets kopiering som ska utföras</span><span class="sxs-lookup"><span data-stu-id="a5aff-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="a5aff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5aff-120">-DefaultProfile</span></span>

<span data-ttu-id="a5aff-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5aff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5aff-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="a5aff-122">-EnableCompression</span></span>

<span data-ttu-id="a5aff-123">Om Aktivera komprimering krävs</span><span class="sxs-lookup"><span data-stu-id="a5aff-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="a5aff-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="a5aff-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="a5aff-125">Anger en förfallo tid för återställnings punkten som ett DateTime-objekt, om inget anges används standardvärdet 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="a5aff-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="a5aff-126">Gäller endast för VM, SQL (endast för kopia-fullständig säkerhets kopierings typ), AFS-säkerhetskopierade objekt.</span><span class="sxs-lookup"><span data-stu-id="a5aff-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="a5aff-127">-Objekt</span><span class="sxs-lookup"><span data-stu-id="a5aff-127">-Item</span></span>

<span data-ttu-id="a5aff-128">Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.</span><span class="sxs-lookup"><span data-stu-id="a5aff-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="a5aff-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a5aff-129">-VaultId</span></span>

<span data-ttu-id="a5aff-130">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a5aff-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a5aff-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5aff-131">-Confirm</span></span>

<span data-ttu-id="a5aff-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5aff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5aff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5aff-133">-WhatIf</span></span>

<span data-ttu-id="a5aff-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5aff-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="a5aff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5aff-135">CommonParameters</span></span>
<span data-ttu-id="a5aff-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5aff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5aff-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5aff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5aff-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5aff-138">INPUTS</span></span>

### <span data-ttu-id="a5aff-139">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="a5aff-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="a5aff-140">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a5aff-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a5aff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a5aff-141">System.String</span></span>

## <span data-ttu-id="a5aff-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5aff-142">OUTPUTS</span></span>

### <span data-ttu-id="a5aff-143">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="a5aff-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a5aff-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5aff-144">NOTES</span></span>

## <span data-ttu-id="a5aff-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5aff-145">RELATED LINKS</span></span>

[<span data-ttu-id="a5aff-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a5aff-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a5aff-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a5aff-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a5aff-148">Återställ-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a5aff-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
