---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931293"
---
# <span data-ttu-id="89ab4-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89ab4-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="89ab4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89ab4-102">SYNOPSIS</span></span>
<span data-ttu-id="89ab4-103">Hämtar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="89ab4-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ab4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89ab4-104">SYNTAX</span></span>

### <span data-ttu-id="89ab4-105">NoExpandStandAloneNic (standard)</span><span class="sxs-lookup"><span data-stu-id="89ab4-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ab4-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="89ab4-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ab4-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="89ab4-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ab4-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="89ab4-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89ab4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89ab4-109">DESCRIPTION</span></span>
<span data-ttu-id="89ab4-110">Cmdleten **Get-AzureRmNetworkInterface** får ett Azure-nätverkskort eller en lista med Azure Network-gränssnitt i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="89ab4-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="89ab4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89ab4-111">EXAMPLES</span></span>

### <span data-ttu-id="89ab4-112">Exempel 1: skaffa alla nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="89ab4-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="89ab4-113">Det här kommandot får alla nätverks gränssnitt för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="89ab4-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="89ab4-114">Exempel 2: Hämta alla nätverks gränssnitt med ett specifikt etablerings tillstånd</span><span class="sxs-lookup"><span data-stu-id="89ab4-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="89ab4-115">Det här kommandot får alla nätverks gränssnitt i resurs gruppen som heter ResourceGroup1 och som har ett etablerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="89ab4-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="89ab4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89ab4-116">PARAMETERS</span></span>

### <span data-ttu-id="89ab4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ab4-117">-DefaultProfile</span></span>
<span data-ttu-id="89ab4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89ab4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89ab4-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="89ab4-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ab4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="89ab4-120">-Name</span></span>
<span data-ttu-id="89ab4-121">Anger namnet på det nätverks gränssnitt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="89ab4-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ab4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ab4-122">-ResourceGroupName</span></span>
<span data-ttu-id="89ab4-123">Anger namnet på den resurs grupp från vilken denna cmdlet får nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="89ab4-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ab4-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="89ab4-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="89ab4-125">Anger det virtuella dator indexet för den virtuella datorns skal uppsättning som denna cmdlet hämtar nätverks gränssnitten från.</span><span class="sxs-lookup"><span data-stu-id="89ab4-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ab4-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89ab4-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="89ab4-127">Anger namnet på den skalnings uppsättning för virtuell dator från vilken denna cmdlet hämtar nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="89ab4-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ab4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ab4-128">CommonParameters</span></span>
<span data-ttu-id="89ab4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ab4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ab4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ab4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ab4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89ab4-131">INPUTS</span></span>

## <span data-ttu-id="89ab4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89ab4-132">OUTPUTS</span></span>

### <span data-ttu-id="89ab4-133">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89ab4-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="89ab4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89ab4-134">NOTES</span></span>

## <span data-ttu-id="89ab4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89ab4-135">RELATED LINKS</span></span>

[<span data-ttu-id="89ab4-136">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89ab4-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="89ab4-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89ab4-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="89ab4-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89ab4-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


