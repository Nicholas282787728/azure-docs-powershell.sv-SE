---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273440"
---
# <span data-ttu-id="02688-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02688-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="02688-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02688-102">SYNOPSIS</span></span>
<span data-ttu-id="02688-103">Skapar en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="02688-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="02688-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02688-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02688-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02688-105">DESCRIPTION</span></span>
<span data-ttu-id="02688-106">Cmdleten **New-AzManagedHsm** skapar en hanterad HSM i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="02688-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="02688-107">Om du vill lägga till, ta bort eller lista nycklar i den hanterade HSM ska användaren bevilja behörigheter genom att lägga till användar-ID i administratören.</span><span class="sxs-lookup"><span data-stu-id="02688-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="02688-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02688-108">EXAMPLES</span></span>

### <span data-ttu-id="02688-109">Exempel 1: skapa en StandardB1 hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="02688-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="02688-110">Det här kommandot skapar en hanterad HSM med namnet myhsm i eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="02688-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="02688-111">Kommandot lägger till hanterad HSM i resurs gruppen med namnet myrg1.</span><span class="sxs-lookup"><span data-stu-id="02688-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="02688-112">Eftersom kommandot inte anger ett värde för parametern *SKU* skapas en Standard_B1 hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="02688-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="02688-113">Exempel 2: skapa en CustomB32 hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="02688-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="02688-114">Det här kommandot skapar en hanterad HSM, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="02688-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="02688-115">Men det anger ett värde för CustomB32 för parametern *SKU* för att skapa en CustomB32-hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="02688-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="02688-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02688-116">PARAMETERS</span></span>

### <span data-ttu-id="02688-117">-Administratör</span><span class="sxs-lookup"><span data-stu-id="02688-117">-Administrator</span></span>
<span data-ttu-id="02688-118">Ursprungligt administratörs objekt-ID för den här hanterade HSM-poolen.</span><span class="sxs-lookup"><span data-stu-id="02688-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="02688-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02688-119">-AsJob</span></span>
<span data-ttu-id="02688-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="02688-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02688-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02688-121">-DefaultProfile</span></span>
<span data-ttu-id="02688-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02688-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02688-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="02688-123">-Location</span></span>
<span data-ttu-id="02688-124">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="02688-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="02688-125">Använd kommandot Get-AzResourceProvider med parametern ProviderNamespace för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="02688-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="02688-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="02688-126">-Name</span></span>
<span data-ttu-id="02688-127">Anger namnet på den hanterade HSM som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="02688-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="02688-128">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="02688-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="02688-129">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="02688-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="02688-130">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="02688-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="02688-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02688-131">-ResourceGroupName</span></span>
<span data-ttu-id="02688-132">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="02688-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="02688-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="02688-133">-Sku</span></span>
<span data-ttu-id="02688-134">Anger SKU för den hanterade HSM-instansen.</span><span class="sxs-lookup"><span data-stu-id="02688-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="02688-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="02688-135">-Tag</span></span>
<span data-ttu-id="02688-136">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="02688-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="02688-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02688-137">-Confirm</span></span>
<span data-ttu-id="02688-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02688-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02688-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02688-139">-WhatIf</span></span>
<span data-ttu-id="02688-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02688-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02688-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02688-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02688-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02688-142">CommonParameters</span></span>
<span data-ttu-id="02688-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02688-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02688-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02688-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02688-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02688-145">INPUTS</span></span>

### <span data-ttu-id="02688-146">System. String</span><span class="sxs-lookup"><span data-stu-id="02688-146">System.String</span></span>

### <span data-ttu-id="02688-147">System. string []</span><span class="sxs-lookup"><span data-stu-id="02688-147">System.String[]</span></span>

### <span data-ttu-id="02688-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="02688-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02688-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02688-149">OUTPUTS</span></span>

### <span data-ttu-id="02688-150">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02688-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="02688-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02688-151">NOTES</span></span>

## <span data-ttu-id="02688-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02688-152">RELATED LINKS</span></span>

[<span data-ttu-id="02688-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02688-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="02688-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02688-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="02688-155">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="02688-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)