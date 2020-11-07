---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: de91566be3c9bcd62f28dbcba80409622e86a4b5
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93758455"
---
# <span data-ttu-id="40984-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="40984-101">Get-AzResource</span></span>

## <span data-ttu-id="40984-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40984-102">SYNOPSIS</span></span>

<span data-ttu-id="40984-103">Hämtar resurser.</span><span class="sxs-lookup"><span data-stu-id="40984-103">Gets resources.</span></span>

## <span data-ttu-id="40984-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40984-104">SYNTAX</span></span>

### <span data-ttu-id="40984-105">ByTagNameValueParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="40984-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40984-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="40984-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40984-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40984-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40984-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40984-108">DESCRIPTION</span></span>

<span data-ttu-id="40984-109">Cmdleten **Get-AzResource** får Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="40984-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="40984-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40984-110">EXAMPLES</span></span>

### <span data-ttu-id="40984-111">Exempel 1: Hämta alla resurser i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="40984-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="40984-112">Det här kommandot får alla resurser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="40984-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="40984-113">Exempel 2: Hämta alla resurser i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="40984-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="40984-114">Det här kommandot får alla resurser i resurs gruppen "testRG".</span><span class="sxs-lookup"><span data-stu-id="40984-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="40984-115">Exempel 3: Hämta alla resurser vars resurs grupp matchar det tillhandahållna jokertecken</span><span class="sxs-lookup"><span data-stu-id="40984-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="40984-116">Det här kommandot får alla resurser vars resurs grupp de tillhör "annat".</span><span class="sxs-lookup"><span data-stu-id="40984-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="40984-117">Exempel 4: Hämta alla resurser med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="40984-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="40984-118">Det här kommandot får alla resurser vars resurs namn är "testVM".</span><span class="sxs-lookup"><span data-stu-id="40984-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="40984-119">Exempel 5: Hämta alla resurser vars namn matchar det tillhandahållna jokertecken</span><span class="sxs-lookup"><span data-stu-id="40984-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="40984-120">Det här kommandot får alla resurser vars resurs namn börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="40984-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="40984-121">Exempel 6: Hämta alla resurser av en viss resurs typ</span><span class="sxs-lookup"><span data-stu-id="40984-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="40984-122">Det här kommandot får alla resurser i de aktuella prenumerationerna som är virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="40984-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="40984-123">Exempel 7: Hämta en resurs efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="40984-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="40984-124">Med det här kommandot får du resursen ett angivet resurs-ID, som är en virtuell dator som heter "testVM" i resurs gruppen "testRG".</span><span class="sxs-lookup"><span data-stu-id="40984-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="40984-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40984-125">PARAMETERS</span></span>

### <span data-ttu-id="40984-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="40984-126">-ApiVersion</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40984-127">-DefaultProfile</span></span>
<span data-ttu-id="40984-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40984-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40984-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="40984-129">-ExpandProperties</span></span>
<span data-ttu-id="40984-130">Expanderar egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="40984-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="40984-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="40984-131">-Name</span></span>
<span data-ttu-id="40984-132">Namnet på den eller de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="40984-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="40984-133">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="40984-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="40984-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="40984-134">-ODataQuery</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-135">-För</span><span class="sxs-lookup"><span data-stu-id="40984-135">-Pre</span></span>

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

### <span data-ttu-id="40984-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40984-136">-ResourceGroupName</span></span>
<span data-ttu-id="40984-137">Den resurs grupp som retireved hör till.</span><span class="sxs-lookup"><span data-stu-id="40984-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="40984-138">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="40984-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="40984-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40984-139">-ResourceId</span></span>
<span data-ttu-id="40984-140">Anger det fullständiga resurs-ID: t, som i följande exempel `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="40984-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40984-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="40984-141">-ResourceType</span></span>
<span data-ttu-id="40984-142">Resurs typen för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="40984-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="40984-143">Till exempel Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="40984-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="40984-144">-Tag</span></span>

<span data-ttu-id="40984-145">Hämtar resurser som har den angivna Azure-taggen.</span><span class="sxs-lookup"><span data-stu-id="40984-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="40984-146">Ange en hash-tabell med en namn nyckel eller namn-och värde nycklar.</span><span class="sxs-lookup"><span data-stu-id="40984-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="40984-147">Jokertecken stöds inte. En "tagg" är ett namn värde par som du kan använda för resurser och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="40984-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="40984-148">Använd taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="40984-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="40984-149">Om du vill lägga till en tagg till en resurs använder du parametern tagg för New-AzResource eller Set-AzResource cmdletar.</span><span class="sxs-lookup"><span data-stu-id="40984-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="40984-150">Använd New-AzTag cmdlet för att skapa en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="40984-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="40984-151">Om du behöver hjälp med hash-tabeller i Windows PowerShell kör du "Get-Help about_Hashtables".</span><span class="sxs-lookup"><span data-stu-id="40984-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="40984-152">-TagName</span></span>
<span data-ttu-id="40984-153">Den grundläggande flaggan för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="40984-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="40984-154">-TagValue</span></span>
<span data-ttu-id="40984-155">Värdet i taggen för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="40984-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40984-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40984-156">CommonParameters</span></span>
<span data-ttu-id="40984-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40984-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40984-158">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40984-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40984-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40984-159">INPUTS</span></span>

### <span data-ttu-id="40984-160">System. String</span><span class="sxs-lookup"><span data-stu-id="40984-160">System.String</span></span>

## <span data-ttu-id="40984-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40984-161">OUTPUTS</span></span>

### <span data-ttu-id="40984-162">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="40984-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="40984-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40984-163">NOTES</span></span>

## <span data-ttu-id="40984-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40984-164">RELATED LINKS</span></span>

[<span data-ttu-id="40984-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="40984-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="40984-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="40984-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="40984-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="40984-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="40984-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="40984-168">Set-AzResource</span></span>](./Set-AzResource.md)
