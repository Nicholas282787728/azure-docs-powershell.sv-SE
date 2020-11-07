---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755463"
---
# <span data-ttu-id="e055a-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e055a-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="e055a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e055a-102">SYNOPSIS</span></span>
<span data-ttu-id="e055a-103">Hämtar säkerhets kopierings behållare.</span><span class="sxs-lookup"><span data-stu-id="e055a-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e055a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e055a-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e055a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e055a-105">DESCRIPTION</span></span>
<span data-ttu-id="e055a-106">Cmdleten **Get-AzureRmBackupContainer** får Azure Backup-behållare.</span><span class="sxs-lookup"><span data-stu-id="e055a-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="e055a-107">En **AzureBackupContainer** kapslar in data källor, skyddade objekt och återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="e055a-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="e055a-108">En **AzureBackupContainer** kan vara något av följande:</span><span class="sxs-lookup"><span data-stu-id="e055a-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="e055a-109">En Windows Server-dator</span><span class="sxs-lookup"><span data-stu-id="e055a-109">A Windows Server computer</span></span>
- <span data-ttu-id="e055a-110">En System Center Data Protection Manager (SCDPM)-Server</span><span class="sxs-lookup"><span data-stu-id="e055a-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="e055a-111">En Azure-infrastruktur som tjänst (IaaS)</span><span class="sxs-lookup"><span data-stu-id="e055a-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="e055a-112">Innan säkerhets kopiering kan säkerhetskopiera en data källa eller ett objekt måste du registrera den behållare som innehåller den med Azure Backup-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e055a-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="e055a-113">Behållaren måste autentiseras för att skicka säkerhets kopior till säkerhets kopierings valvet.</span><span class="sxs-lookup"><span data-stu-id="e055a-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="e055a-114">För Windows Server-datorer och SCDPM-servrar hålls registreringen med det fullt kvalificerade domän namnet för servern.</span><span class="sxs-lookup"><span data-stu-id="e055a-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="e055a-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e055a-115">EXAMPLES</span></span>

### <span data-ttu-id="e055a-116">Exempel 1: Visa alla servrar registrerade i ett valv</span><span class="sxs-lookup"><span data-stu-id="e055a-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="e055a-117">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="e055a-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="e055a-118">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="e055a-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="e055a-119">Det andra kommandot får alla behållare av typen fönster från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="e055a-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="e055a-120">Exempel 2: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="e055a-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="e055a-121">Det här kommandot får behållaren DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="e055a-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="e055a-122">Kommandot anger valvet i $Vault och typen av container.</span><span class="sxs-lookup"><span data-stu-id="e055a-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="e055a-123">Exempel 3: Visa alla registrerade virtuella Azure-datorer</span><span class="sxs-lookup"><span data-stu-id="e055a-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="e055a-124">Det här kommandot hämtar de registrerade virtuella datorerna från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="e055a-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="e055a-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e055a-125">PARAMETERS</span></span>

### <span data-ttu-id="e055a-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e055a-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e055a-127">Anger namnet på den resurs grupp som är kopplad till behållaren.</span><span class="sxs-lookup"><span data-stu-id="e055a-127">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="e055a-128">Det här namnet är samma värde som du angav för parametern *ServiceName* eller *ResourceGroupName* för Register-AzureRmBackupContainer cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e055a-128">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e055a-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="e055a-129">-Name</span></span>
<span data-ttu-id="e055a-130">Anger namnet på den behållare som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="e055a-130">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e055a-131">-Status</span><span class="sxs-lookup"><span data-stu-id="e055a-131">-Status</span></span>
<span data-ttu-id="e055a-132">Anger aktuell status för de behållare som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e055a-132">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="e055a-133">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e055a-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e055a-134">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="e055a-134">NotRegistered</span></span> 
- <span data-ttu-id="e055a-135">Rekommendera</span><span class="sxs-lookup"><span data-stu-id="e055a-135">Registered</span></span> 
- <span data-ttu-id="e055a-136">Registreringen</span><span class="sxs-lookup"><span data-stu-id="e055a-136">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e055a-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e055a-137">-Type</span></span>
<span data-ttu-id="e055a-138">Anger den typ av behållare som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="e055a-138">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e055a-139">-Valv</span><span class="sxs-lookup"><span data-stu-id="e055a-139">-Vault</span></span>
<span data-ttu-id="e055a-140">Anger ett säkerhets kopierings valv som den här cmdleten får behållare för.</span><span class="sxs-lookup"><span data-stu-id="e055a-140">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="e055a-141">För att få en **AzureRmBackupVault** , Använd cmdleten Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="e055a-141">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e055a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e055a-142">-DefaultProfile</span></span>
<span data-ttu-id="e055a-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e055a-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e055a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e055a-144">CommonParameters</span></span>
<span data-ttu-id="e055a-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e055a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e055a-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e055a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e055a-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e055a-147">INPUTS</span></span>

### <span data-ttu-id="e055a-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="e055a-148">AzureBackupVault</span></span>

## <span data-ttu-id="e055a-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e055a-149">OUTPUTS</span></span>

### <span data-ttu-id="e055a-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e055a-150">AzureBackupContainer</span></span>

## <span data-ttu-id="e055a-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e055a-151">NOTES</span></span>
* <span data-ttu-id="e055a-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="e055a-152">None</span></span>

## <span data-ttu-id="e055a-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e055a-153">RELATED LINKS</span></span>

[<span data-ttu-id="e055a-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e055a-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="e055a-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e055a-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="e055a-156">Avregistrera-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e055a-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


