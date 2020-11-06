---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575330"
---
# <span data-ttu-id="4e6a9-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4e6a9-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="4e6a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6a9-103">Avbryter ett befintligt säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e6a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e6a9-104">SYNTAX</span></span>

### <span data-ttu-id="4e6a9-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="4e6a9-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e6a9-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="4e6a9-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e6a9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e6a9-107">DESCRIPTION</span></span>
<span data-ttu-id="4e6a9-108">Cmdleten **Stop-AzureRmBackupJob** avbryter ett befintligt Azure Backup-jobb.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="4e6a9-109">Använd den här parametern för att stoppa ett jobb som tar för lång tid att blockera andra aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="4e6a9-110">Du kan bara avbryta följande typer av jobb:</span><span class="sxs-lookup"><span data-stu-id="4e6a9-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="4e6a9-111">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="4e6a9-111">Backup</span></span>
- <span data-ttu-id="4e6a9-112">Terställa</span><span class="sxs-lookup"><span data-stu-id="4e6a9-112">Restore</span></span>

## <span data-ttu-id="4e6a9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e6a9-113">EXAMPLES</span></span>

### <span data-ttu-id="4e6a9-114">Exempel 1: stoppa ett säkerhets kopierings jobb med ett jobb-ID</span><span class="sxs-lookup"><span data-stu-id="4e6a9-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="4e6a9-115">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="4e6a9-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4e6a9-116">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="4e6a9-117">Det andra kommandot får ett säkerhets kopierings jobb från valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="4e6a9-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="4e6a9-118">Kommandot lagrar jobbet i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="4e6a9-119">I det här exemplet finns det bara en säkerhets kopierings åtgärd i det angivna valvet.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="4e6a9-120">Det sista kommandot stoppar det jobb som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="4e6a9-121">Exempel 2: stoppa alla återställnings åtgärder</span><span class="sxs-lookup"><span data-stu-id="4e6a9-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="4e6a9-122">Det här kommandot får alla återställnings operationer i valvet i $Vault och överför dem sedan till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e6a9-123">Den aktuella cmdleten stoppar varje jobb.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="4e6a9-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e6a9-124">PARAMETERS</span></span>

### <span data-ttu-id="4e6a9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6a9-125">-DefaultProfile</span></span>
<span data-ttu-id="4e6a9-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4e6a9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e6a9-127">-Jobb</span><span class="sxs-lookup"><span data-stu-id="4e6a9-127">-Job</span></span>
<span data-ttu-id="4e6a9-128">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="4e6a9-129">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e6a9-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="4e6a9-130">-JobID</span></span>
<span data-ttu-id="4e6a9-131">Anger ett jobb som denna cmdlet avbryter.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="4e6a9-132">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6a9-133">-Valv</span><span class="sxs-lookup"><span data-stu-id="4e6a9-133">-Vault</span></span>
<span data-ttu-id="4e6a9-134">Anger det säkerhets kopierings valv där denna cmdlet avbryter ett jobb.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="4e6a9-135">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e6a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6a9-136">CommonParameters</span></span>
<span data-ttu-id="4e6a9-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e6a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6a9-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e6a9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6a9-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e6a9-139">INPUTS</span></span>

### <span data-ttu-id="4e6a9-140">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="4e6a9-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="4e6a9-141">Parametrar: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4e6a9-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="4e6a9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e6a9-142">OUTPUTS</span></span>

### <span data-ttu-id="4e6a9-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="4e6a9-143">System.Void</span></span>

## <span data-ttu-id="4e6a9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e6a9-144">NOTES</span></span>

## <span data-ttu-id="4e6a9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e6a9-145">RELATED LINKS</span></span>

[<span data-ttu-id="4e6a9-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4e6a9-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="4e6a9-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4e6a9-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4e6a9-148">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4e6a9-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


