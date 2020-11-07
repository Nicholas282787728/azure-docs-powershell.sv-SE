---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: f99f5742e9719ca9761313cd40d2c996d4e23be9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924910"
---
# <span data-ttu-id="eb317-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb317-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="eb317-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb317-102">SYNOPSIS</span></span>
<span data-ttu-id="eb317-103">Tar bort en konfiguration för nätverks gränssnitt från en VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb317-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="eb317-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb317-104">SYNTAX</span></span>

### <span data-ttu-id="eb317-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb317-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb317-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb317-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb317-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb317-107">DESCRIPTION</span></span>
<span data-ttu-id="eb317-108">Cmdleten **Remove-AzVmssNetworkInterfaceConfiguration** tar bort en konfiguration för nätverks gränssnitt från en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="eb317-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="eb317-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb317-109">EXAMPLES</span></span>

### <span data-ttu-id="eb317-110">Exempel 1: ta bort en gränssnitts konfiguration</span><span class="sxs-lookup"><span data-stu-id="eb317-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="eb317-111">Det första kommandot får en VMSS med hjälp av Get-AzVmss cmdlet och lagrar den i $VMSS-variabeln.</span><span class="sxs-lookup"><span data-stu-id="eb317-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="eb317-112">Med det andra kommandot tas konfigurationen för nätverks gränssnittet bort med namnet ContosoVmssInterface02 från uppsättningen i $VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb317-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="eb317-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb317-113">PARAMETERS</span></span>

### <span data-ttu-id="eb317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb317-114">-DefaultProfile</span></span>
<span data-ttu-id="eb317-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb317-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb317-116">-ID</span><span class="sxs-lookup"><span data-stu-id="eb317-116">-Id</span></span>
<span data-ttu-id="eb317-117">Anger ID: t för nätverks gränssnitts konfigurationen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="eb317-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb317-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb317-118">-Name</span></span>
<span data-ttu-id="eb317-119">Anger namnet på den nätverks gränssnitts konfiguration som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="eb317-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb317-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb317-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="eb317-121">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="eb317-121">Specifies the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb317-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb317-122">-Confirm</span></span>
<span data-ttu-id="eb317-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb317-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb317-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb317-124">-WhatIf</span></span>
<span data-ttu-id="eb317-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb317-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb317-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb317-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb317-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb317-127">CommonParameters</span></span>
<span data-ttu-id="eb317-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb317-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb317-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb317-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb317-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb317-130">INPUTS</span></span>

### <span data-ttu-id="eb317-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb317-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="eb317-132">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb317-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="eb317-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb317-133">OUTPUTS</span></span>

### <span data-ttu-id="eb317-134">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="eb317-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="eb317-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb317-135">NOTES</span></span>

## <span data-ttu-id="eb317-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb317-136">RELATED LINKS</span></span>

[<span data-ttu-id="eb317-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb317-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="eb317-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eb317-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


