---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756894"
---
# <span data-ttu-id="d2676-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d2676-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d2676-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2676-102">SYNOPSIS</span></span>
<span data-ttu-id="d2676-103">Startar en säkerhets kopiering för en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="d2676-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2676-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2676-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2676-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2676-105">DESCRIPTION</span></span>
<span data-ttu-id="d2676-106">**Säkerhets kopiering-AzureRmRecoveryServicesBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.</span><span class="sxs-lookup"><span data-stu-id="d2676-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="d2676-107">Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="d2676-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="d2676-108">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d2676-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d2676-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2676-109">EXAMPLES</span></span>

### <span data-ttu-id="d2676-110">Exempel 1: starta en säkerhets kopia av ett säkerhets kopie objekt</span><span class="sxs-lookup"><span data-stu-id="d2676-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="d2676-111">Det första kommandot får säkerhets kopierings behållaren av typen AzureVM med namnet pstestv2vm1 och lagrar den sedan i $NamedContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="d2676-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="d2676-112">Det andra kommandot får det säkerhets kopie objekt som motsvarar behållaren i $NamedContainer och lagrar det sedan i $Item-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d2676-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="d2676-113">Det sista kommandot utlöser säkerhets kopierings jobbet i $Item.</span><span class="sxs-lookup"><span data-stu-id="d2676-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="d2676-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2676-114">PARAMETERS</span></span>

### <span data-ttu-id="d2676-115">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="d2676-115">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="d2676-116">Anger en förfallo tid som ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d2676-116">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2676-117">-Objekt</span><span class="sxs-lookup"><span data-stu-id="d2676-117">-Item</span></span>
<span data-ttu-id="d2676-118">Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.</span><span class="sxs-lookup"><span data-stu-id="d2676-118">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2676-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2676-119">-DefaultProfile</span></span>
<span data-ttu-id="d2676-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2676-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2676-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2676-121">CommonParameters</span></span>
<span data-ttu-id="d2676-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2676-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2676-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2676-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2676-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2676-124">INPUTS</span></span>

### <span data-ttu-id="d2676-125">DateTime</span><span class="sxs-lookup"><span data-stu-id="d2676-125">DateTime</span></span>
<span data-ttu-id="d2676-126">Parametern ' ExpiryDateTimeUTC ' godkänner värdet för typen ' DateTime ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d2676-126">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="d2676-127">ItemBase</span><span class="sxs-lookup"><span data-stu-id="d2676-127">ItemBase</span></span>
<span data-ttu-id="d2676-128">Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d2676-128">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="d2676-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2676-129">OUTPUTS</span></span>

### <span data-ttu-id="d2676-130">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d2676-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d2676-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2676-131">NOTES</span></span>

## <span data-ttu-id="d2676-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2676-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2676-133">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d2676-133">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="d2676-134">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d2676-134">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d2676-135">Återställ-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d2676-135">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


