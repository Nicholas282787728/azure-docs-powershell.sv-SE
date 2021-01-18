---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524109"
---
# <span data-ttu-id="bf896-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bf896-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="bf896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf896-102">SYNOPSIS</span></span>
<span data-ttu-id="bf896-103">Skapar en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="bf896-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="bf896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf896-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf896-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf896-105">DESCRIPTION</span></span>
<span data-ttu-id="bf896-106">Cmdleten **New-AzKeyVaultManagedHsm** skapar en hanterad HSM i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bf896-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="bf896-107">Om du vill lägga till, ta bort eller lista nycklar i den hanterade HSM ska användaren bevilja behörigheter genom att lägga till användar-ID i administratören.</span><span class="sxs-lookup"><span data-stu-id="bf896-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="bf896-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf896-108">EXAMPLES</span></span>

### <span data-ttu-id="bf896-109">Exempel 1: skapa en StandardB1 hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="bf896-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="bf896-110">Det här kommandot skapar en hanterad HSM med namnet myhsm i eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="bf896-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="bf896-111">Kommandot lägger till hanterad HSM i resurs gruppen med namnet myrg1.</span><span class="sxs-lookup"><span data-stu-id="bf896-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="bf896-112">Eftersom kommandot inte anger ett värde för parametern *SKU* skapas en Standard_B1 hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="bf896-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="bf896-113">Exempel 2: skapa en CustomB32 hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="bf896-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="bf896-114">Det här kommandot skapar en hanterad HSM, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="bf896-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="bf896-115">Men det anger ett värde för CustomB32 för parametern *SKU* för att skapa en CustomB32-hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="bf896-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="bf896-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf896-116">PARAMETERS</span></span>

### <span data-ttu-id="bf896-117">-Administratör</span><span class="sxs-lookup"><span data-stu-id="bf896-117">-Administrator</span></span>
<span data-ttu-id="bf896-118">Ursprungligt administratörs objekt-ID för den här hanterade HSM-poolen.</span><span class="sxs-lookup"><span data-stu-id="bf896-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf896-119">-AsJob</span></span>
<span data-ttu-id="bf896-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bf896-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf896-121">-DefaultProfile</span></span>
<span data-ttu-id="bf896-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf896-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf896-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="bf896-123">-Location</span></span>
<span data-ttu-id="bf896-124">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="bf896-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="bf896-125">Använd kommandot Get-AzResourceProvider med parametern ProviderNamespace för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="bf896-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf896-126">-Name</span></span>
<span data-ttu-id="bf896-127">Anger namnet på den hanterade HSM som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="bf896-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="bf896-128">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="bf896-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="bf896-129">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="bf896-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="bf896-130">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="bf896-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf896-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf896-132">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="bf896-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="bf896-133">-Sku</span></span>
<span data-ttu-id="bf896-134">Anger SKU för den hanterade HSM-instansen.</span><span class="sxs-lookup"><span data-stu-id="bf896-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="bf896-135">-Tag</span></span>
<span data-ttu-id="bf896-136">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="bf896-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf896-137">-Confirm</span></span>
<span data-ttu-id="bf896-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf896-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf896-139">-WhatIf</span></span>
<span data-ttu-id="bf896-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf896-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf896-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf896-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf896-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf896-142">CommonParameters</span></span>
<span data-ttu-id="bf896-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf896-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf896-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf896-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf896-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf896-145">INPUTS</span></span>

### <span data-ttu-id="bf896-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bf896-146">System.String</span></span>

### <span data-ttu-id="bf896-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="bf896-147">System.String[]</span></span>

### <span data-ttu-id="bf896-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="bf896-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bf896-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf896-149">OUTPUTS</span></span>

### <span data-ttu-id="bf896-150">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bf896-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="bf896-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf896-151">NOTES</span></span>

## <span data-ttu-id="bf896-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf896-152">RELATED LINKS</span></span>

[<span data-ttu-id="bf896-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bf896-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="bf896-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bf896-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="bf896-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="bf896-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)