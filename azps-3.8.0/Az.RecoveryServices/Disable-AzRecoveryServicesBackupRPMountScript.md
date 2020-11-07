---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 5796abe47efd1ca6d68aee3663d1bbb810e80ba7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927577"
---
# <span data-ttu-id="b53c8-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b53c8-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b53c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b53c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b53c8-103">Demonterar alla filer för återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="b53c8-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="b53c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b53c8-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b53c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b53c8-105">DESCRIPTION</span></span>
<span data-ttu-id="b53c8-106">Disable-AzRecoveryServicesBackupRPMountScript cmdlet demonterar filerna för återställnings punkten som monterades tidigare med Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b53c8-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="b53c8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b53c8-107">EXAMPLES</span></span>

### <span data-ttu-id="b53c8-108">Exempel 1: demontera en återställnings punkt</span><span class="sxs-lookup"><span data-stu-id="b53c8-108">Example 1: Dismount a recovery point</span></span>
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

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="b53c8-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b53c8-109">PARAMETERS</span></span>

### <span data-ttu-id="b53c8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53c8-110">-DefaultProfile</span></span>
<span data-ttu-id="b53c8-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b53c8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b53c8-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b53c8-112">-PassThru</span></span>
<span data-ttu-id="b53c8-113">Returnera återställnings punkten.</span><span class="sxs-lookup"><span data-stu-id="b53c8-113">Return the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b53c8-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b53c8-114">-RecoveryPoint</span></span>
<span data-ttu-id="b53c8-115">Återställnings punkt objekt som ska återställas</span><span class="sxs-lookup"><span data-stu-id="b53c8-115">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="b53c8-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b53c8-116">-VaultId</span></span>
<span data-ttu-id="b53c8-117">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b53c8-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b53c8-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b53c8-118">-Confirm</span></span>
<span data-ttu-id="b53c8-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b53c8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b53c8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b53c8-120">-WhatIf</span></span>
<span data-ttu-id="b53c8-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b53c8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b53c8-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b53c8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b53c8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53c8-123">CommonParameters</span></span>
<span data-ttu-id="b53c8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53c8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53c8-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b53c8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53c8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b53c8-126">INPUTS</span></span>

### <span data-ttu-id="b53c8-127">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b53c8-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="b53c8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b53c8-128">System.String</span></span>

## <span data-ttu-id="b53c8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b53c8-129">OUTPUTS</span></span>

### <span data-ttu-id="b53c8-130">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b53c8-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b53c8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b53c8-131">NOTES</span></span>

## <span data-ttu-id="b53c8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b53c8-132">RELATED LINKS</span></span>
