---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575021"
---
# <span data-ttu-id="463ba-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="463ba-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="463ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="463ba-102">SYNOPSIS</span></span>
<span data-ttu-id="463ba-103">Hämtar säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="463ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="463ba-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="463ba-105">DESCRIPTION</span></span>
<span data-ttu-id="463ba-106">Cmdleten **Get-AzureRmBackupVault** får Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="463ba-107">Denna cmdlet returnerar **AzureRmBackupVault** -objekt som ska användas med andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="463ba-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="463ba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="463ba-108">EXAMPLES</span></span>

### <span data-ttu-id="463ba-109">Exempel 1: Visa alla säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="463ba-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="463ba-110">Det här kommandot får alla Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="463ba-111">Exempel 2: Visa alla valv som skapats i västra USA</span><span class="sxs-lookup"><span data-stu-id="463ba-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="463ba-112">Det här kommandot får alla säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="463ba-113">Kommandot skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="463ba-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="463ba-114">Denna cmdlet filtrerar resultaten baserat på egenskapen **område** .</span><span class="sxs-lookup"><span data-stu-id="463ba-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="463ba-115">Om du vill ha mer information skriver du `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="463ba-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="463ba-116">Exempel 3: skaffa ett visst valv</span><span class="sxs-lookup"><span data-stu-id="463ba-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="463ba-117">Det här kommandot får valvet med namnet Vault03.</span><span class="sxs-lookup"><span data-stu-id="463ba-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="463ba-118">Exempel 4: räkna antalet valv som har lokalt redundant lagrings utrymme</span><span class="sxs-lookup"><span data-stu-id="463ba-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="463ba-119">Det här kommandot får alla Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="463ba-120">Kommandot skickar dem till **WHERE-objekt** , som filtrerar resultaten baserat på egenskapen **lagring** .</span><span class="sxs-lookup"><span data-stu-id="463ba-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="463ba-121">Kommandot skickar de som har värdet LocallyRedundant till cmdleten Measure-Object och räknar resultatet.</span><span class="sxs-lookup"><span data-stu-id="463ba-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="463ba-122">Om du vill ha mer information skriver du `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="463ba-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="463ba-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="463ba-123">PARAMETERS</span></span>

### <span data-ttu-id="463ba-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="463ba-124">-Name</span></span>
<span data-ttu-id="463ba-125">Anger namnet på det säkerhets kopierings valv som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="463ba-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="463ba-126">Om det finns fler än ett säkerhets kopierings valv med samma namn, returnerar denna cmdlet alla.</span><span class="sxs-lookup"><span data-stu-id="463ba-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="463ba-127">Ange parametern *ResourceGroupName* för att få ett unikt valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="463ba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="463ba-128">-ResourceGroupName</span></span>
<span data-ttu-id="463ba-129">Anger namnet på en Azure-adressresurs där denna cmdlet får ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="463ba-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

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

### <span data-ttu-id="463ba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463ba-130">-DefaultProfile</span></span>
<span data-ttu-id="463ba-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="463ba-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="463ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463ba-132">CommonParameters</span></span>
<span data-ttu-id="463ba-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="463ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463ba-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="463ba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463ba-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="463ba-135">INPUTS</span></span>

## <span data-ttu-id="463ba-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="463ba-136">OUTPUTS</span></span>

### <span data-ttu-id="463ba-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="463ba-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="463ba-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="463ba-138">NOTES</span></span>
* <span data-ttu-id="463ba-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="463ba-139">None</span></span>

## <span data-ttu-id="463ba-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="463ba-140">RELATED LINKS</span></span>

[<span data-ttu-id="463ba-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="463ba-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="463ba-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="463ba-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="463ba-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="463ba-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="463ba-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="463ba-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


