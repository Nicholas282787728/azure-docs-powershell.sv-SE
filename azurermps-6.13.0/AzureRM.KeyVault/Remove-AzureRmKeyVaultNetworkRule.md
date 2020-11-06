---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576956"
---
# <span data-ttu-id="ad384-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad384-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="ad384-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad384-102">SYNOPSIS</span></span>
<span data-ttu-id="ad384-103">Tar bort en nätverks regel från ett valv.</span><span class="sxs-lookup"><span data-stu-id="ad384-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad384-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad384-104">SYNTAX</span></span>

### <span data-ttu-id="ad384-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="ad384-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad384-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad384-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad384-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad384-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad384-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad384-108">DESCRIPTION</span></span>
<span data-ttu-id="ad384-109">Tar bort en nätverks regel från ett valv.</span><span class="sxs-lookup"><span data-stu-id="ad384-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="ad384-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad384-110">EXAMPLES</span></span>

### <span data-ttu-id="ad384-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad384-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="ad384-112">Det här kommandot tar bort en nätverks regel från det angivna valvet, förutsatt att en regel hittas som matchar angiven IP-adress och ID för virtuell nätverks resurs.</span><span class="sxs-lookup"><span data-stu-id="ad384-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="ad384-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad384-113">PARAMETERS</span></span>

### <span data-ttu-id="ad384-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad384-114">-DefaultProfile</span></span>
<span data-ttu-id="ad384-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad384-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad384-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad384-116">-InputObject</span></span>
<span data-ttu-id="ad384-117">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="ad384-117">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="ad384-118">-IpAddressRange</span></span>
<span data-ttu-id="ad384-119">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="ad384-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad384-120">-PassThru</span></span>
<span data-ttu-id="ad384-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="ad384-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ad384-122">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="ad384-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad384-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad384-124">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="ad384-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad384-125">-ResourceId</span></span>
<span data-ttu-id="ad384-126">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="ad384-126">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ad384-127">-VaultName</span></span>
<span data-ttu-id="ad384-128">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="ad384-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ad384-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ad384-130">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="ad384-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad384-131">-Confirm</span></span>
<span data-ttu-id="ad384-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad384-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad384-133">-WhatIf</span></span>
<span data-ttu-id="ad384-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad384-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad384-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad384-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad384-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad384-136">CommonParameters</span></span>
<span data-ttu-id="ad384-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad384-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad384-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad384-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad384-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad384-139">INPUTS</span></span>

### <span data-ttu-id="ad384-140">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad384-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ad384-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad384-141">OUTPUTS</span></span>

### <span data-ttu-id="ad384-142">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad384-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ad384-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad384-143">NOTES</span></span>

## <span data-ttu-id="ad384-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad384-144">RELATED LINKS</span></span>
