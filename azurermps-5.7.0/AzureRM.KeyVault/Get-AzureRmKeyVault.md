---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586087"
---
# <span data-ttu-id="f7678-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f7678-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="f7678-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7678-102">SYNOPSIS</span></span>
<span data-ttu-id="f7678-103">Hämtar viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="f7678-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7678-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7678-104">SYNTAX</span></span>

### <span data-ttu-id="f7678-105">ListAllVaultsInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="f7678-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7678-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="f7678-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7678-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f7678-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7678-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="f7678-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7678-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7678-109">DESCRIPTION</span></span>
<span data-ttu-id="f7678-110">Cmdleten **Get-AzureRmKeyVault** hämtar information om viktiga valv i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f7678-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="f7678-111">Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.</span><span class="sxs-lookup"><span data-stu-id="f7678-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="f7678-112">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="f7678-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="f7678-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7678-113">EXAMPLES</span></span>

### <span data-ttu-id="f7678-114">Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="f7678-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="f7678-115">Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f7678-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="f7678-116">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="f7678-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="f7678-117">Det här kommandot får Key-valvet som heter Contoso03Vault i ditt nuvarande abonnemang och lagrar det sedan i $MyVault variabel.</span><span class="sxs-lookup"><span data-stu-id="f7678-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="f7678-118">Du kan kontrol lera egenskaperna för $MyVault för att få information om nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="f7678-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="f7678-119">Exempel 3: Hämta viktiga valv i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="f7678-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="f7678-120">Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7678-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="f7678-121">Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="f7678-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="f7678-122">Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="f7678-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="f7678-123">Exempel 5: skaffa ett borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="f7678-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="f7678-124">Det här kommandot hämtar informationen om viktiga valv som heter Contoso03Vault i ditt nuvarande abonnemang och i eastus2 region.</span><span class="sxs-lookup"><span data-stu-id="f7678-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="f7678-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7678-125">PARAMETERS</span></span>

### <span data-ttu-id="f7678-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7678-126">-DefaultProfile</span></span>
<span data-ttu-id="f7678-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f7678-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7678-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f7678-128">-InRemovedState</span></span>
<span data-ttu-id="f7678-129">Anger om de tidigare borttagna valverna ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="f7678-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="f7678-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="f7678-130">-Location</span></span>
<span data-ttu-id="f7678-131">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="f7678-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7678-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7678-132">-ResourceGroupName</span></span>
<span data-ttu-id="f7678-133">Anger namnet på den resurs grupp som är kopplad till Key Vault eller Key vaultes.</span><span class="sxs-lookup"><span data-stu-id="f7678-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="f7678-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f7678-134">-Tag</span></span>
<span data-ttu-id="f7678-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f7678-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f7678-136">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="f7678-136">For example:</span></span>

<span data-ttu-id="f7678-137">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f7678-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7678-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f7678-138">-VaultName</span></span>
<span data-ttu-id="f7678-139">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="f7678-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7678-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7678-140">CommonParameters</span></span>
<span data-ttu-id="f7678-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7678-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7678-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7678-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7678-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7678-143">INPUTS</span></span>

### <span data-ttu-id="f7678-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="f7678-144">None</span></span>
<span data-ttu-id="f7678-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f7678-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7678-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7678-146">OUTPUTS</span></span>

### <span data-ttu-id="f7678-147">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f7678-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f7678-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="f7678-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="f7678-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="f7678-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="f7678-150">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="f7678-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="f7678-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7678-151">NOTES</span></span>

## <span data-ttu-id="f7678-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7678-152">RELATED LINKS</span></span>

[<span data-ttu-id="f7678-153">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f7678-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="f7678-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f7678-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
