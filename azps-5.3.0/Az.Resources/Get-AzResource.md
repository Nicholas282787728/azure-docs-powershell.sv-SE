---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 738b2258f327cbe00b3162d39aaeebd647d1a2e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521512"
---
# <span data-ttu-id="1231d-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1231d-101">Get-AzResource</span></span>

## <span data-ttu-id="1231d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1231d-102">SYNOPSIS</span></span>

<span data-ttu-id="1231d-103">Hämtar resurser.</span><span class="sxs-lookup"><span data-stu-id="1231d-103">Gets resources.</span></span>

## <span data-ttu-id="1231d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1231d-104">SYNTAX</span></span>

### <span data-ttu-id="1231d-105">ByTagNameValueParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1231d-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1231d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1231d-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1231d-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1231d-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1231d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1231d-108">DESCRIPTION</span></span>

<span data-ttu-id="1231d-109">Cmdleten **Get-AzResource** får Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="1231d-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="1231d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1231d-110">EXAMPLES</span></span>

### <span data-ttu-id="1231d-111">Exempel 1: Hämta alla resurser i det aktuella abonnemanget</span><span class="sxs-lookup"><span data-stu-id="1231d-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="1231d-112">Det här kommandot får alla resurser i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1231d-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="1231d-113">Exempel 2: Hämta alla resurser i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="1231d-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="1231d-114">Det här kommandot får alla resurser i resurs gruppen "testRG".</span><span class="sxs-lookup"><span data-stu-id="1231d-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="1231d-115">Exempel 3: Hämta alla resurser vars resurs grupp matchar det tillhandahållna jokertecken</span><span class="sxs-lookup"><span data-stu-id="1231d-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="1231d-116">Det här kommandot får alla resurser vars resurs grupp de tillhör "annat".</span><span class="sxs-lookup"><span data-stu-id="1231d-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="1231d-117">Exempel 4: Hämta alla resurser med ett angivet namn</span><span class="sxs-lookup"><span data-stu-id="1231d-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="1231d-118">Det här kommandot får alla resurser vars resurs namn är "testVM".</span><span class="sxs-lookup"><span data-stu-id="1231d-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="1231d-119">Exempel 5: Hämta alla resurser vars namn matchar det tillhandahållna jokertecken</span><span class="sxs-lookup"><span data-stu-id="1231d-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="1231d-120">Det här kommandot får alla resurser vars resurs namn börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="1231d-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="1231d-121">Exempel 6: Hämta alla resurser av en viss resurs typ</span><span class="sxs-lookup"><span data-stu-id="1231d-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="1231d-122">Det här kommandot får alla resurser i de aktuella prenumerationerna som är virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="1231d-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="1231d-123">Exempel 7: Hämta en resurs efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="1231d-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="1231d-124">Med det här kommandot får du resursen ett angivet resurs-ID, som är en virtuell dator som heter "testVM" i resurs gruppen "testRG".</span><span class="sxs-lookup"><span data-stu-id="1231d-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="1231d-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1231d-125">PARAMETERS</span></span>

### <span data-ttu-id="1231d-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1231d-126">-ApiVersion</span></span>

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

### <span data-ttu-id="1231d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1231d-127">-DefaultProfile</span></span>
<span data-ttu-id="1231d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1231d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1231d-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="1231d-129">-ExpandProperties</span></span>
<span data-ttu-id="1231d-130">Expanderar egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="1231d-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="1231d-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="1231d-131">-Name</span></span>
<span data-ttu-id="1231d-132">Namnet på den eller de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1231d-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="1231d-133">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="1231d-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="1231d-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1231d-134">-ODataQuery</span></span>

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

### <span data-ttu-id="1231d-135">-För</span><span class="sxs-lookup"><span data-stu-id="1231d-135">-Pre</span></span>

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

### <span data-ttu-id="1231d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1231d-136">-ResourceGroupName</span></span>
<span data-ttu-id="1231d-137">Den resurs grupp som har hämtats.</span><span class="sxs-lookup"><span data-stu-id="1231d-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="1231d-138">Den här parametern har stöd för jokertecken i början och/eller slutet av strängen.</span><span class="sxs-lookup"><span data-stu-id="1231d-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="1231d-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1231d-139">-ResourceId</span></span>
<span data-ttu-id="1231d-140">Anger det fullständiga resurs-ID: t, som i följande exempel `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="1231d-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="1231d-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1231d-141">-ResourceType</span></span>
<span data-ttu-id="1231d-142">Resurs typen för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1231d-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="1231d-143">Till exempel Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="1231d-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="1231d-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1231d-144">-Tag</span></span>

<span data-ttu-id="1231d-145">Hämtar resurser som har den angivna Azure-taggen.</span><span class="sxs-lookup"><span data-stu-id="1231d-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="1231d-146">Ange en hash-tabell med en namn nyckel eller namn-och värde nycklar.</span><span class="sxs-lookup"><span data-stu-id="1231d-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="1231d-147">Jokertecken stöds inte. En "tagg" är ett namn värde par som du kan använda för resurser och resurs grupper.</span><span class="sxs-lookup"><span data-stu-id="1231d-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="1231d-148">Använd taggar för att kategorisera dina resurser, till exempel efter avdelning eller kostnads ställe, eller för att spåra anteckningar eller kommentarer om resurserna.</span><span class="sxs-lookup"><span data-stu-id="1231d-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="1231d-149">Om du vill lägga till en tagg till en resurs använder du parametern tagg för New-AzResource eller Set-AzResource cmdletar.</span><span class="sxs-lookup"><span data-stu-id="1231d-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="1231d-150">Använd New-AzTag cmdlet för att skapa en fördefinierad tagg.</span><span class="sxs-lookup"><span data-stu-id="1231d-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="1231d-151">Om du behöver hjälp med hash-tabeller i Windows PowerShell kör du "Get-Help about_Hashtables".</span><span class="sxs-lookup"><span data-stu-id="1231d-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="1231d-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="1231d-152">-TagName</span></span>
<span data-ttu-id="1231d-153">Den grundläggande flaggan för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1231d-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="1231d-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="1231d-154">-TagValue</span></span>
<span data-ttu-id="1231d-155">Värdet i taggen för de resurser som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="1231d-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="1231d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1231d-156">CommonParameters</span></span>
<span data-ttu-id="1231d-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1231d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1231d-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1231d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1231d-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1231d-159">INPUTS</span></span>

### <span data-ttu-id="1231d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="1231d-160">System.String</span></span>

## <span data-ttu-id="1231d-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1231d-161">OUTPUTS</span></span>

### <span data-ttu-id="1231d-162">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="1231d-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="1231d-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1231d-163">NOTES</span></span>

## <span data-ttu-id="1231d-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1231d-164">RELATED LINKS</span></span>

[<span data-ttu-id="1231d-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="1231d-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="1231d-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="1231d-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="1231d-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="1231d-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="1231d-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="1231d-168">Set-AzResource</span></span>](./Set-AzResource.md)