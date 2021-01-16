---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409400"
---
# <span data-ttu-id="b0313-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0313-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="b0313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0313-102">SYNOPSIS</span></span>
<span data-ttu-id="b0313-103">Hämtar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="b0313-103">Gets a public IP address.</span></span>

## <span data-ttu-id="b0313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0313-104">SYNTAX</span></span>

### <span data-ttu-id="b0313-105">NoExpandStandAloneIp (standard)</span><span class="sxs-lookup"><span data-stu-id="b0313-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0313-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="b0313-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0313-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b0313-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0313-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="b0313-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0313-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0313-109">DESCRIPTION</span></span>
<span data-ttu-id="b0313-110">Cmdleten **Get-AzPublicIPAddress** har en eller flera offentliga IP-adresser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b0313-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="b0313-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0313-111">EXAMPLES</span></span>

### <span data-ttu-id="b0313-112">Exempel 1: skaffa en offentlig IP-resurs</span><span class="sxs-lookup"><span data-stu-id="b0313-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="b0313-113">Det här kommandot får en offentlig IP-adressresurs med namnet myPublicIp i resurs gruppen myRg.</span><span class="sxs-lookup"><span data-stu-id="b0313-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="b0313-114">Exempel 2: Hämta offentliga IP-resurser med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="b0313-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="b0313-115">Det här kommandot får alla offentliga IP-adressresurser vars namn börjar med myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="b0313-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="b0313-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0313-116">PARAMETERS</span></span>

### <span data-ttu-id="b0313-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0313-117">-DefaultProfile</span></span>
<span data-ttu-id="b0313-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0313-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0313-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="b0313-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0313-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b0313-120">-IpConfigurationName</span></span>
<span data-ttu-id="b0313-121">IP-konfigurations namn för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b0313-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0313-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0313-122">-Name</span></span>
<span data-ttu-id="b0313-123">Anger namnet på den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b0313-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b0313-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b0313-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="b0313-125">Namn på den virtuella datorns nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="b0313-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0313-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0313-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0313-127">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b0313-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b0313-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="b0313-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="b0313-129">Index för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b0313-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0313-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b0313-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="b0313-131">Namn på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b0313-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0313-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0313-132">CommonParameters</span></span>
<span data-ttu-id="b0313-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0313-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0313-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0313-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0313-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0313-135">INPUTS</span></span>

### <span data-ttu-id="b0313-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b0313-136">System.String</span></span>

## <span data-ttu-id="b0313-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0313-137">OUTPUTS</span></span>

### <span data-ttu-id="b0313-138">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0313-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b0313-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0313-139">NOTES</span></span>

## <span data-ttu-id="b0313-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0313-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0313-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0313-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="b0313-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0313-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="b0313-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="b0313-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


