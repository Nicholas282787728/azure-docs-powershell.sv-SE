---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 42d5ef31b49f8abe5c8e582e0a85e8766a71b9a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584644"
---
# <span data-ttu-id="56d51-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56d51-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="56d51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56d51-102">SYNOPSIS</span></span>
<span data-ttu-id="56d51-103">Hämtar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="56d51-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56d51-104">SYNTAX</span></span>

### <span data-ttu-id="56d51-105">NoExpandStandAloneNic (standard)</span><span class="sxs-lookup"><span data-stu-id="56d51-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56d51-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="56d51-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56d51-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="56d51-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56d51-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="56d51-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56d51-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56d51-109">DESCRIPTION</span></span>
<span data-ttu-id="56d51-110">Cmdleten **Get-AzureRmNetworkInterface** får ett Azure-nätverkskort eller en lista med Azure Network-gränssnitt i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="56d51-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="56d51-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56d51-111">EXAMPLES</span></span>

### <span data-ttu-id="56d51-112">Exempel 1: skaffa alla nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="56d51-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="56d51-113">Det här kommandot får alla nätverks gränssnitt för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="56d51-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="56d51-114">Exempel 2: Hämta alla nätverks gränssnitt med ett specifikt etablerings tillstånd</span><span class="sxs-lookup"><span data-stu-id="56d51-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="56d51-115">Det här kommandot får alla nätverks gränssnitt i resurs gruppen som heter ResourceGroup1 och som har ett etablerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="56d51-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="56d51-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56d51-116">PARAMETERS</span></span>

### <span data-ttu-id="56d51-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="56d51-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d51-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="56d51-118">-Name</span></span>
<span data-ttu-id="56d51-119">Anger namnet på det nätverks gränssnitt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="56d51-119">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d51-120">-ResourceGroupName</span></span>
<span data-ttu-id="56d51-121">Anger namnet på den resurs grupp från vilken denna cmdlet får nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="56d51-121">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d51-122">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="56d51-122">-VirtualMachineIndex</span></span>
<span data-ttu-id="56d51-123">Anger det virtuella dator indexet för den virtuella datorns skal uppsättning som denna cmdlet hämtar nätverks gränssnitten från.</span><span class="sxs-lookup"><span data-stu-id="56d51-123">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d51-124">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="56d51-124">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="56d51-125">Anger namnet på den skalnings uppsättning för virtuell dator från vilken denna cmdlet hämtar nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="56d51-125">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d51-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d51-126">-DefaultProfile</span></span>
<span data-ttu-id="56d51-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56d51-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d51-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d51-128">CommonParameters</span></span>
<span data-ttu-id="56d51-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d51-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d51-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d51-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d51-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56d51-131">INPUTS</span></span>

## <span data-ttu-id="56d51-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56d51-132">OUTPUTS</span></span>

### <span data-ttu-id="56d51-133">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56d51-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="56d51-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56d51-134">NOTES</span></span>

## <span data-ttu-id="56d51-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56d51-135">RELATED LINKS</span></span>

[<span data-ttu-id="56d51-136">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56d51-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="56d51-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56d51-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="56d51-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56d51-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


