---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: d0f0e52db76f4f16f41d1758b7e568ee17d6eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575726"
---
# <span data-ttu-id="ea7f5-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7f5-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="ea7f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7f5-103">Hämtar säkerhets kopierings principer för ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea7f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea7f5-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea7f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea7f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7f5-106">Cmdleten **Get-AzureRmBackupProtectionPolicy** hämtar säkerhets kopierings principer för ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="ea7f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea7f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ea7f5-108">Exempel 1: Visa principerna i ett valv</span><span class="sxs-lookup"><span data-stu-id="ea7f5-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="ea7f5-109">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ea7f5-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ea7f5-110">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ea7f5-111">Det andra kommandot får alla säkerhets kopierings principer för valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="ea7f5-112">Exempel 2: skaffa en specifik policy från ett valv</span><span class="sxs-lookup"><span data-stu-id="ea7f5-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="ea7f5-113">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ea7f5-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ea7f5-114">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ea7f5-115">Det andra kommandot får säkerhets kopierings principen med namnet DefaultPolicy för valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="ea7f5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea7f5-116">PARAMETERS</span></span>

### <span data-ttu-id="ea7f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7f5-117">-DefaultProfile</span></span>
<span data-ttu-id="ea7f5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ea7f5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea7f5-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea7f5-119">-Name</span></span>
<span data-ttu-id="ea7f5-120">Anger namnet på den princip som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-120">Specifies the name of the policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ea7f5-121">-Valv</span><span class="sxs-lookup"><span data-stu-id="ea7f5-121">-Vault</span></span>
<span data-ttu-id="ea7f5-122">Anger det säkerhets kopierings valv som denna cmdlet hämtar principer för.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="ea7f5-123">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7f5-124">CommonParameters</span></span>
<span data-ttu-id="ea7f5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7f5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7f5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea7f5-127">INPUTS</span></span>

### <span data-ttu-id="ea7f5-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ea7f5-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="ea7f5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea7f5-129">OUTPUTS</span></span>

### <span data-ttu-id="ea7f5-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7f5-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="ea7f5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea7f5-131">NOTES</span></span>
* <span data-ttu-id="ea7f5-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="ea7f5-132">None</span></span>

## <span data-ttu-id="ea7f5-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea7f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea7f5-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ea7f5-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ea7f5-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ea7f5-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="ea7f5-136">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7f5-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="ea7f5-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ea7f5-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


