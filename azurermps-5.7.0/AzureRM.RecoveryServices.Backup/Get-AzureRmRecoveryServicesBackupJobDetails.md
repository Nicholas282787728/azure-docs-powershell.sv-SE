---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574235"
---
# <span data-ttu-id="b29be-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="b29be-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="b29be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b29be-102">SYNOPSIS</span></span>
<span data-ttu-id="b29be-103">Hämtar information om ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="b29be-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b29be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b29be-104">SYNTAX</span></span>

### <span data-ttu-id="b29be-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b29be-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b29be-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="b29be-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b29be-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b29be-107">DESCRIPTION</span></span>
<span data-ttu-id="b29be-108">Cmdleten **Get-AzureRmRecoveryServicesBackupJobDetails** hämtar information om Azure Backup-jobbet för ett angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="b29be-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="b29be-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b29be-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b29be-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b29be-110">EXAMPLES</span></span>

### <span data-ttu-id="b29be-111">Exempel 1: Hämta information om jobb för misslyckade jobb</span><span class="sxs-lookup"><span data-stu-id="b29be-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="b29be-112">Det första kommandot får en matris med misslyckade jobb i valvet och lagrar dem i $Jobs matrisen.</span><span class="sxs-lookup"><span data-stu-id="b29be-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="b29be-113">Det andra kommandot får jobb informationen för misslyckade jobb i $Jobs och lagrar dem sedan i $JobDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="b29be-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="b29be-114">Det sista kommandot visar fel information för misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="b29be-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="b29be-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b29be-115">PARAMETERS</span></span>

### <span data-ttu-id="b29be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29be-116">-DefaultProfile</span></span>
<span data-ttu-id="b29be-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b29be-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b29be-118">-Jobb</span><span class="sxs-lookup"><span data-stu-id="b29be-118">-Job</span></span>
<span data-ttu-id="b29be-119">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="b29be-119">Specifies the job to get.</span></span>
<span data-ttu-id="b29be-120">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="b29be-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29be-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="b29be-121">-JobId</span></span>
<span data-ttu-id="b29be-122">Anger ID för ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="b29be-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="b29be-123">ID är InstanceId-egenskapen för ett **BackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b29be-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b29be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29be-124">CommonParameters</span></span>
<span data-ttu-id="b29be-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b29be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29be-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29be-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29be-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b29be-127">INPUTS</span></span>

### <span data-ttu-id="b29be-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="b29be-128">None</span></span>
<span data-ttu-id="b29be-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b29be-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b29be-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b29be-130">OUTPUTS</span></span>

### <span data-ttu-id="b29be-131">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b29be-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b29be-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b29be-132">NOTES</span></span>

## <span data-ttu-id="b29be-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b29be-133">RELATED LINKS</span></span>

[<span data-ttu-id="b29be-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b29be-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


