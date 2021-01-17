---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393144"
---
# <span data-ttu-id="7aa7e-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7aa7e-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="7aa7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7aa7e-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa7e-103">Skaffa hanterade HSMs.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-103">Get managed HSMs.</span></span>

## <span data-ttu-id="7aa7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7aa7e-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7aa7e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7aa7e-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa7e-106">Cmdleten **Get-AzKeyVaultManagedHsm** hämtar information om de hanterade HSMs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="7aa7e-107">Du kan visa alla hanterade HSMs-instanser i en prenumeration, eller filtrera dina resultat efter en resurs grupp eller en viss hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="7aa7e-108">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får en enda hanterad HSM bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="7aa7e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7aa7e-109">EXAMPLES</span></span>

### <span data-ttu-id="7aa7e-110">Exempel 1: Hämta alla hanterade HSMs i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="7aa7e-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7aa7e-111">Det här kommandot får alla hanterade HSMs i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="7aa7e-112">Exempel 2: Hämta en specifik hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="7aa7e-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7aa7e-113">Det här kommandot får den hanterade HSM som heter myhsm i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="7aa7e-114">Exempel 3: Hämta hanterade HSMs i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="7aa7e-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7aa7e-115">Det här kommandot får alla hanterade HSMs i resurs gruppen "myrg1".</span><span class="sxs-lookup"><span data-stu-id="7aa7e-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="7aa7e-116">Exempel 4: Hämta hanterade HSMs med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="7aa7e-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="7aa7e-117">Det här kommandot får alla hanterade HSMs i prenumerationen som börjar med "myhsm".</span><span class="sxs-lookup"><span data-stu-id="7aa7e-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="7aa7e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7aa7e-118">PARAMETERS</span></span>

### <span data-ttu-id="7aa7e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa7e-119">-DefaultProfile</span></span>
<span data-ttu-id="7aa7e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aa7e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="7aa7e-121">-Name</span></span>
<span data-ttu-id="7aa7e-122">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-122">HSM name.</span></span> <span data-ttu-id="7aa7e-123">Cmdlet konstruerar FQDN för en HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7aa7e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa7e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7aa7e-125">Anger namnet på den resurs grupp som är kopplad till den hanterade HSM som efter frågas.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7aa7e-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7aa7e-126">-Tag</span></span>
<span data-ttu-id="7aa7e-127">Anger tangenten och det valfria värdet för den angivna taggen för att filtrera listan med hanterade HSMs.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa7e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa7e-128">CommonParameters</span></span>
<span data-ttu-id="7aa7e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa7e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa7e-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aa7e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa7e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7aa7e-131">INPUTS</span></span>

### <span data-ttu-id="7aa7e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7aa7e-132">System.String</span></span>

### <span data-ttu-id="7aa7e-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7aa7e-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7aa7e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7aa7e-134">OUTPUTS</span></span>

### <span data-ttu-id="7aa7e-135">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7aa7e-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="7aa7e-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7aa7e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="7aa7e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7aa7e-137">NOTES</span></span>

## <span data-ttu-id="7aa7e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7aa7e-138">RELATED LINKS</span></span>

[<span data-ttu-id="7aa7e-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7aa7e-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7aa7e-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7aa7e-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7aa7e-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7aa7e-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)