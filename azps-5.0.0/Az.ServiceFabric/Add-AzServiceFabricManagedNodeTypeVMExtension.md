---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: baff896564d8f3b8d70f69b190bc3429d4f465c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273029"
---
# <span data-ttu-id="de386-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="de386-101">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="de386-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de386-102">SYNOPSIS</span></span>
<span data-ttu-id="de386-103">Lägg till virtuellt dator tillägg till nodtypen.</span><span class="sxs-lookup"><span data-stu-id="de386-103">Add vm extension to the node type.</span></span>

## <span data-ttu-id="de386-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de386-104">SYNTAX</span></span>

### <span data-ttu-id="de386-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="de386-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String>
 [-ForceUpdateTag <String>] -Publisher <String> -Type <String> -TypeHandlerVersion <String>
 [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de386-106">ByName</span><span class="sxs-lookup"><span data-stu-id="de386-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-ForceUpdateTag <String>] -Publisher <String> -Type <String>
 -TypeHandlerVersion <String> [-AutoUpgradeMinorVersion] [-Setting <Object>] [-ProtectedSetting <Object>]
 [-ProvisionAfterExtension <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de386-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de386-107">DESCRIPTION</span></span>
<span data-ttu-id="de386-108">Lägg till virtuellt dator tillägg till nodtypen.</span><span class="sxs-lookup"><span data-stu-id="de386-108">Add vm extension to the node type.</span></span> <span data-ttu-id="de386-109">Då läggs tillägget till i resursen för underliying virtuella dator skalning.</span><span class="sxs-lookup"><span data-stu-id="de386-109">This will add the extension to the underliying Virtual Machine Scale Set resource.</span></span>

## <span data-ttu-id="de386-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de386-110">EXAMPLES</span></span>

### <span data-ttu-id="de386-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="de386-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="de386-112">Det här kommandot lägger till ett tillägg till nodtypen.</span><span class="sxs-lookup"><span data-stu-id="de386-112">This command adds an extension to the node type.</span></span>

### <span data-ttu-id="de386-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="de386-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$settings = @{ "secretsManagementSettings" = @{ "pollingIntervalInS" = "3600"; "certificateStoreName" = "MY"; "certificateStoreLocation" = "LocalMachine"; "observedCertificates" = @( "https:/testkv.vault.azure.net/secrets/TestSecret" ) } };
$protectedSettings = @{"testProgectedSetting" = $protectedSetting };
Add-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name KeyVaultForWindows -Publisher Microsoft.Azure.KeyVault -Type KeyVaultForWindows -TypeHandlerVersion 1.0 -Settings $settings -ProtectedSettings $protectedSettings  -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="de386-114">Det här kommandot lägger till ett tillägg med inställningar och skyddade inställningar till nodtypen.</span><span class="sxs-lookup"><span data-stu-id="de386-114">This command adds an extension with settings and protected settings to the node type.</span></span>

### <span data-ttu-id="de386-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="de386-115">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMExtension $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion -Verbose
```

<span data-ttu-id="de386-116">Det här kommandot lägger till ett tillägg till nodtypen med rör.</span><span class="sxs-lookup"><span data-stu-id="de386-116">This command adds an extension to the node type, with piping.</span></span>

## <span data-ttu-id="de386-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de386-117">PARAMETERS</span></span>

### <span data-ttu-id="de386-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de386-118">-AsJob</span></span>
<span data-ttu-id="de386-119">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="de386-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="de386-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="de386-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="de386-121">Anger om tillägget ska använda en nyare del version om en sådan finns tillgänglig vid distribution.</span><span class="sxs-lookup"><span data-stu-id="de386-121">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="de386-122">När tillägget har distribuerats uppgraderas inte del versioner såvida inte den här egenskapen är angiven till true.</span><span class="sxs-lookup"><span data-stu-id="de386-122">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="de386-123">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="de386-123">-ClusterName</span></span>
<span data-ttu-id="de386-124">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="de386-124">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de386-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de386-125">-DefaultProfile</span></span>
<span data-ttu-id="de386-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="de386-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-127">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="de386-127">-ForceUpdateTag</span></span>
<span data-ttu-id="de386-128">Om ett värde anges och skiljer sig från det tidigare värdet tvingas förlängnings hanteraren att uppdateras även om tilläggs konfigurationen inte har ändrats.</span><span class="sxs-lookup"><span data-stu-id="de386-128">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de386-129">-InputObject</span></span>
<span data-ttu-id="de386-130">Resurs för nodtyp</span><span class="sxs-lookup"><span data-stu-id="de386-130">Node Type resource</span></span>

```yaml
Type: PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de386-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="de386-131">-Name</span></span>
<span data-ttu-id="de386-132">namn på tillägg.</span><span class="sxs-lookup"><span data-stu-id="de386-132">extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-133">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="de386-133">-NodeTypeName</span></span>
<span data-ttu-id="de386-134">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="de386-134">Specify the name of the node type.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de386-135">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="de386-135">-ProtectedSetting</span></span>
<span data-ttu-id="de386-136">Tillägget kan innehålla antingen protectedSettings eller protectedSettingsFromKeyVault eller inga skyddade inställningar alls.</span><span class="sxs-lookup"><span data-stu-id="de386-136">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-137">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="de386-137">-ProvisionAfterExtension</span></span>
<span data-ttu-id="de386-138">Samling med tilläggs namn efter vilka tillägget måste etableras.</span><span class="sxs-lookup"><span data-stu-id="de386-138">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="de386-139">-Publisher</span><span class="sxs-lookup"><span data-stu-id="de386-139">-Publisher</span></span>
<span data-ttu-id="de386-140">Namnet på tilläggs hanterarens utgivare.</span><span class="sxs-lookup"><span data-stu-id="de386-140">The name of the extension handler publisher.</span></span>
<span data-ttu-id="de386-141">Detta kan använda Get-AzVMImagePublisher cmdlet för att skaffa utgivaren.</span><span class="sxs-lookup"><span data-stu-id="de386-141">This can use the Get-AzVMImagePublisher cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de386-142">-ResourceGroupName</span></span>
<span data-ttu-id="de386-143">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="de386-143">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de386-144">-Ställ in</span><span class="sxs-lookup"><span data-stu-id="de386-144">-Setting</span></span>
<span data-ttu-id="de386-145">JSON-formaterade offentliga inställningar för tillägget.</span><span class="sxs-lookup"><span data-stu-id="de386-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-146">– Skriv</span><span class="sxs-lookup"><span data-stu-id="de386-146">-Type</span></span>
<span data-ttu-id="de386-147">Anger typen av förlängning; ett exempel är "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="de386-147">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
<span data-ttu-id="de386-148">Du kan använda Get-AzVMExtensionImageType cmdlet för att få fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="de386-148">You can use the Get-AzVMExtensionImageType cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="de386-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="de386-150">Anger versionen för skript hanteraren.</span><span class="sxs-lookup"><span data-stu-id="de386-150">Specifies the version of the script handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de386-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de386-151">-Confirm</span></span>
<span data-ttu-id="de386-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de386-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de386-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de386-153">-WhatIf</span></span>
<span data-ttu-id="de386-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de386-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de386-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de386-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de386-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de386-156">CommonParameters</span></span>
<span data-ttu-id="de386-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de386-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de386-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de386-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de386-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de386-159">INPUTS</span></span>

### <span data-ttu-id="de386-160">System. String</span><span class="sxs-lookup"><span data-stu-id="de386-160">System.String</span></span>

### <span data-ttu-id="de386-161">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="de386-161">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="de386-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de386-162">OUTPUTS</span></span>

### <span data-ttu-id="de386-163">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="de386-163">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="de386-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de386-164">NOTES</span></span>

## <span data-ttu-id="de386-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de386-165">RELATED LINKS</span></span>
