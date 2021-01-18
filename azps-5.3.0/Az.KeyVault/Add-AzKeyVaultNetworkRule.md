---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525989"
---
# <span data-ttu-id="02af4-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="02af4-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="02af4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02af4-102">SYNOPSIS</span></span>
<span data-ttu-id="02af4-103">Lägger till en regel för att begränsa åtkomsten till ett nyckeltal baserat på klientens Internet adress.</span><span class="sxs-lookup"><span data-stu-id="02af4-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="02af4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02af4-104">SYNTAX</span></span>

### <span data-ttu-id="02af4-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="02af4-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02af4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02af4-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02af4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02af4-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02af4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02af4-108">DESCRIPTION</span></span>
<span data-ttu-id="02af4-109">Cmdleten **Add-AzKeyVaultNetworkRule** beviljar eller begränsar åtkomsten till ett nyckeltal till en uppsättning som har utsetts av sina IP-adresser eller det virtuella nätverk som de tillhör.</span><span class="sxs-lookup"><span data-stu-id="02af4-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="02af4-110">Regeln har möjlighet att begränsa åtkomsten för andra användare, program eller säkerhets grupper som har beviljats behörigheter via åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="02af4-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="02af4-111">Observera att alla IP-adressintervall i `10.0.0.0-10.255.255.255` (privata IP-adresser) inte kan användas för att lägga till nätverks regler.</span><span class="sxs-lookup"><span data-stu-id="02af4-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="02af4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02af4-112">EXAMPLES</span></span>

### <span data-ttu-id="02af4-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="02af4-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="02af4-114">Det här kommandot lägger till en nätverks regel till det angivna valvet, vilket tillåter åtkomst till angiven IP-adress från det virtuella nätverk som identifieras av $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="02af4-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="02af4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02af4-115">PARAMETERS</span></span>

### <span data-ttu-id="02af4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02af4-116">-DefaultProfile</span></span>
<span data-ttu-id="02af4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02af4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02af4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02af4-118">-InputObject</span></span>
<span data-ttu-id="02af4-119">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="02af4-119">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="02af4-120">-IpAddressRange</span></span>
<span data-ttu-id="02af4-121">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="02af4-121">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02af4-122">-PassThru</span></span>
<span data-ttu-id="02af4-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="02af4-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="02af4-124">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="02af4-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="02af4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02af4-125">-ResourceGroupName</span></span>
<span data-ttu-id="02af4-126">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="02af4-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02af4-127">-ResourceId</span></span>
<span data-ttu-id="02af4-128">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="02af4-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="02af4-129">-VaultName</span></span>
<span data-ttu-id="02af4-130">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="02af4-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="02af4-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="02af4-132">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="02af4-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02af4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02af4-133">-Confirm</span></span>
<span data-ttu-id="02af4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02af4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02af4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02af4-135">-WhatIf</span></span>
<span data-ttu-id="02af4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02af4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02af4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02af4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02af4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02af4-138">CommonParameters</span></span>
<span data-ttu-id="02af4-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02af4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02af4-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02af4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02af4-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02af4-141">INPUTS</span></span>

### <span data-ttu-id="02af4-142">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="02af4-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="02af4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="02af4-143">System.String</span></span>

## <span data-ttu-id="02af4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02af4-144">OUTPUTS</span></span>

### <span data-ttu-id="02af4-145">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="02af4-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="02af4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02af4-146">NOTES</span></span>

## <span data-ttu-id="02af4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02af4-147">RELATED LINKS</span></span>
