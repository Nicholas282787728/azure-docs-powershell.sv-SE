---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574232"
---
# <span data-ttu-id="b11bb-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b11bb-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b11bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b11bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b11bb-103">Laddar ned ett skript för att montera alla filer för återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="b11bb-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b11bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b11bb-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b11bb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b11bb-105">DESCRIPTION</span></span>
<span data-ttu-id="b11bb-106">Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet laddar ned ett skript som monterar volymerna på återställnings punkten på den dator där den körs.</span><span class="sxs-lookup"><span data-stu-id="b11bb-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="b11bb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b11bb-107">EXAMPLES</span></span>

### <span data-ttu-id="b11bb-108">Exempel 1: montera en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="b11bb-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="b11bb-109">När skriptet körs monteras filerna på återställnings punkten $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="b11bb-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="b11bb-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b11bb-110">PARAMETERS</span></span>

### <span data-ttu-id="b11bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11bb-111">-DefaultProfile</span></span>
<span data-ttu-id="b11bb-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b11bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b11bb-113">-Path</span><span class="sxs-lookup"><span data-stu-id="b11bb-113">-Path</span></span>
<span data-ttu-id="b11bb-114">Plats där filen ska hämtas om fil återställning.</span><span class="sxs-lookup"><span data-stu-id="b11bb-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="b11bb-115">Om-Path inte anges hämtas skript filen till den aktuella katalogen.</span><span class="sxs-lookup"><span data-stu-id="b11bb-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b11bb-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b11bb-116">-RecoveryPoint</span></span>
<span data-ttu-id="b11bb-117">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="b11bb-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b11bb-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b11bb-118">-Confirm</span></span>
<span data-ttu-id="b11bb-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b11bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b11bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b11bb-120">-WhatIf</span></span>
<span data-ttu-id="b11bb-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b11bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b11bb-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b11bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b11bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11bb-123">CommonParameters</span></span>
<span data-ttu-id="b11bb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11bb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11bb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11bb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b11bb-126">INPUTS</span></span>

### <span data-ttu-id="b11bb-127">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b11bb-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b11bb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b11bb-128">OUTPUTS</span></span>

### <span data-ttu-id="b11bb-129">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="b11bb-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="b11bb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b11bb-130">NOTES</span></span>

## <span data-ttu-id="b11bb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b11bb-131">RELATED LINKS</span></span>

