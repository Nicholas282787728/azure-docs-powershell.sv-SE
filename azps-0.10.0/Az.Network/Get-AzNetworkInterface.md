---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922261"
---
# <span data-ttu-id="3eeb3-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3eeb3-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="3eeb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3eeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="3eeb3-103">Hämtar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-103">Gets a network interface.</span></span>

## <span data-ttu-id="3eeb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3eeb3-104">SYNTAX</span></span>

### <span data-ttu-id="3eeb3-105">NoExpandStandAloneNic (standard)</span><span class="sxs-lookup"><span data-stu-id="3eeb3-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eeb3-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="3eeb3-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eeb3-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="3eeb3-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eeb3-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="3eeb3-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3eeb3-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3eeb3-109">DESCRIPTION</span></span>
<span data-ttu-id="3eeb3-110">Cmdleten **Get-AzNetworkInterface** får ett Azure-nätverkskort eller en lista med Azure Network-gränssnitt i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="3eeb3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3eeb3-111">EXAMPLES</span></span>

### <span data-ttu-id="3eeb3-112">Exempel 1: skaffa alla nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="3eeb3-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="3eeb3-113">Det här kommandot får alla nätverks gränssnitt för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="3eeb3-114">Exempel 2: Hämta alla nätverks gränssnitt med ett specifikt etablerings tillstånd</span><span class="sxs-lookup"><span data-stu-id="3eeb3-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="3eeb3-115">Det här kommandot får alla nätverks gränssnitt i resurs gruppen som heter ResourceGroup1 och som har ett etablerings tillstånd.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="3eeb3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3eeb3-116">PARAMETERS</span></span>

### <span data-ttu-id="3eeb3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eeb3-117">-DefaultProfile</span></span>
<span data-ttu-id="3eeb3-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eeb3-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="3eeb3-119">-ExpandResource</span></span>
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

### <span data-ttu-id="3eeb3-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3eeb3-120">-Name</span></span>
<span data-ttu-id="3eeb3-121">Anger namnet på det nätverks gränssnitt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3eeb3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eeb3-122">-ResourceGroupName</span></span>
<span data-ttu-id="3eeb3-123">Anger namnet på den resurs grupp från vilken denna cmdlet får nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="3eeb3-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="3eeb3-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="3eeb3-125">Anger det virtuella dator indexet för den virtuella datorns skal uppsättning som denna cmdlet hämtar nätverks gränssnitten från.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="3eeb3-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3eeb3-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="3eeb3-127">Anger namnet på den skalnings uppsättning för virtuell dator från vilken denna cmdlet hämtar nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="3eeb3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eeb3-128">CommonParameters</span></span>
<span data-ttu-id="3eeb3-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eeb3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eeb3-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eeb3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eeb3-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3eeb3-131">INPUTS</span></span>

## <span data-ttu-id="3eeb3-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3eeb3-132">OUTPUTS</span></span>

### <span data-ttu-id="3eeb3-133">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3eeb3-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="3eeb3-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3eeb3-134">NOTES</span></span>

## <span data-ttu-id="3eeb3-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3eeb3-135">RELATED LINKS</span></span>

[<span data-ttu-id="3eeb3-136">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3eeb3-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="3eeb3-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3eeb3-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="3eeb3-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3eeb3-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


