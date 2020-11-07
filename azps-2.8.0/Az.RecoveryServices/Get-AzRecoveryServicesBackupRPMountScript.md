---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6301c621de4399509c70271eb318983e91ebd121
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919740"
---
# <span data-ttu-id="ce57b-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="ce57b-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="ce57b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce57b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce57b-103">Laddar ned ett skript för att montera alla filer för återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="ce57b-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="ce57b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce57b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce57b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce57b-105">DESCRIPTION</span></span>
<span data-ttu-id="ce57b-106">Get-AzRecoveryServicesBackupRPMountScript cmdlet laddar ned ett skript som monterar volymerna på återställnings punkten på den dator där den körs.</span><span class="sxs-lookup"><span data-stu-id="ce57b-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="ce57b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce57b-107">EXAMPLES</span></span>

### <span data-ttu-id="ce57b-108">Exempel 1: montera en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="ce57b-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="ce57b-109">När skriptet körs monteras filerna på återställnings punkten $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ce57b-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="ce57b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce57b-110">PARAMETERS</span></span>

### <span data-ttu-id="ce57b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce57b-111">-DefaultProfile</span></span>
<span data-ttu-id="ce57b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce57b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce57b-113">-Path</span><span class="sxs-lookup"><span data-stu-id="ce57b-113">-Path</span></span>
<span data-ttu-id="ce57b-114">Plats där filen ska hämtas om fil återställning.</span><span class="sxs-lookup"><span data-stu-id="ce57b-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="ce57b-115">Om-Path inte anges hämtas skript filen till den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="ce57b-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce57b-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ce57b-116">-RecoveryPoint</span></span>
<span data-ttu-id="ce57b-117">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="ce57b-117">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce57b-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ce57b-118">-VaultId</span></span>
<span data-ttu-id="ce57b-119">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="ce57b-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ce57b-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ce57b-120">-Confirm</span></span>
<span data-ttu-id="ce57b-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ce57b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce57b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce57b-122">-WhatIf</span></span>
<span data-ttu-id="ce57b-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ce57b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce57b-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ce57b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce57b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce57b-125">CommonParameters</span></span>
<span data-ttu-id="ce57b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce57b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce57b-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce57b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce57b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce57b-128">INPUTS</span></span>

### <span data-ttu-id="ce57b-129">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="ce57b-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="ce57b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ce57b-130">System.String</span></span>

## <span data-ttu-id="ce57b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce57b-131">OUTPUTS</span></span>

### <span data-ttu-id="ce57b-132">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="ce57b-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="ce57b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce57b-133">NOTES</span></span>

## <span data-ttu-id="ce57b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce57b-134">RELATED LINKS</span></span>
