---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582088"
---
# <span data-ttu-id="271d3-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="271d3-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="271d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="271d3-102">SYNOPSIS</span></span>
<span data-ttu-id="271d3-103">Skapar ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="271d3-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="271d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="271d3-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="271d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="271d3-105">DESCRIPTION</span></span>
<span data-ttu-id="271d3-106">Cmdleten **New-AzureRmBackupVault** skapar ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="271d3-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="271d3-107">Denna cmdlet returnerar ett **AzureRmBackupVault** -objekt som fungerar som en referens till Valve-enheten.</span><span class="sxs-lookup"><span data-stu-id="271d3-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="271d3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="271d3-108">EXAMPLES</span></span>

### <span data-ttu-id="271d3-109">Exempel 1: skapa ett säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="271d3-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="271d3-110">Det här kommandot skapar ett Azure Backup-valv med namnet Vault03.</span><span class="sxs-lookup"><span data-stu-id="271d3-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="271d3-111">Valvet finns i resurs gruppen som heter ResourceGroup01 i det västra USA-området.</span><span class="sxs-lookup"><span data-stu-id="271d3-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="271d3-112">Valvet använder standard typen av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="271d3-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="271d3-113">Exempel 2: skapa ett säkerhets kopierings valv som använder lokalt redundant lagring</span><span class="sxs-lookup"><span data-stu-id="271d3-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="271d3-114">Det här kommandot skapar ett Azure Backup-valv med namnet Vault03.</span><span class="sxs-lookup"><span data-stu-id="271d3-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="271d3-115">Valvet finns i resurs gruppen som heter ResourceGroup02 i det västra USA-området.</span><span class="sxs-lookup"><span data-stu-id="271d3-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="271d3-116">Valvet använder lagrings typen LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="271d3-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="271d3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="271d3-117">PARAMETERS</span></span>

### <span data-ttu-id="271d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="271d3-118">-DefaultProfile</span></span>
<span data-ttu-id="271d3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="271d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="271d3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="271d3-120">-Name</span></span>
<span data-ttu-id="271d3-121">Anger ett namn för Azure Backup-valvet.</span><span class="sxs-lookup"><span data-stu-id="271d3-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="271d3-122">Namnet måste vara unikt i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="271d3-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271d3-123">-Region</span><span class="sxs-lookup"><span data-stu-id="271d3-123">-Region</span></span>
<span data-ttu-id="271d3-124">Anger ett Azure-område där säkerhets kopierings valvet finns.</span><span class="sxs-lookup"><span data-stu-id="271d3-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="271d3-125">För Hybrid säkerhets kopierings scenarier rekommenderar vi att du skapar ett valv i en region nära den lokala servern för att minska svars tiden.</span><span class="sxs-lookup"><span data-stu-id="271d3-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="271d3-126">För säkerhets kopiering av Azure-infrastruktur som en tjänst (IaaS) virtuella datorer blir valvet identifierings platsen för lokala virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="271d3-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271d3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="271d3-127">-ResourceGroupName</span></span>
<span data-ttu-id="271d3-128">Anger namnet på en befintlig Azure-resurspost där denna cmdlet skapar ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="271d3-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="271d3-129">Använd New-AzureRMResourceGroup cmdlet för att skapa en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="271d3-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="271d3-130">Resurs gruppen och Azure Backup-valvet behöver inte vara i samma region.</span><span class="sxs-lookup"><span data-stu-id="271d3-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271d3-131">-Lagring</span><span class="sxs-lookup"><span data-stu-id="271d3-131">-Storage</span></span>
<span data-ttu-id="271d3-132">Anger lagrings typen för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="271d3-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="271d3-133">De acceptabla värdena för den här parametern är: LocallyRedundant och är bevarade.</span><span class="sxs-lookup"><span data-stu-id="271d3-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="271d3-134">Standardvärdet är billigt.</span><span class="sxs-lookup"><span data-stu-id="271d3-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="271d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="271d3-135">CommonParameters</span></span>
<span data-ttu-id="271d3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="271d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="271d3-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="271d3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="271d3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="271d3-138">INPUTS</span></span>

### <span data-ttu-id="271d3-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="271d3-139">None</span></span>

## <span data-ttu-id="271d3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="271d3-140">OUTPUTS</span></span>

### <span data-ttu-id="271d3-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="271d3-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="271d3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="271d3-142">NOTES</span></span>
* <span data-ttu-id="271d3-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="271d3-143">None</span></span>

## <span data-ttu-id="271d3-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="271d3-144">RELATED LINKS</span></span>

[<span data-ttu-id="271d3-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="271d3-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="271d3-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="271d3-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="271d3-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="271d3-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


