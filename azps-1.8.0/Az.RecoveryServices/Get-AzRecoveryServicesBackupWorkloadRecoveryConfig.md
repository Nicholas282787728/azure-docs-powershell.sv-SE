---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747409"
---
# <span data-ttu-id="9e078-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="9e078-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="9e078-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e078-102">SYNOPSIS</span></span>
<span data-ttu-id="9e078-103">Det här kommandot konstruerar återställnings konfigurationen för ett säkerhetskopierat objekt, till exempel SQL DB.</span><span class="sxs-lookup"><span data-stu-id="9e078-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="9e078-104">Konfigurationsobjektet lagrar alla uppgifter, till exempel återställnings läget, mål destinationer för de återställda och programspecifika parametrarna som mål fysiska sökvägar för SQL.</span><span class="sxs-lookup"><span data-stu-id="9e078-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="9e078-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e078-105">SYNTAX</span></span>

### <span data-ttu-id="9e078-106">RpParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9e078-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e078-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e078-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e078-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e078-108">DESCRIPTION</span></span>
<span data-ttu-id="9e078-109">Kommandot returnerar en återställnings konfiguration för AzureWorkload objekt som skickas till cmdleten Restore.</span><span class="sxs-lookup"><span data-stu-id="9e078-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="9e078-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e078-110">EXAMPLES</span></span>

### <span data-ttu-id="9e078-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e078-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="9e078-112">Den första cmdleten används för att hämta återställnings punkt objekt.</span><span class="sxs-lookup"><span data-stu-id="9e078-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="9e078-113">Den andra cmdleten skapar en återställnings plan för återställning av en ursprunglig plats.</span><span class="sxs-lookup"><span data-stu-id="9e078-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="9e078-114">Den tredje cmdleten crreats en återställnings plan för återställning av en alternativ plats.</span><span class="sxs-lookup"><span data-stu-id="9e078-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="9e078-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e078-115">PARAMETERS</span></span>

### <span data-ttu-id="9e078-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="9e078-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="9e078-117">Anger att den säkerhetskopierade databasen ska skrivas över med DB-informationen i återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="9e078-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="9e078-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e078-118">-DefaultProfile</span></span>
<span data-ttu-id="9e078-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e078-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e078-120">-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e078-120">-Item</span></span>
<span data-ttu-id="9e078-121">Anger det säkerhets kopierings objekt som återställningen utförs på.</span><span class="sxs-lookup"><span data-stu-id="9e078-121">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e078-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="9e078-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="9e078-123">Anger att den säkerhetskopierade databasen ska skrivas över med DB-informationen i återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="9e078-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="9e078-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="9e078-124">-PointInTime</span></span>
<span data-ttu-id="9e078-125">Slut tid för tidsintervall för vilken återställnings punkt måste hämtas</span><span class="sxs-lookup"><span data-stu-id="9e078-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e078-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9e078-126">-RecoveryPoint</span></span>
<span data-ttu-id="9e078-127">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="9e078-127">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e078-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="9e078-128">-TargetItem</span></span>
<span data-ttu-id="9e078-129">Anger det mål som ska återställas av databasen.</span><span class="sxs-lookup"><span data-stu-id="9e078-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="9e078-130">För att du ska kunna återställa SQL måste det vara skrivskyddat objekt typen SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="9e078-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e078-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9e078-131">-VaultId</span></span>
<span data-ttu-id="9e078-132">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="9e078-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9e078-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e078-133">-Confirm</span></span>
<span data-ttu-id="9e078-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e078-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e078-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e078-135">-WhatIf</span></span>
<span data-ttu-id="9e078-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e078-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e078-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e078-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e078-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e078-138">CommonParameters</span></span>
<span data-ttu-id="9e078-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e078-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e078-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e078-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e078-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e078-141">INPUTS</span></span>

### <span data-ttu-id="9e078-142">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="9e078-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="9e078-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9e078-143">System.String</span></span>

## <span data-ttu-id="9e078-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e078-144">OUTPUTS</span></span>

### <span data-ttu-id="9e078-145">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="9e078-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="9e078-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e078-146">NOTES</span></span>

## <span data-ttu-id="9e078-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e078-147">RELATED LINKS</span></span>