---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: ce44ac04914419fa2551062b28108abeca9d4249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758338"
---
# <span data-ttu-id="cf401-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cf401-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="cf401-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf401-102">SYNOPSIS</span></span>
<span data-ttu-id="cf401-103">Väntar på att ett säkerhets kopierings jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="cf401-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf401-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf401-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf401-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf401-105">DESCRIPTION</span></span>
<span data-ttu-id="cf401-106">Cmdleten **wait-AzureRmBackupJob** väntar på att ett Azure Backup-jobb ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="cf401-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="cf401-107">Det kan ta lång tid att säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="cf401-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="cf401-108">Om du kör ett säkerhets kopierings jobb som en del av ett skript kanske du vill tvinga skriptet att vänta på jobbet innan det fortsätter med andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cf401-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="cf401-109">Ett skript som innehåller denna cmdlet kan vara enklare än en som Avsök säkerhets kopierings tjänsten för jobb statusen.</span><span class="sxs-lookup"><span data-stu-id="cf401-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="cf401-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf401-110">EXAMPLES</span></span>

## <span data-ttu-id="cf401-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf401-111">PARAMETERS</span></span>

### <span data-ttu-id="cf401-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf401-112">-DefaultProfile</span></span>
<span data-ttu-id="cf401-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cf401-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf401-114">-Jobb</span><span class="sxs-lookup"><span data-stu-id="cf401-114">-Job</span></span>
<span data-ttu-id="cf401-115">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="cf401-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="cf401-116">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="cf401-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf401-117">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="cf401-117">-TimeOut</span></span>
<span data-ttu-id="cf401-118">Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska avslutas.</span><span class="sxs-lookup"><span data-stu-id="cf401-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="cf401-119">Vi rekommenderar att du anger ett timeout-värde.</span><span class="sxs-lookup"><span data-stu-id="cf401-119">We recommend that you specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf401-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf401-120">CommonParameters</span></span>
<span data-ttu-id="cf401-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf401-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf401-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf401-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf401-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf401-123">INPUTS</span></span>

### <span data-ttu-id="cf401-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cf401-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="cf401-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf401-125">OUTPUTS</span></span>

### <span data-ttu-id="cf401-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="cf401-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="cf401-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf401-127">NOTES</span></span>

## <span data-ttu-id="cf401-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf401-128">RELATED LINKS</span></span>

[<span data-ttu-id="cf401-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cf401-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="cf401-130">Stopp-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="cf401-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


