---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270957"
---
# <span data-ttu-id="6cd85-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6cd85-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="6cd85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cd85-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd85-103">Skaffa hanterade HSMs.</span><span class="sxs-lookup"><span data-stu-id="6cd85-103">Get managed HSMs.</span></span>

## <span data-ttu-id="6cd85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cd85-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cd85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cd85-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd85-106">Cmdleten **Get-AzManagedHsm** hämtar information om de hanterade HSMs i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6cd85-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="6cd85-107">Du kan visa alla hanterade HSMs-instanser i en prenumeration, eller filtrera dina resultat efter en resurs grupp eller en viss hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="6cd85-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="6cd85-108">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får en enda hanterad HSM bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="6cd85-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="6cd85-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cd85-109">EXAMPLES</span></span>

### <span data-ttu-id="6cd85-110">Exempel 1: Hämta alla hanterade HSMs i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="6cd85-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="6cd85-111">Det här kommandot får alla hanterade HSMs i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6cd85-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="6cd85-112">Exempel 2: Hämta en specifik hanterad HSM</span><span class="sxs-lookup"><span data-stu-id="6cd85-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="6cd85-113">Det här kommandot får den hanterade HSM som heter myhsm i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6cd85-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="6cd85-114">Exempel 3: Hämta hanterade HSMs i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6cd85-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="6cd85-115">Det här kommandot får alla hanterade HSMs i resurs gruppen "myrg1".</span><span class="sxs-lookup"><span data-stu-id="6cd85-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="6cd85-116">Exempel 4: Hämta hanterade HSMs med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="6cd85-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="6cd85-117">Det här kommandot får alla hanterade HSMs i prenumerationen som börjar med "myhsm".</span><span class="sxs-lookup"><span data-stu-id="6cd85-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="6cd85-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cd85-118">PARAMETERS</span></span>

### <span data-ttu-id="6cd85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd85-119">-DefaultProfile</span></span>
<span data-ttu-id="6cd85-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd85-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd85-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cd85-121">-Name</span></span>
<span data-ttu-id="6cd85-122">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="6cd85-122">HSM name.</span></span> <span data-ttu-id="6cd85-123">Cmdlet konstruerar FQDN för en HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="6cd85-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd85-124">-ResourceGroupName</span></span>
<span data-ttu-id="6cd85-125">Anger namnet på den resurs grupp som är kopplad till den hanterade HSM som efter frågas.</span><span class="sxs-lookup"><span data-stu-id="6cd85-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cd85-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6cd85-126">-Tag</span></span>
<span data-ttu-id="6cd85-127">Anger tangenten och det valfria värdet för den angivna taggen för att filtrera listan med hanterade HSMs.</span><span class="sxs-lookup"><span data-stu-id="6cd85-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="6cd85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd85-128">CommonParameters</span></span>
<span data-ttu-id="6cd85-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd85-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cd85-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd85-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cd85-131">INPUTS</span></span>

### <span data-ttu-id="6cd85-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6cd85-132">System.String</span></span>

### <span data-ttu-id="6cd85-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6cd85-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cd85-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cd85-134">OUTPUTS</span></span>

### <span data-ttu-id="6cd85-135">Microsoft. Azure. commands. valv. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6cd85-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="6cd85-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6cd85-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="6cd85-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cd85-137">NOTES</span></span>

## <span data-ttu-id="6cd85-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cd85-138">RELATED LINKS</span></span>

[<span data-ttu-id="6cd85-139">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6cd85-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="6cd85-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6cd85-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="6cd85-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6cd85-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)