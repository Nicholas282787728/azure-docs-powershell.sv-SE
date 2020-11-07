---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922224"
---
# <span data-ttu-id="d9da3-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9da3-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="d9da3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9da3-102">SYNOPSIS</span></span>
<span data-ttu-id="d9da3-103">Hämtar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d9da3-103">Gets a public IP address.</span></span>

## <span data-ttu-id="d9da3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9da3-104">SYNTAX</span></span>

### <span data-ttu-id="d9da3-105">NoExpandStandAloneIp (standard)</span><span class="sxs-lookup"><span data-stu-id="d9da3-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9da3-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="d9da3-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9da3-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d9da3-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9da3-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="d9da3-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9da3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9da3-109">DESCRIPTION</span></span>
<span data-ttu-id="d9da3-110">Cmdleten **Get-AzPublicIPAddress** har en eller flera offentliga IP-adresser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d9da3-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="d9da3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9da3-111">EXAMPLES</span></span>

### <span data-ttu-id="d9da3-112">1: skaffa en offentlig IP-resurs</span><span class="sxs-lookup"><span data-stu-id="d9da3-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="d9da3-113">Det här kommandot får en offentlig IP-adressresurs med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="d9da3-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="d9da3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9da3-114">PARAMETERS</span></span>

### <span data-ttu-id="d9da3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9da3-115">-DefaultProfile</span></span>
<span data-ttu-id="d9da3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9da3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9da3-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d9da3-117">-ExpandResource</span></span>
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

### <span data-ttu-id="d9da3-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d9da3-118">-IpConfigurationName</span></span>
<span data-ttu-id="d9da3-119">IP-konfigurations namn för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d9da3-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="d9da3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9da3-120">-Name</span></span>
<span data-ttu-id="d9da3-121">Anger namnet på den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d9da3-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9da3-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d9da3-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="d9da3-123">Namn på den virtuella datorns nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d9da3-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="d9da3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9da3-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9da3-125">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d9da3-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d9da3-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="d9da3-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="d9da3-127">Index för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d9da3-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="d9da3-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d9da3-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="d9da3-129">Namn på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="d9da3-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="d9da3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9da3-130">CommonParameters</span></span>
<span data-ttu-id="d9da3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9da3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9da3-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9da3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9da3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9da3-133">INPUTS</span></span>

## <span data-ttu-id="d9da3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9da3-134">OUTPUTS</span></span>

### <span data-ttu-id="d9da3-135">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9da3-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d9da3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9da3-136">NOTES</span></span>

## <span data-ttu-id="d9da3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9da3-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9da3-138">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9da3-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d9da3-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9da3-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="d9da3-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d9da3-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


