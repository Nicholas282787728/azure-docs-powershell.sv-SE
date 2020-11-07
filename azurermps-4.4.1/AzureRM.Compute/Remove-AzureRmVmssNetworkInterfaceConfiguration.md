---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 85f593c1d66b02f9982cecc4606603fbef1385d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755298"
---
# <span data-ttu-id="f0d97-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d97-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f0d97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0d97-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d97-103">Tar bort en konfiguration för nätverks gränssnitt från en VMSS.</span><span class="sxs-lookup"><span data-stu-id="f0d97-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0d97-104">SYNTAX</span></span>

### <span data-ttu-id="f0d97-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d97-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d97-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d97-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d97-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0d97-107">DESCRIPTION</span></span>
<span data-ttu-id="f0d97-108">Cmdleten **Remove-AzureRmVmssNetworkInterfaceConfiguration** tar bort en konfiguration för nätverks gränssnitt från en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f0d97-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f0d97-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0d97-109">EXAMPLES</span></span>

### <span data-ttu-id="f0d97-110">Exempel 1: ta bort en gränssnitts konfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d97-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="f0d97-111">Det första kommandot får en VMSS med hjälp av Get-AzureRmVmss cmdlet och lagrar den i $VMSS-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f0d97-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="f0d97-112">Med det andra kommandot tas konfigurationen för nätverks gränssnittet bort med namnet ContosoVmssInterface02 från uppsättningen i $VMSS.</span><span class="sxs-lookup"><span data-stu-id="f0d97-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="f0d97-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0d97-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d97-114">-DefaultProfile</span></span>
<span data-ttu-id="f0d97-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d97-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d97-116">-ID</span><span class="sxs-lookup"><span data-stu-id="f0d97-116">-Id</span></span>
<span data-ttu-id="f0d97-117">Anger ID: t för nätverks gränssnitts konfigurationen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f0d97-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d97-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0d97-118">-Name</span></span>
<span data-ttu-id="f0d97-119">Anger namnet på den nätverks gränssnitts konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f0d97-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d97-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0d97-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f0d97-121">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="f0d97-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d97-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0d97-122">-Confirm</span></span>
<span data-ttu-id="f0d97-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0d97-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d97-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d97-124">-WhatIf</span></span>
<span data-ttu-id="f0d97-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0d97-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0d97-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0d97-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d97-127">CommonParameters</span></span>
<span data-ttu-id="f0d97-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d97-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d97-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d97-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0d97-130">INPUTS</span></span>

## <span data-ttu-id="f0d97-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0d97-131">OUTPUTS</span></span>

## <span data-ttu-id="f0d97-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0d97-132">NOTES</span></span>

## <span data-ttu-id="f0d97-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0d97-133">RELATED LINKS</span></span>

[<span data-ttu-id="f0d97-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0d97-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="f0d97-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0d97-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


