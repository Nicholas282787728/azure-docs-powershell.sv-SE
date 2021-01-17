---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411723"
---
# <span data-ttu-id="f6dcd-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f6dcd-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="f6dcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dcd-103">Tar bort en nätverks regel från ett valv.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="f6dcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6dcd-104">SYNTAX</span></span>

### <span data-ttu-id="f6dcd-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="f6dcd-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6dcd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6dcd-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6dcd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6dcd-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6dcd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="f6dcd-109">Tar bort en nätverks regel från ett valv.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="f6dcd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6dcd-110">EXAMPLES</span></span>

### <span data-ttu-id="f6dcd-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6dcd-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="f6dcd-112">Det här kommandot tar bort en nätverks regel från det angivna valvet, förutsatt att en regel hittas som matchar angiven IP-adress och ID för virtuell nätverks resurs.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="f6dcd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6dcd-113">PARAMETERS</span></span>

### <span data-ttu-id="f6dcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6dcd-114">-DefaultProfile</span></span>
<span data-ttu-id="f6dcd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6dcd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6dcd-116">-InputObject</span></span>
<span data-ttu-id="f6dcd-117">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="f6dcd-117">KeyVault object</span></span>

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

### <span data-ttu-id="f6dcd-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="f6dcd-118">-IpAddressRange</span></span>
<span data-ttu-id="f6dcd-119">Anger tillåtet nätverks-IP-adressintervall för nätverks regel.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="f6dcd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6dcd-120">-PassThru</span></span>
<span data-ttu-id="f6dcd-121">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f6dcd-122">Om den här växeln är angiven returneras det uppdaterade nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="f6dcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6dcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6dcd-124">Anger namnet på den resurs grupp som är kopplad till det huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f6dcd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6dcd-125">-ResourceId</span></span>
<span data-ttu-id="f6dcd-126">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="f6dcd-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="f6dcd-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f6dcd-127">-VaultName</span></span>
<span data-ttu-id="f6dcd-128">Anger namnet på ett huvud valv vars nätverks regel ändras.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="f6dcd-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f6dcd-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f6dcd-130">Anger tillåtet virtuellt nätverks-ID för nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="f6dcd-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6dcd-131">-Confirm</span></span>
<span data-ttu-id="f6dcd-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6dcd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6dcd-133">-WhatIf</span></span>
<span data-ttu-id="f6dcd-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6dcd-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6dcd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dcd-136">CommonParameters</span></span>
<span data-ttu-id="f6dcd-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6dcd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dcd-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6dcd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dcd-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6dcd-139">INPUTS</span></span>

### <span data-ttu-id="f6dcd-140">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f6dcd-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f6dcd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f6dcd-141">System.String</span></span>

## <span data-ttu-id="f6dcd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6dcd-142">OUTPUTS</span></span>

### <span data-ttu-id="f6dcd-143">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f6dcd-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f6dcd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6dcd-144">NOTES</span></span>

## <span data-ttu-id="f6dcd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6dcd-145">RELATED LINKS</span></span>
