---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 769fd151f68da6a38c1cf4d5b3636d7990a92943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574926"
---
# <span data-ttu-id="8bb1a-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bb1a-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="8bb1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bb1a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb1a-103">Hämtar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bb1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bb1a-104">SYNTAX</span></span>

### <span data-ttu-id="8bb1a-105">NoExpandStandAloneIp (standard)</span><span class="sxs-lookup"><span data-stu-id="8bb1a-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb1a-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="8bb1a-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb1a-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8bb1a-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bb1a-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="8bb1a-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bb1a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bb1a-109">DESCRIPTION</span></span>
<span data-ttu-id="8bb1a-110">Cmdleten **Get-AzureRmPublicIPAddress** har en eller flera offentliga IP-adresser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="8bb1a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bb1a-111">EXAMPLES</span></span>

### <span data-ttu-id="8bb1a-112">1: skaffa en offentlig IP-resurs</span><span class="sxs-lookup"><span data-stu-id="8bb1a-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="8bb1a-113">Det här kommandot får en offentlig IP-adressresurs med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="8bb1a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bb1a-114">PARAMETERS</span></span>

### <span data-ttu-id="8bb1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb1a-115">-DefaultProfile</span></span>
<span data-ttu-id="8bb1a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bb1a-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8bb1a-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8bb1a-118">-IpConfigurationName</span></span>
<span data-ttu-id="8bb1a-119">IP-konfigurations namn för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8bb1a-120">-Name</span></span>
<span data-ttu-id="8bb1a-121">Anger namnet på den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8bb1a-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="8bb1a-123">Namn på den virtuella datorns nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bb1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8bb1a-125">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="8bb1a-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="8bb1a-127">Index för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8bb1a-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="8bb1a-129">Namn på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb1a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb1a-130">CommonParameters</span></span>
<span data-ttu-id="8bb1a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb1a-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bb1a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb1a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bb1a-133">INPUTS</span></span>

### <span data-ttu-id="8bb1a-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="8bb1a-134">None</span></span>
<span data-ttu-id="8bb1a-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8bb1a-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8bb1a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bb1a-136">OUTPUTS</span></span>

### <span data-ttu-id="8bb1a-137">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bb1a-137">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8bb1a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bb1a-138">NOTES</span></span>

## <span data-ttu-id="8bb1a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bb1a-139">RELATED LINKS</span></span>

[<span data-ttu-id="8bb1a-140">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bb1a-140">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8bb1a-141">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bb1a-141">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8bb1a-142">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8bb1a-142">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


