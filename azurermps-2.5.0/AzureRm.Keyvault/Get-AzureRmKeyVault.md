---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930585"
---
# <span data-ttu-id="621ba-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="621ba-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="621ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="621ba-102">SYNOPSIS</span></span>
<span data-ttu-id="621ba-103">Hämtar viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="621ba-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="621ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="621ba-104">SYNTAX</span></span>

### <span data-ttu-id="621ba-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="621ba-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="621ba-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="621ba-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="621ba-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="621ba-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="621ba-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="621ba-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="621ba-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="621ba-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="621ba-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="621ba-110">DESCRIPTION</span></span>
<span data-ttu-id="621ba-111">Cmdleten **Get-AzureRmKeyVault** hämtar information om viktiga valv i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="621ba-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="621ba-112">Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.</span><span class="sxs-lookup"><span data-stu-id="621ba-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="621ba-113">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="621ba-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="621ba-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="621ba-114">EXAMPLES</span></span>

### <span data-ttu-id="621ba-115">Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="621ba-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="621ba-116">Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="621ba-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="621ba-117">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="621ba-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="621ba-118">Det här kommandot får Key-valvet som heter Contoso03Vault i ditt nuvarande abonnemang och lagrar det sedan i $MyVault variabel.</span><span class="sxs-lookup"><span data-stu-id="621ba-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="621ba-119">Du kan kontrol lera egenskaperna för $MyVault för att få information om nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="621ba-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="621ba-120">Exempel 3: Hämta viktiga valv i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="621ba-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="621ba-121">Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="621ba-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="621ba-122">Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="621ba-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="621ba-123">Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="621ba-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="621ba-124">Exempel 5: skaffa ett borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="621ba-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="621ba-125">Det här kommandot hämtar informationen om viktiga valv som heter Contoso03Vault i ditt nuvarande abonnemang och i eastus2 region.</span><span class="sxs-lookup"><span data-stu-id="621ba-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="621ba-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="621ba-126">PARAMETERS</span></span>

### <span data-ttu-id="621ba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621ba-127">-DefaultProfile</span></span>
<span data-ttu-id="621ba-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="621ba-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="621ba-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="621ba-129">-InRemovedState</span></span>
<span data-ttu-id="621ba-130">Anger om de tidigare borttagna valverna ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="621ba-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621ba-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="621ba-131">-Location</span></span>
<span data-ttu-id="621ba-132">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="621ba-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621ba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621ba-133">-ResourceGroupName</span></span>
<span data-ttu-id="621ba-134">Anger namnet på den resurs grupp som är kopplad till Key Vault eller Key vaultes.</span><span class="sxs-lookup"><span data-stu-id="621ba-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621ba-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="621ba-135">-Tag</span></span>
<span data-ttu-id="621ba-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="621ba-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="621ba-137">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="621ba-137">For example:</span></span>

<span data-ttu-id="621ba-138">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="621ba-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621ba-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="621ba-139">-VaultName</span></span>
<span data-ttu-id="621ba-140">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="621ba-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="621ba-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621ba-141">CommonParameters</span></span>
<span data-ttu-id="621ba-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621ba-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621ba-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621ba-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621ba-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="621ba-144">INPUTS</span></span>

## <span data-ttu-id="621ba-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="621ba-145">OUTPUTS</span></span>

### <span data-ttu-id="621ba-146">Microsoft. Azure. commands. valv. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="621ba-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="621ba-147">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="621ba-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="621ba-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="621ba-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="621ba-149">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="621ba-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="621ba-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="621ba-150">NOTES</span></span>

## <span data-ttu-id="621ba-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="621ba-151">RELATED LINKS</span></span>

[<span data-ttu-id="621ba-152">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="621ba-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="621ba-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="621ba-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
