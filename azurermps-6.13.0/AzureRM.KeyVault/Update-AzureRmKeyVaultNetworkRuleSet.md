---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurermkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
ms.openlocfilehash: b1a0081f24932cf25026bdea4e9064e9dbb5a0cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576251"
---
# <span data-ttu-id="1bd9c-101">Update-AzureRmKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bd9c-101">Update-AzureRmKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="1bd9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1bd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd9c-103">Uppdaterar nätverks regeln som är inställd på ett Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-103">Updates the network rule set on a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1bd9c-104">SYNTAX</span></span>

### <span data-ttu-id="1bd9c-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="1bd9c-105">ByVaultName (Default)</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd9c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1bd9c-106">ByInputObject</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd9c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd9c-107">ByResourceId</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bd9c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1bd9c-108">DESCRIPTION</span></span>
<span data-ttu-id="1bd9c-109">Kommandot **Update-AzureRmKeyVaultNetworkRuleSet** uppdaterar de nätverks regler som tillämpas på det angivna Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-109">The **Update-AzureRmKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="1bd9c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1bd9c-110">EXAMPLES</span></span>

### <span data-ttu-id="1bd9c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1bd9c-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzureRmKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
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
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="1bd9c-112">Det här kommandot uppdaterar nätverks-ruleset för valvet med namnet "för valv" för det angivna IP-adressintervallet och det virtuella nätverket, vilket möjliggör förbikoppling av nätverks regeln för Azure-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="1bd9c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1bd9c-113">PARAMETERS</span></span>

### <span data-ttu-id="1bd9c-114">-Kringgå</span><span class="sxs-lookup"><span data-stu-id="1bd9c-114">-Bypass</span></span>
<span data-ttu-id="1bd9c-115">Anger kringgående av nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-115">Specifies bypass of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd9c-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1bd9c-116">-DefaultAction</span></span>
<span data-ttu-id="1bd9c-117">Anger standard åtgärd för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-117">Specifies default action of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd9c-118">-DefaultProfile</span></span>
<span data-ttu-id="1bd9c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd9c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bd9c-120">-InputObject</span></span>
<span data-ttu-id="1bd9c-121">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="1bd9c-121">KeyVault object</span></span>

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

### <span data-ttu-id="1bd9c-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="1bd9c-122">-IpAddressRange</span></span>
<span data-ttu-id="1bd9c-123">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-123">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="1bd9c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bd9c-124">-PassThru</span></span>
<span data-ttu-id="1bd9c-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1bd9c-126">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-126">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="1bd9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bd9c-128">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1bd9c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd9c-129">-ResourceId</span></span>
<span data-ttu-id="1bd9c-130">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="1bd9c-130">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="1bd9c-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1bd9c-131">-VaultName</span></span>
<span data-ttu-id="1bd9c-132">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1bd9c-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd9c-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1bd9c-134">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="1bd9c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1bd9c-135">-Confirm</span></span>
<span data-ttu-id="1bd9c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd9c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd9c-137">-WhatIf</span></span>
<span data-ttu-id="1bd9c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd9c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd9c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd9c-140">CommonParameters</span></span>
<span data-ttu-id="1bd9c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bd9c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd9c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd9c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd9c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1bd9c-143">INPUTS</span></span>

### <span data-ttu-id="1bd9c-144">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1bd9c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1bd9c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1bd9c-145">OUTPUTS</span></span>

### <span data-ttu-id="1bd9c-146">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1bd9c-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1bd9c-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1bd9c-147">NOTES</span></span>

## <span data-ttu-id="1bd9c-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1bd9c-148">RELATED LINKS</span></span>
