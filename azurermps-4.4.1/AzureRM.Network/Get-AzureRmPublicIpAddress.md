---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583820"
---
# <span data-ttu-id="9e69b-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e69b-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="9e69b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e69b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e69b-103">Hämtar en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="9e69b-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e69b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e69b-104">SYNTAX</span></span>

### <span data-ttu-id="9e69b-105">NoExpandStandAloneIp (standard)</span><span class="sxs-lookup"><span data-stu-id="9e69b-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e69b-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="9e69b-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e69b-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="9e69b-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e69b-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="9e69b-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e69b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e69b-109">DESCRIPTION</span></span>
<span data-ttu-id="9e69b-110">Cmdleten **Get-AzureRmPublicIPAddress** har en eller flera offentliga IP-adresser i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9e69b-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="9e69b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e69b-111">EXAMPLES</span></span>

### <span data-ttu-id="9e69b-112">1: skaffa en offentlig IP-resurs</span><span class="sxs-lookup"><span data-stu-id="9e69b-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="9e69b-113">Det här kommandot får en offentlig IP-adressresurs med namnet $publicIPName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="9e69b-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="9e69b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e69b-114">PARAMETERS</span></span>

### <span data-ttu-id="9e69b-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9e69b-115">-ExpandResource</span></span>
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

### <span data-ttu-id="9e69b-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9e69b-116">-IpConfigurationName</span></span>
<span data-ttu-id="9e69b-117">IP-konfigurations namn för nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="9e69b-117">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="9e69b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e69b-118">-Name</span></span>
<span data-ttu-id="9e69b-119">Anger namnet på den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9e69b-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e69b-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9e69b-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="9e69b-121">Namn på den virtuella datorns nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="9e69b-121">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="9e69b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e69b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9e69b-123">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="9e69b-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e69b-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="9e69b-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="9e69b-125">Index för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9e69b-125">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="9e69b-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9e69b-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="9e69b-127">Namn på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9e69b-127">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="9e69b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e69b-128">-DefaultProfile</span></span>
<span data-ttu-id="9e69b-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e69b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e69b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e69b-130">CommonParameters</span></span>
<span data-ttu-id="9e69b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e69b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e69b-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e69b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e69b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e69b-133">INPUTS</span></span>

## <span data-ttu-id="9e69b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e69b-134">OUTPUTS</span></span>

### <span data-ttu-id="9e69b-135">Microsoft. Azure. commands. Networks. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e69b-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9e69b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e69b-136">NOTES</span></span>

## <span data-ttu-id="9e69b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e69b-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e69b-138">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e69b-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9e69b-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e69b-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="9e69b-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9e69b-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


