---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 91658fc0772dfa2752d7f12f93efc62d57330891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756567"
---
# <span data-ttu-id="7497f-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="7497f-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="7497f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7497f-102">SYNOPSIS</span></span>
<span data-ttu-id="7497f-103">Hämtar information om ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="7497f-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7497f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7497f-104">SYNTAX</span></span>

### <span data-ttu-id="7497f-105">JobFilterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7497f-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7497f-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="7497f-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7497f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7497f-107">DESCRIPTION</span></span>
<span data-ttu-id="7497f-108">Cmdleten **Get-AzureRmRecoveryServicesBackupJobDetails** hämtar information om Azure Backup-jobbet för ett angivet jobb.</span><span class="sxs-lookup"><span data-stu-id="7497f-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="7497f-109">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7497f-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7497f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7497f-110">EXAMPLES</span></span>

### <span data-ttu-id="7497f-111">Exempel 1: Hämta information om jobb för misslyckade jobb</span><span class="sxs-lookup"><span data-stu-id="7497f-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="7497f-112">Det första kommandot får en matris med misslyckade jobb i valvet och lagrar dem i $Jobs matrisen.</span><span class="sxs-lookup"><span data-stu-id="7497f-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="7497f-113">Det andra kommandot får jobb informationen för misslyckade jobb i $Jobs och lagrar dem sedan i $JobDetails variabel.</span><span class="sxs-lookup"><span data-stu-id="7497f-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="7497f-114">Det sista kommandot visar fel information för misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="7497f-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="7497f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7497f-115">PARAMETERS</span></span>

### <span data-ttu-id="7497f-116">-Jobb</span><span class="sxs-lookup"><span data-stu-id="7497f-116">-Job</span></span>
<span data-ttu-id="7497f-117">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="7497f-117">Specifies the job to get.</span></span>
<span data-ttu-id="7497f-118">För att hämta ett **BackupJob** -objekt, Använd cmdleten Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="7497f-118">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7497f-119">-JobId</span><span class="sxs-lookup"><span data-stu-id="7497f-119">-JobId</span></span>
<span data-ttu-id="7497f-120">Anger ID för ett säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="7497f-120">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="7497f-121">ID är InstanceId-egenskapen för ett **BackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7497f-121">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7497f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7497f-122">-DefaultProfile</span></span>
<span data-ttu-id="7497f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7497f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7497f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7497f-124">CommonParameters</span></span>
<span data-ttu-id="7497f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7497f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7497f-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7497f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7497f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7497f-127">INPUTS</span></span>

## <span data-ttu-id="7497f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7497f-128">OUTPUTS</span></span>

### <span data-ttu-id="7497f-129">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="7497f-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7497f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7497f-130">NOTES</span></span>

## <span data-ttu-id="7497f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7497f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7497f-132">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7497f-132">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


