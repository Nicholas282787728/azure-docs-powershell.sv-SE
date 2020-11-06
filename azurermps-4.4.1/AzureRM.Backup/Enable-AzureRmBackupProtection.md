---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574738"
---
# <span data-ttu-id="3f484-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="3f484-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="3f484-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f484-102">SYNOPSIS</span></span>
<span data-ttu-id="3f484-103">Associerar ett objekt med en integritets policy för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="3f484-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f484-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f484-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f484-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f484-105">DESCRIPTION</span></span>
<span data-ttu-id="3f484-106">Cmdleten **Enable-AzureRmBackupProtection** associerar ett objekt med en integritets policy för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="3f484-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="3f484-107">För att aktivera en skydds princip måste du först ha ett befintligt säkerhets kopierings objekt och en befintlig princip.</span><span class="sxs-lookup"><span data-stu-id="3f484-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="3f484-108">Båda måste tillhöra samma säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="3f484-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="3f484-109">Schemat för säkerhets kopiering gör den fullständiga initiala kopian av objektet och den inkrementella kopian för kommande säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="3f484-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="3f484-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f484-110">EXAMPLES</span></span>

### <span data-ttu-id="3f484-111">Exempel 1: Aktivera skydd på en virtuell Azure-dator</span><span class="sxs-lookup"><span data-stu-id="3f484-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="3f484-112">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="3f484-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="3f484-113">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="3f484-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="3f484-114">Det andra kommandot får säkerhets kopierings principen med namnet DefaultPolicy för valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="3f484-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="3f484-115">Kommandot lagrar objektet i $Policy variabel.</span><span class="sxs-lookup"><span data-stu-id="3f484-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3f484-116">Det sista kommandot använder pipeline-operatorn för att överföra värden från en cmdlet till nästa.</span><span class="sxs-lookup"><span data-stu-id="3f484-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="3f484-117">Den får en behållare genom att använda Get-AzureRmBackupContainer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f484-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="3f484-118">Kommandot hämtar säkerhets kopian från den behållaren med hjälp av Get-AzureRmBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f484-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="3f484-119">Den aktuella cmdleten aktiverar den princip som lagras i $Policy för objektet som kommandot skickar till denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f484-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="3f484-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f484-120">PARAMETERS</span></span>

### <span data-ttu-id="3f484-121">-Objekt</span><span class="sxs-lookup"><span data-stu-id="3f484-121">-Item</span></span>
<span data-ttu-id="3f484-122">Anger det säkerhets kopie objekt som denna cmdlet aktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="3f484-122">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="3f484-123">För att få en **AzureRmBackupItem** , Använd cmdleten Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="3f484-123">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f484-124">-Princip</span><span class="sxs-lookup"><span data-stu-id="3f484-124">-Policy</span></span>
<span data-ttu-id="3f484-125">Anger skydds princip som denna cmdlet associerar med ett objekt.</span><span class="sxs-lookup"><span data-stu-id="3f484-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="3f484-126">Använd Get-AzureRmBackupProtectionPolicy cmdlet för att få ett **AzureRmBackupProtectionPolicy** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3f484-126">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f484-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f484-127">-DefaultProfile</span></span>
<span data-ttu-id="3f484-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f484-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f484-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f484-129">CommonParameters</span></span>
<span data-ttu-id="3f484-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f484-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f484-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f484-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f484-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f484-132">INPUTS</span></span>

### <span data-ttu-id="3f484-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3f484-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="3f484-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f484-134">OUTPUTS</span></span>

### <span data-ttu-id="3f484-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3f484-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="3f484-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f484-136">NOTES</span></span>

## <span data-ttu-id="3f484-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f484-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f484-138">Säkerhets kopiering-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3f484-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="3f484-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="3f484-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="3f484-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f484-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


