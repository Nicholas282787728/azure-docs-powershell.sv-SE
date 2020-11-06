---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576243"
---
# <span data-ttu-id="f11f0-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f11f0-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="f11f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f11f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f11f0-103">Hämtar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="f11f0-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f11f0-104">SYNTAX</span></span>

### <span data-ttu-id="f11f0-105">NoExpandStandAloneIp (standard)</span><span class="sxs-lookup"><span data-stu-id="f11f0-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f11f0-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="f11f0-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f11f0-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f11f0-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f11f0-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="f11f0-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f11f0-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f11f0-109">DESCRIPTION</span></span>
<span data-ttu-id="f11f0-110">Cmdleten **Get-AzureRmPublicIPAddress** har en eller flera offentliga IP-adresser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f11f0-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="f11f0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f11f0-111">EXAMPLES</span></span>

### <span data-ttu-id="f11f0-112">1: skaffa en offentlig IP-resurs</span><span class="sxs-lookup"><span data-stu-id="f11f0-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="f11f0-113">Det här kommandot får en offentlig IP-adressresurs med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="f11f0-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="f11f0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f11f0-114">PARAMETERS</span></span>

### <span data-ttu-id="f11f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11f0-115">-DefaultProfile</span></span>
<span data-ttu-id="f11f0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f11f0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11f0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f11f0-117">-ExpandResource</span></span>
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

### <span data-ttu-id="f11f0-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f11f0-118">-IpConfigurationName</span></span>
<span data-ttu-id="f11f0-119">IP-konfigurations namn för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f11f0-119">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="f11f0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f11f0-120">-Name</span></span>
<span data-ttu-id="f11f0-121">Anger namnet på den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f11f0-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11f0-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f11f0-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="f11f0-123">Namn på den virtuella datorns nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="f11f0-123">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="f11f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f11f0-125">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="f11f0-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11f0-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="f11f0-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="f11f0-127">Index för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="f11f0-127">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="f11f0-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f11f0-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="f11f0-129">Namn på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f11f0-129">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="f11f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11f0-130">CommonParameters</span></span>
<span data-ttu-id="f11f0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11f0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11f0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11f0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f11f0-133">INPUTS</span></span>

### <span data-ttu-id="f11f0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f11f0-134">System.String</span></span>

## <span data-ttu-id="f11f0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f11f0-135">OUTPUTS</span></span>

### <span data-ttu-id="f11f0-136">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f11f0-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f11f0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f11f0-137">NOTES</span></span>

## <span data-ttu-id="f11f0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f11f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="f11f0-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f11f0-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f11f0-140">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f11f0-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="f11f0-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f11f0-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


