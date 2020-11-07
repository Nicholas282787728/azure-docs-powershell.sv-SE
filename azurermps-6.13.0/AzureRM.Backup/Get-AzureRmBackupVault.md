---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756705"
---
# <span data-ttu-id="d7fd5-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7fd5-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="d7fd5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d7fd5-103">Hämtar säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7fd5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7fd5-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7fd5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="d7fd5-106">Cmdleten **Get-AzureRmBackupVault** får Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="d7fd5-107">Denna cmdlet returnerar **AzureRmBackupVault** -objekt som ska användas med andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="d7fd5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7fd5-108">EXAMPLES</span></span>

### <span data-ttu-id="d7fd5-109">Exempel 1: Visa alla säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="d7fd5-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="d7fd5-110">Det här kommandot får alla Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="d7fd5-111">Exempel 2: Visa alla valv som skapats i västra USA</span><span class="sxs-lookup"><span data-stu-id="d7fd5-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="d7fd5-112">Det här kommandot får alla säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="d7fd5-113">Kommandot skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7fd5-114">Denna cmdlet filtrerar resultaten baserat på egenskapen **område** .</span><span class="sxs-lookup"><span data-stu-id="d7fd5-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="d7fd5-115">Om du vill ha mer information skriver du `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="d7fd5-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="d7fd5-116">Exempel 3: skaffa ett visst valv</span><span class="sxs-lookup"><span data-stu-id="d7fd5-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="d7fd5-117">Det här kommandot får valvet med namnet Vault03.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="d7fd5-118">Exempel 4: räkna antalet valv som har lokalt redundant lagrings utrymme</span><span class="sxs-lookup"><span data-stu-id="d7fd5-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="d7fd5-119">Det här kommandot får alla Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="d7fd5-120">Kommandot skickar dem till **WHERE-objekt** , som filtrerar resultaten baserat på egenskapen **lagring** .</span><span class="sxs-lookup"><span data-stu-id="d7fd5-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="d7fd5-121">Kommandot skickar de som har värdet LocallyRedundant till cmdleten Measure-Object och räknar resultatet.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="d7fd5-122">Om du vill ha mer information skriver du `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="d7fd5-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="d7fd5-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7fd5-123">PARAMETERS</span></span>

### <span data-ttu-id="d7fd5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7fd5-124">-DefaultProfile</span></span>
<span data-ttu-id="d7fd5-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d7fd5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7fd5-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7fd5-126">-Name</span></span>
<span data-ttu-id="d7fd5-127">Anger namnet på det säkerhets kopierings valv som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="d7fd5-128">Om det finns fler än ett säkerhets kopierings valv med samma namn, returnerar denna cmdlet alla.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="d7fd5-129">Ange parametern *ResourceGroupName* för att få ett unikt valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fd5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7fd5-130">-ResourceGroupName</span></span>
<span data-ttu-id="d7fd5-131">Anger namnet på en Azure-adressresurs där denna cmdlet får ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7fd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7fd5-132">CommonParameters</span></span>
<span data-ttu-id="d7fd5-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7fd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7fd5-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7fd5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7fd5-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7fd5-135">INPUTS</span></span>

### <span data-ttu-id="d7fd5-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7fd5-136">None</span></span>

## <span data-ttu-id="d7fd5-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7fd5-137">OUTPUTS</span></span>

### <span data-ttu-id="d7fd5-138">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7fd5-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="d7fd5-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7fd5-139">NOTES</span></span>

## <span data-ttu-id="d7fd5-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7fd5-140">RELATED LINKS</span></span>

[<span data-ttu-id="d7fd5-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d7fd5-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="d7fd5-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7fd5-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="d7fd5-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7fd5-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="d7fd5-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d7fd5-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


