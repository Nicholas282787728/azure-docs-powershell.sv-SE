---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRm.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyalias
schema: 2.0.0
ms.openlocfilehash: f0f8f3ded2697e713215929f66ebd82b3af03ea0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930109"
---
# <span data-ttu-id="0aeca-101">Get-AzureRmPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="0aeca-101">Get-AzureRmPolicyAlias</span></span>

## <span data-ttu-id="0aeca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0aeca-102">SYNOPSIS</span></span>
<span data-ttu-id="0aeca-103">Get-AzureRmPolicyAlias hämtar och matar ut de Azure Provider-filtyper som har alias definierade och som matchar de givna parameter värdena.</span><span class="sxs-lookup"><span data-stu-id="0aeca-103">Get-AzureRmPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="0aeca-104">Om det inte finns några parametrar kommer alla resurs typer för leverantörer som innehåller ett alias att matas ut.</span><span class="sxs-lookup"><span data-stu-id="0aeca-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="0aeca-105">Växeln-ListAvailable ändrar det här beteendet genom att visa alla matchande resurs typer, inklusive sådana som saknar alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aeca-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0aeca-106">SYNTAX</span></span>

```
Get-AzureRmPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aeca-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0aeca-107">DESCRIPTION</span></span>
<span data-ttu-id="0aeca-108">Cmdleten **Get-AzureRmPolicyAlias** hämtar en lista över princip Ali Aset.</span><span class="sxs-lookup"><span data-stu-id="0aeca-108">The **Get-AzureRmPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="0aeca-109">Princip Ali Aset används av Azure policy för att referera till resurs typs egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0aeca-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="0aeca-110">Parametrar tillhandahålls som begränsar objekt i listan genom att matcha olika egenskaper för resurs typen eller dess alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="0aeca-111">Ett angivet matchnings värde matchar om mål strängen innehåller en Skift läges okänslig jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0aeca-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="0aeca-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0aeca-112">EXAMPLES</span></span>

### <span data-ttu-id="0aeca-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0aeca-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="0aeca-114">Visar alla resurs typer för leverantörer som har ett alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="0aeca-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0aeca-115">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="0aeca-116">Visar alla resurs typer för leverantörer, inklusive dem som inte har alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="0aeca-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0aeca-117">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="0aeca-118">Visar alla leverantörs resurs typer vars namnrymd matchar ' Compute ' och innehåller ett alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="0aeca-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="0aeca-119">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="0aeca-120">Visar alla leverantörs resurs typer vars resurs typ matchar "virtuellt" och som innehåller ett alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="0aeca-121">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="0aeca-121">Example 5</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="0aeca-122">Visar alla leverantörs resurs typer vars resurs typ matchar "virtuellt", inklusive dem som inte har alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="0aeca-123">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="0aeca-123">Example 6</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="0aeca-124">Visar alla leverantörs resurs typer vars namnrymd matchar "Compute" och resurs typen matchar "Virtual" och innehåller ett alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="0aeca-125">Obs!-NamespaceMatch och-ResourceTypeMatch ger exklusiva träffar, medan de andra är med.</span><span class="sxs-lookup"><span data-stu-id="0aeca-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="0aeca-126">Exempel 7</span><span class="sxs-lookup"><span data-stu-id="0aeca-126">Example 7</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="0aeca-127">Visar alla resurs typer för leverantörer som innehåller ett alias som matchar "virtuell".</span><span class="sxs-lookup"><span data-stu-id="0aeca-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="0aeca-128">Exempel 8</span><span class="sxs-lookup"><span data-stu-id="0aeca-128">Example 8</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="0aeca-129">Visar alla leverantörs resurs typer som innehåller ett alias som matchar "virtuellt" eller ett alias med en sökväg som matchar ' nätverk '.</span><span class="sxs-lookup"><span data-stu-id="0aeca-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="0aeca-130">Exempel 9</span><span class="sxs-lookup"><span data-stu-id="0aeca-130">Example 9</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="0aeca-131">Visar alla leverantörs resurs typer med alfa API-versionen eller som innehåller ett alias med en alpha API-version.</span><span class="sxs-lookup"><span data-stu-id="0aeca-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="0aeca-132">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0aeca-132">PARAMETERS</span></span>

### <span data-ttu-id="0aeca-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-133">-AliasMatch</span></span>
<span data-ttu-id="0aeca-134">Inkluderar i utdatafilerna med alias vars namn matchar det här värdet.</span><span class="sxs-lookup"><span data-stu-id="0aeca-134">Includes in the output items with aliases whose name matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0aeca-135">-ApiVersion</span></span>
<span data-ttu-id="0aeca-136">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0aeca-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="0aeca-137">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="0aeca-137">If not specified, the API version is automatically determined as the latest available.</span></span>
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

### <span data-ttu-id="0aeca-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-138">-ApiVersionMatch</span></span>
<span data-ttu-id="0aeca-139">Inkluderar i de utmatnings objekt vars resurs typer eller alias har en matchande API-version.</span><span class="sxs-lookup"><span data-stu-id="0aeca-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>
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

### <span data-ttu-id="0aeca-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aeca-140">-DefaultProfile</span></span>
<span data-ttu-id="0aeca-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0aeca-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="0aeca-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0aeca-142">-ListAvailable</span></span>
<span data-ttu-id="0aeca-143">Inkluderar i objekten utdata med och utan alias.</span><span class="sxs-lookup"><span data-stu-id="0aeca-143">Includes in the output matching items with and without aliases.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-144">-LocationMatch</span></span>
<span data-ttu-id="0aeca-145">Inkluderar i de utmatnings objekt vars resurs typer har en matchande plats.</span><span class="sxs-lookup"><span data-stu-id="0aeca-145">Includes in the output items whose resource types have a matching location.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-146">-NamespaceMatch</span></span>
<span data-ttu-id="0aeca-147">Begränsar resultatet till objekt vars namn område matchar det här värdet.</span><span class="sxs-lookup"><span data-stu-id="0aeca-147">Limits the output to items whose namespace matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-148">-PathMatch</span></span>
<span data-ttu-id="0aeca-149">Inkluderar objekt med alias som innehåller en sökväg som matchar det här värdet.</span><span class="sxs-lookup"><span data-stu-id="0aeca-149">Includes in the output items with aliases containing a path that matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-150">-För</span><span class="sxs-lookup"><span data-stu-id="0aeca-150">-Pre</span></span>
<span data-ttu-id="0aeca-151">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0aeca-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>
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

### <span data-ttu-id="0aeca-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="0aeca-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="0aeca-153">Begränsar resultatet till objekt vars resurs typ matchar det här värdet.</span><span class="sxs-lookup"><span data-stu-id="0aeca-153">Limits the output to items whose resource type matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aeca-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aeca-154">CommonParameters</span></span>
<span data-ttu-id="0aeca-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aeca-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aeca-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aeca-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aeca-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0aeca-157">INPUTS</span></span>

## <span data-ttu-id="0aeca-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0aeca-158">OUTPUTS</span></span>

### <span data-ttu-id="0aeca-159">Microsoft. Azure. commands. ResourceManager. cmdlets. implementation. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="0aeca-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="0aeca-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0aeca-160">NOTES</span></span>

* <span data-ttu-id="0aeca-161">Om du vill expandera alias eller andra egenskaper går du till utdata till `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="0aeca-161">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="0aeca-162">Till exempel: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="0aeca-162">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="0aeca-163">Ytterligare egenskaper är tillgängliga i utdata och kan visas genom att överföra utdata till `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="0aeca-163">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="0aeca-164">Till exempel: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="0aeca-164">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="0aeca-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0aeca-165">RELATED LINKS</span></span>