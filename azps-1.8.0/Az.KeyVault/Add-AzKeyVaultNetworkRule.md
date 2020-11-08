---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: fd93a933b394fc8729186c7ea78c737123149bf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916366"
---
# <span data-ttu-id="dd2fb-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dd2fb-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="dd2fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2fb-103">Lägger till en regel för att begränsa åtkomsten till ett nyckeltal baserat på klientens Internet adress.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="dd2fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd2fb-104">SYNTAX</span></span>

### <span data-ttu-id="dd2fb-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="dd2fb-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2fb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dd2fb-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2fb-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2fb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd2fb-108">DESCRIPTION</span></span>
<span data-ttu-id="dd2fb-109">Cmdleten **Add-AzKeyVaultNetworkRule** beviljar eller begränsar åtkomsten till ett nyckeltal till en uppsättning som har utsetts av sina IP-adresser eller det virtuella nätverk som de tillhör.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="dd2fb-110">Regeln har möjlighet att begränsa åtkomsten för andra användare, program eller säkerhets grupper som har beviljats behörigheter via åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="dd2fb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd2fb-111">EXAMPLES</span></span>

### <span data-ttu-id="dd2fb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd2fb-112">Example 1</span></span>
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

<span data-ttu-id="dd2fb-113">Det här kommandot lägger till en nätverks regel till det angivna valvet, vilket tillåter åtkomst till angiven IP-adress från det virtuella nätverk som identifieras av $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="dd2fb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd2fb-114">PARAMETERS</span></span>

### <span data-ttu-id="dd2fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2fb-115">-DefaultProfile</span></span>
<span data-ttu-id="dd2fb-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd2fb-117">-InputObject</span></span>
<span data-ttu-id="dd2fb-118">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="dd2fb-118">KeyVault object</span></span>

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

### <span data-ttu-id="dd2fb-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="dd2fb-119">-IpAddressRange</span></span>
<span data-ttu-id="dd2fb-120">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="dd2fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2fb-121">-PassThru</span></span>
<span data-ttu-id="dd2fb-122">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dd2fb-123">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="dd2fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd2fb-125">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="dd2fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2fb-126">-ResourceId</span></span>
<span data-ttu-id="dd2fb-127">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="dd2fb-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="dd2fb-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dd2fb-128">-VaultName</span></span>
<span data-ttu-id="dd2fb-129">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="dd2fb-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2fb-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="dd2fb-131">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="dd2fb-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd2fb-132">-Confirm</span></span>
<span data-ttu-id="dd2fb-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2fb-134">-WhatIf</span></span>
<span data-ttu-id="dd2fb-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2fb-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2fb-137">CommonParameters</span></span>
<span data-ttu-id="dd2fb-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2fb-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2fb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2fb-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd2fb-140">INPUTS</span></span>

### <span data-ttu-id="dd2fb-141">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dd2fb-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="dd2fb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2fb-142">System.String</span></span>

## <span data-ttu-id="dd2fb-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd2fb-143">OUTPUTS</span></span>

### <span data-ttu-id="dd2fb-144">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dd2fb-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="dd2fb-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd2fb-145">NOTES</span></span>

## <span data-ttu-id="dd2fb-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd2fb-146">RELATED LINKS</span></span>