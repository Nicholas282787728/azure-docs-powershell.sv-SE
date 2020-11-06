---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576131"
---
# <span data-ttu-id="67a7f-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="67a7f-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="67a7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="67a7f-103">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="67a7f-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67a7f-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67a7f-105">DESCRIPTION</span></span>
<span data-ttu-id="67a7f-106">**Säkerhets kopiering-AzureRmRecoveryServicesBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="67a7f-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="67a7f-107">Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="67a7f-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="67a7f-108">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67a7f-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="67a7f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67a7f-109">EXAMPLES</span></span>

### <span data-ttu-id="67a7f-110">Exempel 1: starta en säkerhets kopia av ett säkerhets kopie objekt</span><span class="sxs-lookup"><span data-stu-id="67a7f-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="67a7f-111">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM med namnet pstestv2vm1 och lagrar den sedan i $NamedContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="67a7f-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="67a7f-112">Det andra kommandot får det säkerhets kopie objekt som motsvarar behållaren i $NamedContainer och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="67a7f-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="67a7f-113">Det sista kommandot utlöser säkerhets kopierings jobbet i $Item.</span><span class="sxs-lookup"><span data-stu-id="67a7f-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="67a7f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67a7f-114">PARAMETERS</span></span>

### <span data-ttu-id="67a7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a7f-115">-DefaultProfile</span></span>
<span data-ttu-id="67a7f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67a7f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a7f-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="67a7f-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="67a7f-118">Anger en förfallo tid som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="67a7f-118">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="67a7f-119">-Objekt</span><span class="sxs-lookup"><span data-stu-id="67a7f-119">-Item</span></span>
<span data-ttu-id="67a7f-120">Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.</span><span class="sxs-lookup"><span data-stu-id="67a7f-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="67a7f-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="67a7f-121">-VaultId</span></span>
<span data-ttu-id="67a7f-122">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="67a7f-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="67a7f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67a7f-123">-Confirm</span></span>
<span data-ttu-id="67a7f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67a7f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a7f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a7f-125">-WhatIf</span></span>
<span data-ttu-id="67a7f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67a7f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67a7f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67a7f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a7f-128">CommonParameters</span></span>
<span data-ttu-id="67a7f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a7f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a7f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a7f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67a7f-131">INPUTS</span></span>

### <span data-ttu-id="67a7f-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="67a7f-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="67a7f-133">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67a7f-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="67a7f-134">System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="67a7f-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="67a7f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="67a7f-135">System.String</span></span>
<span data-ttu-id="67a7f-136">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67a7f-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="67a7f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67a7f-137">OUTPUTS</span></span>

### <span data-ttu-id="67a7f-138">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="67a7f-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="67a7f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67a7f-139">NOTES</span></span>

## <span data-ttu-id="67a7f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67a7f-140">RELATED LINKS</span></span>

[<span data-ttu-id="67a7f-141">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="67a7f-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="67a7f-142">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="67a7f-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="67a7f-143">Återställ-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="67a7f-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


