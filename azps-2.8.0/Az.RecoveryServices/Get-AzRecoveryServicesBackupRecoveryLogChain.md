---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: d06cae4fc13151d8b1c5c2b0fb4dd7803606fe49
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919739"
---
# <span data-ttu-id="3fe8a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="3fe8a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="3fe8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fe8a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe8a-103">Det här kommandot listar start-och slut punkterna för den felaktiga logg kedjan för det angivna säkerhets kopierings objektet.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="3fe8a-104">Använd den för att avgöra om den tidpunkt då användaren vill återställa databasen ska vara giltig eller inte.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="3fe8a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fe8a-105">SYNTAX</span></span>

### <span data-ttu-id="3fe8a-106">NoFilterParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3fe8a-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fe8a-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="3fe8a-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fe8a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fe8a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fe8a-109">Cmdleten **Get-AzRecoveryServicesBackupRecoveryLogChain** hämtar tidsintervallet för återställning av ett säkerhetskopierat Azure-objekt.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="3fe8a-110">När ett objekt har säkerhetskopierats har ett **AzRecoveryServicesBackupRecoveryLogChain** -objekt ett eller flera återhämtnings tids intervall.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="3fe8a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fe8a-111">EXAMPLES</span></span>

### <span data-ttu-id="3fe8a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3fe8a-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="3fe8a-113">Det första kommandot får datum från sju dagar sedan och lagrar det sedan i $StartDate variabel.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="3fe8a-114">Det andra kommandot får dagens datum och lagrar det sedan i $EndDate variabel.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="3fe8a-115">Det tredje kommandot får AzureWorkload säkerhets kopierings behållare och lagrar dem i $Containers variabel.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="3fe8a-116">Det fjärde kommandot hämtar säkerhets kopian och lagrar det sedan i $BackupItem variabel.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="3fe8a-117">Det sista kommandot får en matris med tids intervall för återställnings punkter för objektet i $BackupItem och lagrar dem i $RP variabeln.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="3fe8a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fe8a-118">PARAMETERS</span></span>

### <span data-ttu-id="3fe8a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe8a-119">-DefaultProfile</span></span>
<span data-ttu-id="3fe8a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe8a-121">-EndDate</span><span class="sxs-lookup"><span data-stu-id="3fe8a-121">-EndDate</span></span>
<span data-ttu-id="3fe8a-122">Slut tid för tidsintervall för vilken återställnings punkt måste hämtas</span><span class="sxs-lookup"><span data-stu-id="3fe8a-122">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe8a-123">-Objekt</span><span class="sxs-lookup"><span data-stu-id="3fe8a-123">-Item</span></span>
<span data-ttu-id="3fe8a-124">Skyddat objekt-objekt som återställnings punkt måste hämtas för</span><span class="sxs-lookup"><span data-stu-id="3fe8a-124">Protected Item object for which recovery point need to be fetched</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe8a-125">-StartDate</span><span class="sxs-lookup"><span data-stu-id="3fe8a-125">-StartDate</span></span>
<span data-ttu-id="3fe8a-126">Start tid för tidsintervall för vilken återställnings punkt måste hämtas</span><span class="sxs-lookup"><span data-stu-id="3fe8a-126">Start time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe8a-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3fe8a-127">-VaultId</span></span>
<span data-ttu-id="3fe8a-128">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3fe8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe8a-129">CommonParameters</span></span>
<span data-ttu-id="3fe8a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe8a-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe8a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe8a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fe8a-132">INPUTS</span></span>

### <span data-ttu-id="3fe8a-133">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="3fe8a-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="3fe8a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3fe8a-134">System.String</span></span>

## <span data-ttu-id="3fe8a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fe8a-135">OUTPUTS</span></span>

### <span data-ttu-id="3fe8a-136">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="3fe8a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="3fe8a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fe8a-137">NOTES</span></span>

## <span data-ttu-id="3fe8a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fe8a-138">RELATED LINKS</span></span>