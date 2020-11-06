---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580032"
---
# <span data-ttu-id="e4712-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e4712-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="e4712-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4712-102">SYNOPSIS</span></span>
<span data-ttu-id="e4712-103">Väntar på att ett säkerhets kopierings jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="e4712-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4712-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4712-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4712-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4712-105">DESCRIPTION</span></span>
<span data-ttu-id="e4712-106">Cmdleten **wait-AzureRmRecoveryServicesBackupJob** väntar på att ett Azure Backup-jobb ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="e4712-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="e4712-107">Det kan ta lång tid att säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="e4712-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="e4712-108">Om du kör ett säkerhets kopierings jobb som en del av ett skript kanske du vill tvinga skriptet att vänta på jobbet innan det fortsätter med andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="e4712-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="e4712-109">Ett skript som innehåller denna cmdlet kan vara enklare än en som Avsök säkerhets kopierings tjänsten för jobb statusen.</span><span class="sxs-lookup"><span data-stu-id="e4712-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="e4712-110">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4712-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e4712-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4712-111">EXAMPLES</span></span>

### <span data-ttu-id="e4712-112">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="e4712-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="e4712-113">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="e4712-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="e4712-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4712-114">PARAMETERS</span></span>

### <span data-ttu-id="e4712-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4712-115">-DefaultProfile</span></span>
<span data-ttu-id="e4712-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4712-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4712-117">-Jobb</span><span class="sxs-lookup"><span data-stu-id="e4712-117">-Job</span></span>
<span data-ttu-id="e4712-118">Anger jobb att vänta på.</span><span class="sxs-lookup"><span data-stu-id="e4712-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="e4712-119">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="e4712-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4712-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e4712-120">-Timeout</span></span>
<span data-ttu-id="e4712-121">Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="e4712-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="e4712-122">Vi rekommenderar att du anger ett timeout-värde.</span><span class="sxs-lookup"><span data-stu-id="e4712-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4712-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e4712-123">-VaultId</span></span>
<span data-ttu-id="e4712-124">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="e4712-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e4712-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4712-125">CommonParameters</span></span>
<span data-ttu-id="e4712-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4712-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4712-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4712-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4712-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4712-128">INPUTS</span></span>

### <span data-ttu-id="e4712-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="e4712-129">System.Object</span></span>
<span data-ttu-id="e4712-130">Parametrar: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4712-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="e4712-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e4712-131">System.String</span></span>
<span data-ttu-id="e4712-132">Parametrar: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4712-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="e4712-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4712-133">OUTPUTS</span></span>

### <span data-ttu-id="e4712-134">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e4712-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e4712-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4712-135">NOTES</span></span>

## <span data-ttu-id="e4712-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4712-136">RELATED LINKS</span></span>

[<span data-ttu-id="e4712-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="e4712-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


